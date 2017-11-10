---
title: "Как использовать единицы измерения производственной партии | Документы Майкрософт"
description: "Если при хранении товара используется одна единица измерения, а при производстве — другая, то производственный заказ должен использовать единицы измерения производственной партии для расчета правильного количества компонентов. Примером расчета единицы измерения производственной партии является ситуация, когда хранение товара на складе осуществляется поштучно, а производство — в тоннах."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1b075d164e18a52fbda56cced8d88fabc77bec3f
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-manufacturing-batch-units-of-measure"></a>Практическое руководство. Работа с единицами измерения производственной партии
Если при хранении товара используется одна единица измерения, а при производстве — другая, может быть создан производственный заказ, в котором единица измерения производственной партии используется для расчета правильного количества компонентов при выполнении пакетного задания **Обновление произв. заказа**. Примером расчета единицы измерения производственной партии является ситуация, когда хранение товара на складе осуществляется поштучно, а производство — в тоннах.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Создание производственной спецификации с использованием единицы измерения партии  
1.  Единица измерения производственной партии настраивается как альтернативная единица измерения в окне **Товар - единицы измерения** для производимого товара. Единица измерения для партии не заменяет базовую единицу измерения товара.  
2.  Создайте производственную спецификацию для товара, настроенного с использованием единицы измерения производственной партии. Дополнительные сведения см. в разделе [Практическое руководство. Создание производственных спецификаций](production-how-to-create-production-boms.md).  
3.  В поле **Код единицы измерения** выберите единицу измерения производственной партии.  
4.  Для каждой строки производственной спецификации в поле **Количество в** введите количество товаров-компонентов, необходимое для создания данной единицы измерения производственной партии.  
5.  Откройте окно **Карточка товара** для соответствующего товара.  

    На экспресс-вкладке **Пополнение** в поле **Номер производственной спецификации** выберите созданную ранее производственную спецификацию.  
6.  Создайте заголовок производственного заказа, используя настройку товара с единицами измерения производственной партии. Дополнительные сведения см. в разделе [Практическое руководство. Создание производственных заказов](production-how-to-create-production-orders.md).  
7.  Выберите действие **Обновить**, затем выберите кнопку **ОК**.  

Для просмотра результатов перейдите на экспресс-вкладку **Строки**, выберите действие **Строка**, затем выберите действие **Компоненты**. Программа вычислит правильное количество компонентов, необходимое для соблюдения производственной спецификации, используя единицу измерения производственной партии.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Вычисление единицы измерения производственной партии для производственного заказа  
1.  Создайте заголовок производственного заказа, используя настройку товара с единицами измерения производственной партии.  
2.  В поле **Код товара** строки производственного заказа введите тот же номер товара, который был использован в заголовке.  
3.  В поле **Кол-во** введите то же количество, которое указано в заголовке.  
4.  В поле **Код единицы измерения** выберите код единицы измерения производственной партии.  
5.  Выберите действие **Обновить**.
6.  На экспресс-вкладке **Вычислить** снимите флажок **Строки**.  
7.  Нажмите кнопку **ОК**.  
8.  Для просмотра результатов перейдите на экспресс-вкладку **Строки**, выберите действие **Строка**, затем выберите действие **Компоненты**. Правильное количество компонентов, необходимое для соблюдения производственной спецификации, вычисляется с помощью единицы измерения производственной партии.  

## <a name="see-also"></a>См. также  
[Практическое руководство. Создание маршрутов](production-how-to-create-routings.md)  
[Практическое руководство. Создание производственных спецификаций](production-how-to-create-production-boms.md)     
[Настройка производства](production-configure-production-processes.md)  
[Производство](production-manage-manufacturing.md)    
[Планирование](production-planning.md)   
[Наличие](inventory-manage-inventory.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
