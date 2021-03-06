---
title: Сведения о проектировании — обработка политик дозаказа | Документация Майкрософт
description: Обзор задач для определения политики повтора заказа при планировании поставок.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8cf4d954171e663ed065128a91c313f6e38b9148
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787925"
---
# <a name="design-details-handling-reordering-policies"></a>Сведения о проектировании: обработка политик дозаказа
Чтобы товар мог участвовать в планировании поставок, должна быть определена политика дозаказа. Существует четыре следующих политики повторного заказа.  

* Фикс. кол-во повтора заказа  
* Максимальное кол-во  
* Заказ  
* Партия на партию  

Политики "Фикс. кол-во дозаказа" и "Максимальное кол-во" относятся к планированию запасов. Хотя планирование запасов технически проще процедуры балансировки, эти политики должны сосуществовать с поэтапной балансировкой поставок и трассировкой заказов. Для контроля интеграции между этими двумя сущностями и обеспечения обзорности соответствующей логики планирования, строгие принципы регулируют работу с политиками повторных заказов.  

## <a name="the-role-of-the-reorder-point"></a>Роль точки дозаказа
В дополнение к общей балансировке спроса и поставки система планирования также отслеживает уровни запасов для соответствующих товаров, чтобы соблюсти требования политики дозаказа.  

Точка дозаказа представляет спрос во время подготовки. Когда прогнозируемые запасы опускаются ниже уровня запасов, определенного точкой повторного заказа, время заказывать дополнительное количество. В то же время ожидается, что запас будет постепенно уменьшатся и, возможно, достигнет нуля (или уровня страхового запаса), пока не поступит пополнение.  

Соответственно, система планирования предложит заказ на поставку с прямым планированием в момент перехода прогнозируемых запасов ниже точки дозаказа.  

Точка повторного заказа отражает определенный уровень запасов. Однако уровни запасов могут сильно перемещаться в горизонте планирования, и, следовательно, система планирования должна постоянно контролировать прогнозируемые доступные запасы.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Отслеживание уровня прогнозируемых запасов и точки дозаказа
Запасы — это тип поставки, но для планирования запасов система планирования разделяет два уровня запасов:  

* Прогнозируемые запасы  
* Прогнозируемые доступные запасы  

### <a name="projected-inventory"></a>Ожидаемые запасы  
Изначально в начале процесса планирования прогнозируемые запасы представляют собой количество общих запасов, включая поставку и спрос в прошлом, даже если они не учтены. В будущем это становится изменяющимся прогнозируемым уровнем запасов, который поддерживается общими количествами из будущей поставки и спроса, поскольку они вводятся со временем (независимо от того, зарезервированы они или размещены иным способом).  

Прогнозируемые запасы используются системой планирования для мониторинга точки повторного запаса и определения количества повторного запаса при использовании политики повторного заказа "Макс. кол-во".  

### <a name="projected-available-inventory"></a>Прогнозируемые доступные запасы  
Прогнозируемые доступные запасы являются частью прогнозируемых запасов, которая на данный момент доступна для удовлетворения спроса. Прогнозируемые доступные запасы используются механизмом планирования при мониторинге уровня страхового запаса.  

Прогнозируемые доступные запасы используются системой планирования для мониторинга уровня страховых запасов, поскольку страховые запасы всегда должны быть доступны для обслуживания неожиданного спроса.  

### <a name="time-buckets"></a>Горизонты планирования  
Обеспечение жесткого контроля прогнозируемых запасов очень важно для определения того, когда достигается или пересекается точка дозаказа, и для расчета правильного количества заказа при использовании политики дозаказа "Максимальное кол-во".  

Как указано ранее, прогнозируемый уровень запасов рассчитывается в начале периода учета. Это общий уровень, на котором не учитываются резервирования и похожие распределения. Для мониторинга этого уровня запасов в последовательности планирования система отслеживает совокупные изменения за период времени или горизонт планирования. Система гарантирует, что горизонт планирования равен хотя бы одному дню, поскольку это самая точная единица времени для события спроса или поставки.  

### <a name="determining-the-projected-inventory-level"></a>Определение уровня прогнозируемых запасов  
Следующая последовательность описывает определение прогнозируемого уровня запасов.  

