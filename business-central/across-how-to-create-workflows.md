---
title: Создание рабочих процессов | Документация Майкрософт
description: Можно создать потоки операций, соединяющие задачи бизнес-процессов, которые выполняются разными пользователями. Системные задачи, такие как автоматический учет, могут включаться в качестве шагов рабочего процесса, предшествующих задачам пользователя или выполняемых после них. Типичные шаги рабочего процесса – запрос и выдача разрешения на создание новых записей.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e6bdc2c57aaf4dfea8cb5df720217a15b315e4df
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785052"
---
# <a name="create-workflows"></a>Создание рабочих процессов
Можно создать потоки операций, соединяющие задачи бизнес-процессов, которые выполняются разными пользователями. Системные задачи, такие как автоматический учет, могут включаться в качестве шагов рабочего процесса, предшествующих задачам пользователя или выполняемых после них. Типичные шаги рабочего процесса – запрос и выдача разрешения на создание новых записей.  

На странице **Рабочий процесс** создайте рабочий процесс, указав в строках связанные с ним шаги. Каждый шаг состоит из события рабочего процесса, ограниченного условиями события, и отклика рабочего процесса, ограниченного параметрами отклика. Шаги рабочего процесса заполняются посредством заполнения полей в строках рабочего процесса из фиксированных списков значений события и отклика, представляющих сценарии, которые поддерживаются кодом приложения.  

При создании рабочих процессов можно скопировать шаги из существующих рабочих процессов из шаблонов рабочих процессов. Шаблоны рабочих процессов не подлежат редактированию и существуют в универсальной версии [!INCLUDE[d365fin](includes/d365fin_md.md)]. Коды для шаблонов процессов, добавленных Майкрософт, имеют приставку "MS-", например "MS-PIW". Дополнительные сведения см. в разделе [Создание рабочих процессов из шаблонов рабочих процессов](across-how-to-create-workflows-from-workflow-templates.md).  

Если бизнес-сценарий требует событий или откликов рабочего процесса, которые не поддерживаются, партнеру Майкрософт придется реализовать их, настроив код приложения.  

