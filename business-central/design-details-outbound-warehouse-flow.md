---
title: Сведения о проектировании — исходящий складской поток | Документация Майкрософт
description: Исходящий поток на складе начинается с запроса из документов-источников выпуска о необходимости переместить товары со склада — отправить третьей стороне или на другой склад. Из зоны хранения складские операции выполняются на разных уровнях сложности для перемещения товаров в зоны отгрузки.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/07/2020
ms.author: edupont
ms.openlocfilehash: aa12b250f404f149d790b0768560cad958c26d31
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787425"
---
# <a name="design-details-outbound-warehouse-flow"></a>Сведения о проектировании: исходящий складской поток

Исходящий поток на складе начинается с запроса из документов-источников выпуска о необходимости переместить товары со склада — отправить третьей стороне или на другой склад. Из зоны хранения складские операции выполняются на разных уровнях сложности для перемещения товаров в зоны отгрузки.  

 Каждый товар определяется и сопоставляется с соответствующим входящим документом-источником. Существуют следующие исходящие документы-источники.  

- Заказ на продажу  
- Заказ на исходящее перемещение  
- Возврат покупки  
- Сервисный заказ  

Кроме того, существуют следующие внутренние документы-источники, которые служат исходящими источниками.  

- Производственный заказ с потребностью в компоненте  
- Заказ на сборку с потребностью в компоненте  

 Последние два документа представляют исходящие потоки со склада во внутренние операционные области. Дополнительные сведения об обработке склада для внутренних исходящих и входящих процессов см. в разделе [Сведения о проектировании: внутренние складские потоки](design-details-internal-warehouse-flows.md).  

 Процессы и документы пользовательского интерфейса в исходящих складских потоках отличаются для базовой и расширенной конфигураций склада. Основное различие в том, что действия выполняются на уровне отдельных заказов в базовых конфигурациях складирования и они консолидируются для нескольких заказов в расширенных конфигурациях складирования. Дополнительные сведения о различных уровнях сложности склада см. в разделах [Сведения о проектировании: обзор склада](design-details-warehouse-setup.md).  

 В [!INCLUDE[d365fin](includes/d365fin_md.md)] исходящие процессы по подбору и отгрузке мажут быть выполнены четырьмя способами при помощи различных функций в зависимости от уровня сложности склада.  

|Метод|Исходящий процесс|Ячейки|Складской подбор|Расх. накладные|Уровень сложности (см. раздел [Сведения о проектировании: настройка склада](design-details-warehouse-setup.md))|  
|------|----------------|----|-----|---------|-------------------------------------------------------------------------------------|  
|П|Выполните учет подбора и отгрузки из строки заказа|X|||2|  
|Б|Выполните учет подбора и отгрузки из складского документа подбора||X||3|  
|C|Выполните учет подбора и отгрузку из документа складской отгрузки|||X|4/5/6|  
|D|Выполните учет подбора из складского документа подбора и учет отгрузки из документа складской отгрузки||X|X|4/5/6|  

 Выбор подхода зависит от принятых в организации практик и уровня организационной сложности. В среде последовательного выполнения заказов с простыми процессами и простой структурой ячеек можно выполнять (метод А) подбор и отгрузку из строки заказа. В других организациях, выполняющих заказы последовательно, где товары для одной строки заказа могут поступать из нескольких ячеек или где работники склада не могут работать с документами заказов, рекомендуется использовать отдельные документы подбора (метод В). Если в процессах подбора и отгрузки организации обрабатывается несколько заказов и, следовательно, требуется более четкое управления и обзор, рекомендуется использовать документ складской отгрузки и документ складского подбора для разделения задачи по подбору и отгрузке (методы С и D).  

 При использовании методов A, B и C действия подбора и отгрузки объединены в один шаг при учете соответствующего документа как отгруженного. При использовании метода D сначала регистрируется подбор, а затем через некоторое время учитывается отгрузка из другого документа.  

## <a name="basic-warehouse-configurations"></a>Базовые конфигурации склада

 На следующей схеме показаны исходящие складские потоки по типам документов в базовых конфигурациях склада. Номер на схеме соответствует шагам в разделах после схемы.  

 ![Исходящий поток в базовых конфигурациях склада](media/design_details_warehouse_management_outbound_basic_flow.png "Исходящий поток в базовых конфигурациях склада")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1. Выпуск документа-источника / Создание подбора запасов или перемещение

 Если пользователь, ответственный за документы-источники, например ответственный за обработку заказа на продажу или планировщик производства, готов к исходящей складской операции, он или она выпускает документ-источник, чтобы сигнализировать работникам склада, что проданные товары или компоненты можно комплектовать и размещать в указанные ячейки. Либо пользователь может создать складские документы комплектования или перемещения для отдельных строк заказа в принудительном порядке с учетом заданных ячеек и обрабатываемых количеств.  

> [!NOTE]  
> Перемещения запасов используются для перемещения товаров в области внутренних операций в базовых конфигурациях склада на основе документов-источников или в зависимости от конкретной ситуации.  

### <a name="2-create-outbound-request"></a>2. Создание исходящего запроса

 При выпуске исходящего документа-источника автоматически создается исходящий складской запрос. Он содержит ссылки на тип и номер документа-источника и не отображается для пользователя.  