* Если событие поставки, например заказ на покупку, полностью спланировано, увеличиваются ожидаемые запасы в дату оплаты.  
* Если событие спроса полностью удовлетворено, прогнозируемый расход склада не будет осуществляться сразу же. Вместо этого учитывается напоминание об уменьшении, которое является внутренней записью, содержащей дату и количество вклада в прогнозируемые запасы.  
* Если планируется последующее событие поставки и оно размещается на временной шкале, учтенные напоминания о расходе изучаются по одному до планируемой даты поставки. При этом обновляются ожидаемые запасы. Во время данного процесса уровень точки дозаказа внутреннего напоминания об увеличении может быть достигнут или пройден.  
* Если введен новый заказ на поставку, система проверяет, был ли он введен до текущей поставки. В этом случае новая поставка становится текущей поставкой, и процедура балансировки начинается снова.  

Далее этот принцип проиллюстрирован графически.  

![Определение уровня прогнозируемых запасов](media/nav_app_supply_planning_2_projected_inventory.png "Определение уровня прогнозируемых запасов")  

1. Поставка **Sa** на 4 штуки (фиксированная) закрывает спрос **Da** на -3 штуки.  
2. CloseDemand: создается напоминание об уменьшении на -3 (не показано).  
3. Поставка **Sa** закрыта с излишком 1 (спрос больше не существует).  

     В результате прогнозируемый уровень склада увеличивается до +4, а прогнозируемые **доступные** запасы равны -1.  

4. Следующая поставка **Sb** на 2 штуки (другой заказ) уже помещена на временную шкалу.  
5. Система проверяет, имеется ли напоминание об уменьшении, предшествующее **Sb** (если нет, никакие действия не предпринимаются).  
6. Система закрывает поставку **Sb** (спрос больше существует) либо A: путем снижения количества до значения 0 (отмена), либо B: оставляя ее как есть.  

     Это увеличивает прогнозируемый уровень запаса (A: +0 => +4 or B: +2 = +6).  

7. Система выполняет окончательную проверку на наличие напоминания об уменьшении. Да, имеется один в дату **Da**.  
8. Система добавляет напоминание об уменьшении, равном -3, к прогнозируемому уровню запасов одним из двух способов: A: +4 -3 = 1 или B: +6 -3 = +3.  
9. В случае А система создает заказ с прямым планирование, начиная с даты **Da**.  

     В случае B достигается точка дозаказа и создается новый заказ.

## <a name="the-role-of-the-time-bucket"></a>Роль горизонта планирования
Цель горизонта планирования — сбор событий спроса на странице времени с целью составления совместного заказа на поставку.  

Для политик дозаказа, в которых используется точка дозаказа, можно определить горизонт планирования. Это обеспечивает аккумуляцию спроса в одном временном периоде до проверки влияния на прогнозируемые запасы и проверки прохождения точки повторного заказа. Если точка дозаказа пройдена, планируется новый заказ на поставку на дату после даты конца периода, указанного в горизонте планирования. Горизонты планирования начинаются в начальную дату планирования.  

Концепция горизонтов планирования отражает осуществляемый вручную процесс проверки уровня запасов на регулярной основе, а не для каждой транзакции. Пользователю требуется определить периодичность (горизонт планирования). Например, пользователь объединяет все потребности в товарах для одного поставщика для размещения еженедельного заказа.  

![Пример горизонта планирования](media/nav_app_supply_planning_2_reorder_cycle.png "Пример горизонта планирования")  

Горизонт планирования, как правило, используется для того, чтобы избежать каскадного эффекта. Например, создается сбалансированная строка спроса и поставки, в которой отменяется преждевременный спрос. Результатом будет перепланирование всех заказов на поставку (кроме последнего).

## <a name="staying-under-the-overflow-level"></a>Нахождение ниже уровня допустимого избытка
При использовании политик максимального количества и фиксированного количества повторного заказа система планирования концентрируется на прогнозируемых складских запасов исключительно в данном горизонте планирования. Это означает, что система планирования может предложить поставку с излишками, если происходят изменения отрицательного спроса или положительного предложения за пределами заданного горизонта планирования. Если, по этой причине предлагается излишняя поставка, система планирования вычисляет количество, на которое следует уменьшить поставку, чтобы избежать излишней поставки. Это количество называется "допустимый избыток". Он передается как строка планирования с действием **Изменить кол-во (уменьшить)** или **Отмена** и следующим предупреждением.  

*Внимание! Прогнозируемые запасы [xx] больше, чем допустимый избыток [xx] на срок выполнения [xx].*  

