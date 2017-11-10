---
title: "Создание XMLports на основе XML-схем | Документы Майкрософт"
description: "Используйте XML-схемы для настройки платформы обмена документами."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: d44e4f55dc43e4ad6b8e8bc1742eed3c966eb918
ms.contentlocale: ru-ru
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a>Практическое руководство. Использование XML-схем для определения обмена данными
Чтобы разрешить импорт или экспорт данных в файл в формате XML с использованием платформы обмена данными в [!INCLUDE[d365fin](includes/d365fin_md.md)], можно воспользоваться XML-схемами для определения элементов данных, которыми можно обмениваться с [!INCLUDE[d365fin](includes/d365fin_md.md)]. Эта работа выполняется в окне **Средство просмотра схем XML** путем загрузки файла XML-схемы. Для этого нужно выбрать соответствующие элементы данных и инициализировать определение обмена данными или XMLport.  

 Определив, какие элементы данных необходимо включить с учетом XML-схемы, можно воспользоваться действием **Создать XMLport** для создания объекта XMLport.  

 Кроме того, можно использовать действие **Создать определение обмена данными**, чтобы инициализировать определение обмена данными на основании выбранных элементов данных, которую затем можно закончить в структуре обмена данными. В результате создается запись в окне **Определения учета обмена**, где затем определяется, какие элементы в файле сопоставляются полям в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Практическое руководство. Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md).  

 Этот раздел содержит следующие процедуры:  

-   загрузка файла XML-схемы  

-   Выбор или удаление узлов в XML-схеме  

-   Создание определения обмена данными на базе XML-схемы  

-   Создание XMLport для файла на основе XML-схемы  

-   Импорт XMLport в конструктор объектов  

### <a name="to-load-an-xml-schema-file"></a>загрузка файла XML-схемы  

1.  Убедитесь, что доступен соответствующий файл XML-схемы. Расширение файла – XSD.  

2.  В поле **Поиск** введите **Схемы XML**, а затем выберите связанную ссылку.  

3.  На вкладке **Главная** в группе **Создать** выберите **Создать**.  

4.  Заполните поля, как описано в следующей таблице.  

    |Поле|[Описание]|  
    |---------------------------------|---------------------------------------|  
    |**Код**|Указание кода для определения XML-схемы.|  
    |**Описание**|Указание описания XML-схемы.|  

     В поле **Целевое пространство имен** задается любое пространство имен из файла XML-схемы, загруженного для соответствующей строки.  

5.  На вкладке **Главная** в группе **Процесс** выберите **Загрузить схему**, затем выберите файл XML-схемы.  

     Если файл загружен, остальные поля в строке заполняются сведениями из этого файла, а также устанавливается флажок **Схема загружена**.  

    > [!NOTE]  
    >  Дерево загруженной XML-схемы по умолчанию свернуто. Можно развернуть каждый узел нажатием кнопки **+** на нем. Чтобы развернуть все узлы, выберите **Раскрыть все** на ленте.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Выбор или удаление узлов в XML-схеме  

1.  В поле **Поиск** введите **Средство просмотра схем XML**, а затем выберите связанную ссылку.  

2.  Заполните поля в заголовке, как описано в следующей таблице.  

    |Поле|Описанием|  
    |---------------------------------|---------------------------------------|  
    |**Код схемы XML**|Укажите файл XML-схемы, загруженный на шаге 5 в разделе "Загрузка файла XML-схемы".|  
    |**Новый номер XMLport**|Укажите номер XMLport, созданного из схемы XML при выборе действия **Создать XMLport**.|  

     Строки заполняются узлами, представляющими все элементы в XML-схеме. Узлы для элементов, которые являются обязательными согласно XML-схеме, выбираются по умолчанию.  

3.  В первой строке в столбце **Название узла** разверните узел **Документ** и постепенного разворачивайте дочерние узлы, которые необходимо просмотреть.  

     В качестве альтернативы щелкните правой кнопкой мыши и выберите **Развернуть все**.  

4.  На вкладке **Главная** в группе **Вид** выберите одно из следующих действий, чтобы изменить узлы для отображения.  

    |**Действие**|Описанием|  
    |----------------|---------------------------------------|  
    |**Показать все**|Отображаются все узлы.|  
    |**Скрыть необязательные**|Отображаются только узлы, представляющие элементы, необходимые согласно XML-схеме. Обычно эти узлы обозначаются **1** в поле **MinOccurs**.<br /><br /> Щелкните **Показать все** для сторнирования представления.|  
    |**Скрыть невыбранные**|Отображаются только узлы, в которых установлен флажок **Выбрано**.<br /><br /> Щелкните **Показать все** для сторнирования представления.|  

5.  На вкладке **Главная** в группе **Управление** выберите **Правка**.  

6.  С помощью флажка **Выбрано** можно для каждого узла указать, требуется ли включить поддержку элемента в определении обмена данными для связанного файла банка SEPA.  

    > [!NOTE]  
    >  При выборе обязательного дочернего узла все родительские узлы над ним также выбираются.  

7.  Выберите действие **Выбрать все обязательные элементы**, чтобы снова выбрать все узлы, представляющие элементы, которые являются обязательными согласно XML-схеме.  

8.  Выберите действие **Снять выделение** для отмены выбора всех элементов.  

     В поле **Выбор** указано, что у узла имеется два или более дочерних узла, которые функционируют как параметры.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Создание определения обмена данными на базе XML-схемы  

1.  В поле **Поиск** введите **Схемы XML**, а затем выберите связанную ссылку.  

2.  Выберите соответствующую XML-схему, а затем на вкладке **Главная** в группе **Процесс** выберите **Открыть средство просмотра XML-схем**.  

3.  Убедитесь, что выбраны соответствующие узлы. Дополнительные сведения см. в разделе "Выбор или отмена выбора узлов на XML-схеме".  

4.  В окне **Средство просмотра схем XML** на вкладке **Главная** в группе **Процесс** выберите **Создать определение обмена данными**.  

 Запись определения обмена данными создается в окне **Определения учета обмена**, которое можно заполнить, указав, какие элементы файла сопоставляются с какими полями в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Практическое руководство. Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Можно также использовать функцию **Получить структуру файла** из окна **Определения учета обмена**, использующую функциональные возможности окна **Средство просмотра схем XML** для предварительного заполнения экспресс-вкладки **Определения столбца**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Создание XMLport на базе XML-схемы  

1.  В поле **Поиск** введите **Схемы XML**, а затем выберите связанную ссылку.  

2.  Выберите соответствующую XML-схему, а затем на вкладке **Главная** в группе **Процесс** выберите **Открыть средство просмотра XML-схем**.  

3.  В поле **Новый номер XMLport** укажите номер, который будет присвоен новому объекту XMLport при его создании.  

4.  Убедитесь, что выбраны соответствующие узлы. Дополнительные сведения см. в разделе "Выбор или отмена выбора узлов на XML-схеме".  

5.  На вкладке **Главная** в группе **Процесс** выберите **Создать XMLPort** и сохраните объект как TXT-файл в соответствующем местоположении.  

6. Импортируйте новый XMLport в среду разработки [!INCLUDE[d365fin](includes/d365fin_md.md)] и скомпилируйте его.

## <a name="see-also"></a>См. также  
[Практическое руководство. Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md)   
[Практическое руководство. Экспорт платежей в банковский файл](payables-how-export-payments-bank-file.md)   
[Сбор платежей с прямым дебетом SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[О структуре обмена данными](across-about-the-data-exchange-framework.md)