### <a name="3-create-inventory-pick-or-movement"></a>3. Создание подбора запасов или перемещение

 На странице **Подбор запасов** или **Перемещение запасов** работник склада извлекает ожидающие строки документа-источника в режиме извлечения на основе исходящих складских запросов. В качестве альтернативы строки подбора запасов уже созданы в режиме распределения пользователем, отвечающим за документ-источник.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4. Учет подбора запасов или регистрация перемещения запасов

 В каждой строке товаров, которые были полностью или частично подобраны или перемещены, работник склада заполняет поле **Количество**, а затем учитывает складской подбор или регистрирует перемещение запасов. Документы-источники, связанные со складским подбором, учитываются как отгруженные или потребленные. Документы-источники, связанные с перемещениями запасов, не учитываются.  

 Для складских подборов создаются отрицательные операции книги товаров, создаются складские операции и удаляется запрос на подбор, если обработка выполнена в полном объеме. Например, обновляется поле **Отгруженное кол-во** в исходящей строке документа-источника. Создается учтенный документ отгрузки, например, со сведениями о заказе на продажу и отгруженными товарами.  

## <a name="advanced-warehouse-configurations"></a>Расширенные конфигурации склада

 На следующей схеме показан исходящий складской поток по типу документов в расширенных конфигурациях склада. Номер на схеме соответствует шагам в разделах после схемы.  

 ![Исходящий поток в расширенных конфигурациях склада](media/design_details_warehouse_management_outbound_advanced_flow.png "Исходящий поток в расширенных конфигурациях склада")  

### <a name="1-release-source-document"></a>1. Выпуск документа-источника

 Если пользователь, ответственный за документы-источники, например ответственный за обработку заказа на продажу или планировщик производства, готов к исходящей складской операции, он или она выпускает документ-источник, чтобы сигнализировать работникам склада, что проданные товары или компоненты можно комплектовать и размещать в указанные ячейки.  

### <a name="2-create-outbound-request-2"></a>2: Создание исходящего запроса (2)

 При выпуске исходящего документа-источника автоматически создается исходящий складской запрос. Он содержит ссылки на тип и номер документа-источника и не отображается для пользователя.  

### <a name="3-create-warehouse-shipment"></a>3. Создание складской отгрузки

 На странице **Складская отгрузка** ответственный экспедитор извлекает ожидающие строки документа-источника на основе исходящего складского запроса. Несколько строк документа-источника можно объединить в один документ складской отгрузки.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4. Выпуск отгрузки / Создание подбора запасов

 Ответственный сотрудник по отгрузке инициирует отгрузку со склада, чтобы работники склада смогли создать или скоординировать отборы со склада для соответствующей отгрузки.  

 В качестве альтернативы пользователь может создать документ складского подбора для отдельных строк отгрузки в режиме распределения на основе указанных ячеек и количеств для обработки.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5. Выпуск внутренней операции / Создание складского подбора

 Пользователь, ответственный за внутренние операции, выпускает внутренний документ-источник, например производственный заказ или заказ на сборку, чтобы сотрудники склада могли создать или скоординировать складские подборы для соответствующей внутренней операции.  

 В качестве альтернативы пользователь может создать документы складского подбора для отдельного производственного заказа или заказа на сборку в режиме распределения на основе указанных ячеек и количеств для обработки.  

### <a name="6-create-pick-request"></a>6. Создание запроса на подбор

 При выпуске исходящего документа-источника автоматически создается запрос на подбор на складе. Он содержит ссылки на тип и номер документа-источника и не отображается для пользователя. В зависимости от настройки потребление производства и заказов на сборку также создает запрос подбора для подбора необходимых компонентов из запасов.  

### <a name="7-generate-pick-worksheet-lines"></a>7. Создание строк журнала подбора

 Пользователь, ответственный за согласование подборов, извлекает строки складского подбора из документа **Журнал подбора** на основе запросов на подбор от складских отгрузок или внутренних операций с потреблением компонентов. Пользователь выбирает строки для комплектования и подготавливает комплектование, указывая, из каких ячеек брать товар, в каких ячейках его размещать и сколько единиц товара обрабатывать. Ячейки могут быть предопределены настройкой местоположения склада или ресурса операции.  

 Пользователь задает методы комплектования для оптимизированного складского хранения, а затем пользуется функцией для создания соответствующих документов складского подбора, которые назначаются разным складским рабочим, выполняющим складские подборы. Если подборы на складе полностью назначены, строки в документе **Журнал подбора** удаляются.  

### <a name="8-create-warehouse-pick-documents"></a>8. Создание документов складского подбора

 Сотрудник склада, выполняющий подборы, создает документ складского подбора в режиме извлечения на основе выпущенного документа-источника. В качестве альтернативы создается документ складского подбора, который назначается работнику склада в режиме распределения.  

### <a name="9-register-warehouse-pick"></a>9. Регистрация складского подбора

 В каждой строке товаров, которые были полностью или частично подобраны, работник склада заполняет поле **Количество** на странице **Складской подбор**, а затем регистрирует складской подбор.  

 Создаются складские операции, а строки складского подбора удаляются, если были полностью обработаны. Документ складского подбора остается открытым до тех пор, пока не будет зарегистрировано полное количество соответствующей складской отгрузки. Поле **Подобр. кол-во** в строках складской отгрузки обновляется соответственно.  

### <a name="10-post-warehouse-shipment"></a>10. Учет складских отгрузок

 Если все элементы в документе складской отгрузки зарегистрированы как подобранные в указанные ячейки отгрузки, ответственный сотрудник склада учитывает складскую отгрузку. Создаются отрицательные операции книги товаров. Например, обновляется поле **Отгруженное кол-во** в исходящей строке документа-источника.  

## <a name="see-also"></a>См. также

[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