![Допустимый избыток запасов](media/supplyplanning_2_overflow1_new.png "Допустимый избыток запасов")  

###  <a name="calculating-the-overflow-level"></a>Расчет допустимого избытка  
Допустимый избыток вычисляется разными способами в зависимости от настройки планирования.  

#### <a name="maximum-qty-reordering-policy"></a>Политика дозаказа "Максимальное кол-во"  
Допустимый избыток = Максимальный запас  

> [!NOTE]  
>  Если существует минимальное количество заказа, оно будет добавлено следующим образом: допустимый избыток = максимальный запас + минимальное количество заказа.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Политика дозаказа "Фикс. кол-во дозаказа"  
Допустимый избыток = кол-во для дозаказа + точка дозаказа  

> [!NOTE]  
>  Если минимальное количество заказа выше точки дозаказа, оно заменяется следующим образом: допустимый избыток = количество дозаказа + минимальное количество заказа  

#### <a name="order-multiple"></a>Заказать несколько  
Если существует множитель заказа, он корректирует допустимый избыток для политик дозаказа "Максимальное кол-во" и "Фикс. кол-во дозаказа".  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Создание строки планирования с предупреждением о переполнении  
Если из-за существующей поставки прогнозируемые запасы выше допустимого избытка по окончании горизонта планирования, создается строка планирования. Чтобы предупредить о возможных излишках поставки, строка планирования содержит предупреждение, поле **Принять указание** не выбрано, а указание имеет значение "Отмена" или "Изменить кол-во".  

#### <a name="calculating-the-planning-line-quantity"></a>Расчет количества строки планирования  
Количество строки планирования = текущее количество поставки - (ожидаемые запасы - допустимый избыток)  

> [!NOTE]  
>  Как и во всех строках предупреждений любое максимальное/минимальное количество заказа или множитель заказа будут игнорироваться.  

#### <a name="defining-the-action-message-type"></a>Определение типа сообщения о действии  

-   Если количество в строке планирования выше или равно 0, отображается сообщение о действии "Изменить кол-во".  
-   Если количество в строке планирования ниже или равно 0, отображается сообщение о действии "Отмена".  

#### <a name="composing-the-warning-message"></a>Создание предупреждающего сообщения  
В случае избытка на странице **Нетрассируемые элементы планирования** отображается предупреждающее сообщение со следующими сведениями:  

-   Прогнозируемый уровень запасов, инициировавший предупреждение  
-   Вычисленный допустимый избыток  
-   Дата оплаты события предложения.  

Пример. Прогнозируемые запасы 120 больше, чем допустимый избыток 60 в 28-01-11  

### <a name="scenario"></a>Сценарий  
В этом сценарии клиент меняет количество заказа на продажу с 70 на 40 штук в период между двумя процессами планирования. Функция переполнения устанавливается для уменьшения покупки, которая была предложена для первоначального количества продаж.  

#### <a name="item-setup"></a>Настройка товара  

|Политика дозаказа|Максимальное кол-во|  
|-----------------------|------------------|  
|Максимальное кол-во заказа|100|  
|Точка дозаказа|50|  
|Запасы|80|  

#### <a name="situation-before-sales-decrease"></a>Ситуация до снижения продаж  

|Событие|Изменить кол-во|Ожидаемые запасы|  
|-----------|-----------------|-------------------------|  
|День первый|Нет|80|  
|Продажа|-70|10|  
|Конец горизонта планирования|Нет|10|  
|Предложение нового возврата покупки|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Ситуация после снижения продаж  

|Изменение|Изменить кол-во|Ожидаемые запасы|  
|------------|-----------------|-------------------------|  
|День первый|Нет|80|  
|Продажа|-40|40|  
|Покупка|+90|130|  
|Конец горизонта планирования|Нет|130|  
|Предложение по уменьшению количества покупки<br /><br /> заказ с 90 до 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Результирующие строки планирования  
 Создается одна строка планирования (предупреждение) для уменьшения количества покупки 30 с 90 до 60 для соответствия прогнозируемых запасов 100 допустимому избытку.  

![Планирование в соответствии с допустимым избытком](media/nav_app_supply_planning_2_overflow2.png "Планирование в соответствии с допустимым избытком")  

> [!NOTE]  
>  Без функции допустимого избытка никаких предупреждений не создается, если прогнозируемый уровень склада выше максимальных запасов. Это может вызвать поставку с излишками в количестве 30.