> [!NOTE]  
>  Все уведомления о шагах потоков операций отправляются через очередь заданий. Убедитесь, что очередь заданий установленной программы настроена для поддержки уведомлений рабочих процессов, и что установлен флажок **Запускать автоматически из NAS**. Дополнительные сведения см. в разделе [Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Создание потока операций  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Рабочие процессы**, затем выберите соответствующую ссылку.  
2. Выберите действие **Создать**. Откроется страница **Рабочий процесс**.  
3. В поле **Код** введите не более 20 знаков для обозначения рабочего процесса.  
4. Для создания рабочего процесса из шаблона рабочего процесса на странице **Рабочий процесс** выберите действие **Создать рабочий процесс из шаблона**. Дополнительные сведения см. в разделе [Создание рабочих процессов из шаблонов рабочих процессов](across-how-to-create-workflows-from-workflow-templates.md).  
5. В поле **Описание** введите описание рабочего процесса.  
6. В поле **Категория** укажите категорию рабочего процесса.  
7. В поле **Событие "когда"** укажите событие, которое должно произойти для запуска этого шага рабочего процесса.  

    При выборе поля открывается страница **События рабочего процесса**, в котором можно выбрать любое из существующих событий рабочего процесса.  
8. В поле **Условие** укажите одно или несколько условий, которые должны быть соблюдены, чтобы произошло событие, указанное в поле **Событие "когда"**.  

    При выборе этого поля откроется страница **Условия события**, на которой можно выбрать одно из списка полей фильтра, относящихся как условия к рассматриваемому событию. Можно добавить новые поля фильтров, которые будут использоваться в качестве условий события. Фильтры условия события устанавливаются точно так же, как фильтры на страницах запросов отчетов.  

    Если событие рабочего процесса предназначено для изменения определенного поля в записи, откроется страница **Условия события** с параметрами для выбора поля и типа изменения.  

    1.  Для указания изменения поля для события на странице **Условия события** в поле **Поле** выберите поле, которое изменяется.  
    2.  В поле **Оператор** выберите **Уменьшено**, **Увеличено** или **Изменено**.  
9. В поле **Отклик "то"** укажите отклик, который последует при возникновении события рабочего процесса.  

     При выборе этого поля открывается страница **Отклики рабочего процесса**, на которой можно выбрать любой из всех откликов рабочего процесса и задать параметры отклика для выбранного отклика.  
10. На экспресс-вкладке **Параметры для выбранного отклика** задайте параметры для отклика рабочего процесса, выбрав значения в различных полях следующим образом:  

    1.  Чтобы указать параметры для рабочего процесса, предусматривающего отправку уведомления, заполните поля, как описано в следующей таблице.  

        |Поле|Описание|  
        |----------------------------------|---------------------------------------|  
        |**Уведомить отправителя**|Укажите, получит ли автор запроса на утверждение уведомление вместо получателя запроса. Если вы установите флажок, поле **Код пользователя получателя** будет отключено, потому что отправитель запроса получит уведомление. Имя ответа рабочего процесса изменяется соответственно на **Создать уведомление для &lt;Отправитель&gt;**. Если флажок не установлен, имя ответа рабочего процесса — **Создать уведомление для &lt;Пользователь&gt;**.
        |**Код пользователя получателя**|Укажите пользователя, которому должно отправляться уведомление. Примечание. Этот параметр доступен только для откликов рабочего процесса с заполнителем для определенного пользователя. Для откликов рабочих процессов без заполнителей для пользователей получатель уведомления обычно определяется путем настройки пользователя утверждения.|  
        |**Тип операции уведомления**|Указывает, будет ли уведомление рабочего процесса вызвано изменением записи, запросом на утверждение или переданными данными.|
        |**Связать целевую страницу**|Задайте другую страницу в [!INCLUDE[d365fin](includes/d365fin_md.md)], чтобы открывалась ссылка в уведомлении вместо страницы по умолчанию.<br /><br />Обратите внимание, что страница должна иметь ту же исходную таблицу, что и соответствующая запись.|  
        |**Пользовательская ссылка**|Укажите URL-адрес ссылки, которая будет добавлена в уведомление в дополнение к ссылке на страницу в [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Чтобы указать параметры для отклика рабочего процесса, предусматривающего создание запроса на утверждение, заполните поля, как описано в следующей таблице.  

        |Поле|Описание|  
        |----------------------------------|---------------------------------------|  
        |**Формула расчета срока утверждения**|Укажите срок в днях, в течение которого запрос разрешения должен быть рассмотрен после дня его отправки.|  
        |**Делегировать через**|Задайте необходимость и время автоматического делегирования запроса на утверждения соответствующей замене. Можно выбрать автоматическое делегирование через один, два или пять дней после даты запроса утверждения.|  
        |**Тип утверждающего**|Укажите, кто является утверждающим, в соответствии с настройкой пользователей утверждения и пользователей рабочего процесса.<br /><br /> Имеются следующие варианты:<br /><br /> -   **Продавец/покупатель** означает, что пользователь, настроенный в поле **Код менеджера** на странице **Настройка пользователя для утверждений**, определяет утверждающее лицо. Затем создаются операции запросов утверждения в соответствии со значением в поле **Тип лимита утверждающего**.<br />     Дополнительные сведения см. в разделе [Настройка утверждающих пользователей](across-how-to-set-up-workflow-users.md).|  
        |**Показать сообщение подтверждения**|Задайте необходимость отображение для пользователей сообщения с подтверждением после их запроса утверждения.|  
        |**Тип лимита утверждающего**|Укажите, как порядок утверждающих лиц влияет на создание для них операций запроса на утверждение. Квалифицированное утверждающее лицо представляет собой утверждающее лицо, лимит утверждения которого превышает значение, указанное в запросе.<br /><br /> Имеются следующие варианты:<br /><br /> 1.  **Цепочка утверждающих** указывает, что операции запроса на утверждение создаются для всех утверждающих лиц данного запроса вплоть до первого квалифицированного утверждающего лица.<br />2.  **Прямой утверждающий** указывает, что операция запроса утверждения создана только для непосредственного утверждающего лица запрашивающей стороны, независимо от лимита утверждения данного утверждающего лица.<br />3.  **Первый квалифицированный утверждающий** указывает, что операция запроса на утверждение создана только для первого квалифицированного утверждающего.<br />|  
    3.  Чтобы задать параметры для рабочего процесса, предусматривающего создание строк журнала, заполните поля, как описано в следующей таблице.  

        |Поле|Описание|  
        |----------------------------------|---------------------------------------|  
        |**Название шаблона финансового журнала**|Определите имя шаблона финансового журнала, в котором создаются указанные строки журнала.|  
        |**Название раздела финансового журнала**|Определите имя шаблона пакета финансового журнала, в котором создаются указанные строки журнала.|  

11. Выберите кнопки **Увеличить отступ** и **Уменьшить отступ** для установки отступа имени события в поле **Когда**, чтобы задать положение шага в рабочем процессе.  
    1.  Укажите, что этот шаг являются следующим в последовательности рабочего процесса, задав отступ для имени события больше отступа для имени события предыдущего шага.  
    2.  Укажите, что шаг является одним из нескольких альтернативных шагов, который может начаться при выполнения соответствующего условия, поместив имя события на том же уровне отступа, что и другие альтернативные шаги. Организуйте такие дополнительные шаги по приоритету, поместив самый важный шаг первым.  

    > [!NOTE]  
    >  Изменение отступа возможно только для шага, который не имеет последующего шага.  

12. Повторите шаги 7 – 11 для добавления других шагов рабочего процесса перед только что созданным шагом или после него.  
13. Установите флажок **Включено**, чтобы указать, что рабочий процесс начнется сразу при возникновении события в первом шаге типа **Точка входа**. Дополнительные сведения см. в разделе [Использование рабочих процессов](across-use-workflows.md).  

> [!NOTE]  
>  Не включайте поток операций, пока не уверены, что этот поток операций завершен и могут быть запущены соответствующие шаги потока операций.  

> [!TIP]  
>  Чтобы просматривать связи между таблицами, используемыми в рабочих процессах, выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), затем введите **Связи таблица - рабочий процесс**.  

## <a name="see-also"></a>См. также  
[Создание рабочих процессов из шаблонов рабочих процессов](across-how-to-create-workflows-from-workflow-templates.md)   
[Настройка утверждающих пользователей](across-how-to-set-up-approval-users.md)   
[Настройка уведомлений рабочего процесса](across-setting-up-workflow-notifications.md)   
[Просмотр архивированных экземпляров шагов рабочих процессов](across-how-to-view-archived-workflow-step-instances.md)   
[Удаление рабочих процессов](across-how-to-delete-workflows.md)   
[Пошаговое руководство. Настройка и использование рабочего процесса утверждения покупки](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Настройка рабочих процессов](across-set-up-workflows.md)   
[Использование рабочих процессов](across-use-workflows.md)   
[Рабочий процесс](across-workflow.md)      