## <a name="handling-projected-negative-inventory"></a>Обработка прогнозируемых отрицательных остатков
Точка повторного заказа выражает предполагаемый спрос во время подготовки товара. Когда точка дозаказа пройдена, нужно заказывать еще. Однако прогнозируемые запасы должны быть достаточно большими для того, чтобы удовлетворить спрос до получения нового заказа. В то же время страховой запас должен устранить колебания в спросе и увеличить количество до целевого уровня обслуживания.  

 Следовательно, система планирования считает, что возникла чрезвычайная ситуация, если будущий спрос невозможно удовлетворить из прогнозируемых запасов, или, иными словами, если прогнозируемые запасы становятся отрицательными. Система обрабатывает такое исключение, предлагая новый заказ на поставку, чтобы покрыть часть спроса, который не может быть покрыт поставкой со склада или другой поставкой. Размер нового заказа на поставку не учитывает максимальные запасы или количество повторного запаса, а также модификаторы заказа, такие как "максимальное кол-во заказа", "минимальное кол-во заказа" и "заказать несколько". Вместо этого будет отражен точный дефицит.  

 Строка планирования для этого типа заказов на поставку отобразит предупреждающий значок аварийной ситуации с возможностью просмотра пользователем дополнительных сведений для прояснения ситуации.  

 На следующем рисунке поставка D представляет экстренный заказ для коррекции отрицательных остатков.  

 ![Предложение экстренного планирования для предотвращения отрицательных остатков](media/nav_app_supply_planning_2_negative_inventory.png "Предложение экстренного планирования для предотвращения отрицательных остатков")  

1.  Поставка **A** (изначально прогнозируемые запасы) ниже точки дозаказа.  
2.  Создана новая поставка с прямым планированием (**C**).  

     (Количество = максимальный запас - уровень прогнозируемых запасов)  
3.  Поставка **A** закрыта спросом **B**, который удовлетворен в полном размере.  

     (В соответствии со спросом **B** можно попытаться запланировать поставку C, однако это будет невозможно согласно понятию "горизонт планирования".)  
4.  Создается новая поставка (**D**) для покрытия оставшегося количества в спросе **B**.  
5.  Спрос **B** закрыт (создание напоминания для прогнозируемых запасов).  
6.  Новая заявка **D** закрыта.  
7.  Ожидаемые запасы проверены; точка дозаказа не пересечена.  
8.  Поставка **C** закрыта (спрос больше не существует).  
9. Окончательная проверка: необработанных напоминаний об уровне запасов не существует.  

> [!NOTE]  
>  Шаг 4 демонстрирует поведение системы в версиях до Microsoft Dynamics NAV 2009 SP1.  

Это завершает описание основных принципов, связанных с планированием запасов на основе политик повторных заказов. В следующем разделе описываются характеристики четырех поддерживаемых политик повторного заказа.

## <a name="reordering-policies"></a>Политики дозаказа
Политики дозаказа определяют количество для заказа, если необходимо пополнить товар. Существует четыре различные политики дозаказа.  

### <a name="fixed-reorder-qty"></a>Фикс. кол-во повтора заказа
Политика фиксированного количества повторного заказа связана с планированием запасов стандартных С-элементов (низкая стоимость запасов, низкий риск устаревания и(или) много элементов). Эта политика обычно используется в связи с точкой повторного заказа, отражая прогнозируемый спрос во время подготовки товара.  

#### <a name="calculated-per-time-bucket"></a>Расчет на горизонт планирования  
Если система планирования обнаруживает, что точка дозаказа достигнута или пройдена в данном горизонте планирования (цикл дозаказа) — количество больше или равно точке дозаказа в начале периода и ниже или равно точке дозаказа в конце периода — она предлагает создать новый заказ на поставку с определенным количеством дозаказа и запланировать его на первую дату после последней даты горизонта планирования.  

Понятие точки повторного заказа в периоде времени уменьшает число предложений поставки. Это отражает ручной процесс периодического обхода склада с целью проверить фактическое содержимое различных ячеек.  

#### <a name="creates-only-necessary-supply"></a>Создание только необходимой поставки  
Перед тем как предложить новый заказ на поставку для соответствия точке дозаказа, система планирования проверяет, была ли уже заказана поставка для получения во время подготовки товара. Если существующий заказ на поставку разрешит проблему, увеличив или уменьшив прогнозируемые запасы по отношению к точке дозаказа в течение времени подготовки, система не предложит новый заказ на поставку.  

Заказы на поставку, созданные специально для соответствия точке дозаказа, исключаются из обычной балансировки поставки и ни при каких обстоятельствах не изменятся в будущем. Следовательно, при отмене (непополнении) товара, использующего точку дозаказа, рекомендуется просмотреть незавершенные заказы на поставку вручную или изменить политику дозаказа на "Партия на партию", в соответствии с чем система уменьшит или отменит излишнюю поставку.  

#### <a name="combines-with-order-modifiers"></a>Объединение с модификаторами заказа  
Модификаторы заказов, минимальное кол-во заказа, максимальное кол-во заказа и задать несколько, не должны играть существенной роли при использовании политики фиксированного количества для повторного заказа. Однако система планирования примет в расчет эти модификаторы и уменьшит количество до указанного максимального количества заказа (и создаст две или более поставки для достижения общего количества заказа), увеличит заказ до указанного минимального количества заказа или округлит количество заказа для соответствия указанному множителю заказа.  

#### <a name="combines-with-calendars"></a>Объединение с календарями  
Перед тем как предложить новый заказ на поставку для соответствия точке дозаказа, система планирования проверяет, запланирован ли заказ на нерабочий день, согласно всем календарям, определенным в поле **Код базового календаря** на страницах **Информация об организации** и **Карточка склада**.  

Если плановая дата является нерабочим днем, система планирования переместит заказ до ближайшей рабочей даты. Это может привести к тому, что заказ достигнет точки повтора заказа, но не удовлетворит определенному спросу. Если такого несбалансированного спроса система планирования создает дополнительную поставку.  

#### <a name="should-not-be-used-with-forecast"></a>Не для использования с прогнозом  
Поскольку ожидаемый спрос уже выражен на уровне точки дозаказа, не обязательно включать прогноз в планирование товара с использованием точки дозаказа. Если политика "Партия на партию" имеет отношение к созданию плана на основе прогноза, используйте ее.  

#### <a name="must-not-be-used-with-reservations"></a>Не для использования с резервированиями  
Если пользователь резервировал количество, например количество в запасах, для некоторого отдаленного спроса, основа планирования будет нарушена. Даже если прогнозируемый уровень запасов является приемлемым в отношении точки дозаказа, количества могут быть недоступны. Система может компенсировать это, создав исключительные заказы; однако рекомендуется задать в поле "Резервирование" значение "Никогда" для товаров, спланированных с использованием точки повторного заказа.

### <a name="maximum-qty"></a>Максимальное кол-во
Политика максимального количества — это способ ведения запасов с использованием точки повтора заказа.  

Все, что имеет отношение к политике "Фикс. кол-во дозаказа", также применяется к этой политике. Единственное отличие — в количестве предлагаемой поставки. При использовании политики максимального количества, количество повторного заказа определяется динамически с учетом прогнозируемого уровня запасов. Как правило, от заказа к заказу это количество различается.  

#### <a name="calculated-per-time-bucket"></a>Расчет на горизонт планирования  
Количество повторного заказа определяется в момент времени (в конце горизонта планирования), когда система планирования обнаружит, что точка повторного заказа пройдена. В этот момент система измеряет разницу между текущим прогнозируемым уровнем запасов и указанным максимальным запасом. Этот представляет количество, которое подлежит дозаказу. Система затем проверяет, была ли поставка заказана где-либо еще для получения в течение времени подготовки и если да, то уменьшает количество нового заказа на поставку на уже заказанное количество.  

Система обеспечит, что планированные запасы хотя бы достигнут точки повторного заказа на случай, если пользователь забудет указать максимальное количество запасов.  

#### <a name="combines-with-order-modifiers"></a>Объединение с модификаторами заказа  
В зависимости от настройки может иметь смысл объединить политику максимального количества с модификаторами заказов для обеспечения минимального количества заказа, его округления до целого числа единиц измерения покупки или разделения на несколько партий в соответствии с максимальным количеством заказа.  

### <a name="combines-with-calendars"></a>Объединение с календарями  
Перед тем как предложить новый заказ на поставку для соответствия точке дозаказа, система планирования проверяет, запланирован ли заказ на нерабочий день, согласно всем календарям, определенным в поле **Код базового календаря** на страницах **Информация об организации** и **Карточка склада**.  

Если плановая дата является нерабочим днем, система планирования переместит заказ до ближайшей рабочей даты. Это может привести к тому, что заказ достигнет точки повтора заказа, но не удовлетворит определенному спросу. Если такого несбалансированного спроса система планирования создает дополнительную поставку.

### <a name="order"></a>Порядок
В среде изготовления продукции на заказ товар приобретается или производится исключительно для удовлетворения определенного спроса. Как правило, это относится к товарам категории А. Мотивация для выбора такой политики повторного заказа — нерегулярный спрос, незначительное время подготовки или варьирование необходимых атрибутов.  

Приложение создает ссылку от заказа к заказу, которая действует как предварительная связь между поставкой, заказом на поставку или запасом и спросом, который будет удовлетворен.  

Помимо использования политики "Заказ" связь "заказ-в-заказ" можно применить во время планирования одним из следующих способов:  

* При использовании политики производства на заказ для создания многоуровневых производственных заказов или заказов проектного типа (производство необходимых компонентов в одном производственном заказе).  
* При использовании функции планирования заказов на продажу для создания производственного заказа из заказа на продажу.  

Даже если производственная организация считает себя организацией, которая изготавливает продукты на заказ, может иметь смысл использовать политику дозаказа "Партия на партию", если товары абсолютно стандартные без изменений атрибутов. В результате, система будет использовать незапланированный запас и накапливать только заказы на продажу с одинаковой датой отгрузки или заказы на продажу в пределах указанного горизонта планирования.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Связи "заказ-в-заказ" и просроченные даты  
В отличие от большинства наборов спрос-предложение, связанные заказы с датами оплаты до даты начала планирования полностью планируются системой. Коммерческое обоснование этого исключения следующее: конкретные наборы спроса и предложения должны синхронизироваться вплоть до самого исполнения. Дополнительные сведения о замороженной зоне, применяемой к большинству типов поставки и требования, см. в разделе [Обработка заказов до даты начала планирования](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Партия на партию
Политика работы с индивидуальными партиями является наиболее гибкой, потому что система реагирует только на фактический спрос, а также на предполагаемый спрос прогнозируемых и общих заказов, а затем сопоставляет количество заказа с учетом спроса. Политика обработки отдельных партий ориентирована на товары категории А и В, где запасы могут быть приняты, однако этого следует избегать.  

В некоторой степени политика "Партия на партию" похожа на политику "Заказ", но имеет общий подход к товарам. В соответствии с ней можно принимать количества в запасах и связывать спрос с соответствующей поставкой в горизонтах планирования, определенных пользователем.  

Горизонт планирования определяется в поле **Горизонт планирования**. Система работает с минимальным горизонтом планирования 1 день, поскольку это минимальная единица измерения событий спроса и предложения в системе (хотя на практике единица измерения производственных заказов и потребности в компонентах может измеряться в секундах).  

Горизонт планирования также устанавливает лимиты перепланирования существующего заказа на поставку с целью удовлетворения имеющегося требования. Если поставка находится в пределах горизонта планирования, она будет перепланирована на более раннюю или позднюю дату, чтобы удовлетворить спрос. В противном, если поставка находится до горизонта планирования, это приведет к ненужному накоплению запасов, и такую поставку следует отменить. В противном случае будет создан новый заказ на поставку.  

С этой политикой можно также определить страховой запас, чтобы компенсировать возможные колебания в поставках или удовлетворить неожиданный спрос.  

Поскольку количество заказа на поставку основывается на фактическом спросе, может иметь смысл использовать модификаторы заказов: округление количества заказа с учетом указанного множителя заказа (или единицы измерения покупки), увеличение количества заказа до определенного минимального значения или уменьшение количества до определенного максимального значения (при этом создается две или больше поставок для достижения необходимого количества).

## <a name="see-also"></a>См. также  
[Сведения о проектировании: параметры планирования](design-details-planning-parameters.md)   
[Сведения о проектировании: таблица "Назначение произ. плана"](design-details-planning-assignment-table.md)   
[Сведения о проектировании: основные понятия системы планирования](design-details-central-concepts-of-the-planning-system.md)   
[Сведения о проектировании: балансировка спроса и поставки](design-details-balancing-demand-and-supply.md)   
[Сведения о проектировании: планирование поставок](design-details-supply-planning.md)
