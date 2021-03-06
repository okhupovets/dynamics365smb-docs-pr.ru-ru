---
title: Пошаговое руководство. Настройка и выставление счетов на продажу | Документация Майкрософт
description: Предоплата — это платежи, для которых выставление счетов и учет в заказах на предоплату при продажах или покупках осуществляется до окончательного выставления счетов. Например, можно потребовать задаток перед производством товара по заказу или платеж перед отгрузкой товаров клиенту. Благодаря функции предоплаты можно выставлять счета в Business Central и собирать необходимые авансы от клиентов либо переводить авансы поставщикам. Таким образом, можно гарантировать учет всех платежей по счету.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: c24fe7eea180b008401f58a401f0e74de2981086
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786675"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Пошаговое руководство. Настройка и выставление счетов на продажу

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Предоплата — это платежи, для которых выставление счетов и учет в заказах на предоплату при продажах или покупках осуществляется до окончательного выставления счетов. Например, можно потребовать задаток перед производством товара по заказу или платеж перед отгрузкой товаров клиенту. Благодаря функции предоплаты можно выставлять счета в [!INCLUDE[d365fin](includes/d365fin_md.md)] и собирать необходимые авансы от клиентов либо переводить авансы поставщикам. Таким образом, можно гарантировать учет всех платежей по счету.  

 Необходимость предоплаты можно определить для клиента или поставщика для всех или выбранных товаров. После завершения необходимой настройки можно сгенерировать счета на предоплату на основе заказов на продажу или покупку для вычисленных сумм предоплаты. При необходимости суммы по умолчанию в счете можно изменить. Например, можно также отправить дополнительные счета на предоплату, если в заказ были добавлены дополнительные товары.  

## <a name="about-this-walkthrough"></a>Об этом пошаговом руководстве  
 В этом пошаговом руководстве описана поэтапная реализация следующих сценариев:  

-   настройка предоплаты;  
-   создание заказа, требующего предоплаты;  
-   создание счета на предоплату;  
-   исправление требований по предоплате для заказа;  
-   применение предоплаты к заказу;  
-   выставление счета на окончательную сумму по заказу с предоплатой.  

### <a name="roles"></a>Роли  
 В этом пошаговом руководстве описываются задачи для следующих ролей:  

-   главный бухгалтер (Фаина);  
-   обработчик заказов (Светлана);  
-   администратор дебиторской задолженности (Артем).  

## <a name="story"></a>Сюжет  
 Фаина - главный бухгалтер. Она принимает решения относительно того, кто из клиентов должен платить задаток перед началом производства или отгрузки товара. Фаина настраивает [!INCLUDE[d365fin](includes/d365fin_md.md)] для автоматического вычисления предоплаты.  

 Светлана обработчик заказов на продажу. Когда клиент обращается, чтобы сделать заказ, она вводит его в систему в процессе разговора с клиентом по телефону. Таким образом, она может сразу же уточнить у клиента цены и условия оплаты, внося корректировки в заказ во время переговоров с клиентом.  

 Артем работает в отделе дебиторской задолженности, в котором он занимается учетом счетов и платежей.  

 В этом сценарии Фаина настраивает требования по предоплате для клиента «Нефтераз», исходя из его кредитной истории, и дает Светлане указания относительно обработки его заказов.  

 Когда звонит клиент, Светлана обсуждает с ним условия до тех пор, пока не будет достигнута договоренность. Затем она может вычислить предоплату множеством различных способов.  

 После того как Светлана отправляет счет на предоплату, клиент заказывает дополнительный товар. Светлана обновляет заказ и создает второй счет на предоплату.  

 Артем регистрирует платеж клиента и применяет его к счетам, а затем отправляет окончательный счет.  

## <a name="setting-up-prepayments"></a>Настройка предоплаты  
 Фаина настраивает систему для обработки предоплаты для клиентов.  

-   Фаина решает, что для предоплаты будет использоваться та же серия номеров, что и для выставления счетов продажи.  
-   Фаина указывает, что приложение должно проверять обязательность предоплаты перед выставлением окончательного счета по заказу.  
-   Фаина задает значения по умолчанию для обязательного процента предоплаты для определенных товаров и клиентов.  

В следующих процедурах описано выполнение задач Фаины:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Процедура настройки серии номеров для предоплаты  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка модуля "Продажи и дебитор. задолж."**, затем выберите соответствующую ссылку.  
2.  На странице **Настройка модуля продаж** раскройте экспресс-вкладку **Нумерация**.  
3.  Убедитесь, что серия номеров для учтенных счетов на предоплату в поле **Серия номеров учт. счетов предопл.** совпадает с серией номеров для учтенных счетов продажи (**Серия номеров учт. счетов**), а серия номеров учтенных кредит-нот предоплаты (**Серия номеров учт. кр.-нот предопл.**) совпадает с серией номеров для учтенных кредит-нот (**Серия номеров учт. кредит-нот**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Блокировка отгрузок при отсутствии предоплаты  
1.  На странице **Настройка модуля продаж** на экспресс-вкладке **Общее** установите флажок **Проверять предоплату при учете**.

    Теперь отгрузка заказа или выставление счета по нему невозможны, если сумма предоплаты по заказу не оплачена.  

Фаина требует, чтобы клиенту 20000 по умолчанию счета выставлялись при 30%-ом первом взносе по всем заказам. Поэтому она введет процент предоплаты по умолчанию в карточке клиента.  

Фаина требует, чтобы всем клиентам при покупке товара 1100 выставлялся счет на предоплату в размере 20 %. У клиента 20000 плохая кредитная история. Следовательно для этого клиента она требует 40% предоплаты по товару 20000 от клиента 1100. В следующей процедуре демонстрируется настройка процентов предоплаты по умолчанию.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Процедура назначения процента предоплаты по умолчанию клиентам и товарам  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Клиенты**, затем выберите соответствующую ссылку.  
2.  Откройте карточку для клиента 20000 (Нефтегаз).
3.  В поле **Предоплата (%)** введите **30**.  
4.  Нажмите кнопку **ОК**, чтобы закрыть карточку клиента.  
5.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Товары**, затем выберите соответствующую ссылку.  
6.  Откройте карточку для клиента 1100.
7.  Выберите действие **Проценты предоплаты**.  
8.  Заполните две строки на странице **Проценты предоплаты при продаже**, как указано ниже.  

    |**Тип продажи**|**Код продажи**|**Код товара**|**Предоплата (%)**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Клиент**|**20000**|**1100**|**40**|  
    |**Все клиенты**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  В зависимости от страны/региона, необходимо также указать код налоговой группы на экспресс-вкладке **Счет** для товаров 1000 и 1100.  

9. Закройте все страницы.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Определение счета для авансов при общей настройке учета  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Общая настройка учета**, затем выберите соответствующую ссылку.  
2.  Выберите строку, для которой в поле **Общая бизнес-группа** установлено значение **ЭКСПОРТ**, а в поле **Общая товарная группа** установлено значение **РОЗНИЦА**, затем выберите действие **Правка**.  
3.  На странице **Карточка общей настройки учета** в поле **Счет предоплат при продаже** укажите требуемый счет.  
4.  Нажмите кнопку **ОК**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Создание заказа, требующего предоплаты  
 В следующем сценарии Светлана, обработчик заказов, создает заказ во время разговора с клиентом. Товары, которые заказывает клиент, требуют предоплаты, а клиент просрочил несколько платежей в прошлом. Поэтому Светлана получила указание требовать фиксированную сумму в размере 2000 в качестве предоплаты по заказу.  

Запросы клиента, по которым можно оплатить 35%, с чем Светлана может согласиться. Как следствие, она меняет заказ.  

Светлана создает счет на предоплату и отправляет его клиенту.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Процедура создания заказа на продажу с предоплатой  
1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на продажу**, затем выберите соответствующую ссылку.  
2.  Выберите действие **Создать**.  
3.  В поле **Код клиента (покупателя)** выберите **20000**.  
5.  Примите отобразившееся предупреждение о просроченной задолженности.  
6.  Заполните две строки продаж следующими сведениями.  

    |**Тип**|**Номер**|**Количество**|  
    |--------------|-------------|------------------|  
    |**Товар**|**1000**|**1**|  
    |**Товар**|**1100**|**1**|

    По умолчанию поле предоплаты в строке продаж скрыто, поэтому необходимо включить его отображение.  

7. Убедитесь, что поле **Предоплата (%)** в строке с товаром **1000** содержит значение **30**. Это значение по умолчанию было взято из заголовка продажи, который был заполнен на основе карточки клиента.  

    Поле **Предоплата (%)** в строке с товаром **1100** содержит значение **40**. Это процент, введенный на странице **Проценты предоплаты при продаже** для товара **1100** и клиента **20000**.  

    Дополнительные сведения см. в разделе [Настройка предоплат](finance-set-up-prepayments.md).  
8. Выберите действие **Статистика**.  
9. На экспресс-вкладке **Предоплата** поле **Сумма в строке предоплаты без НДС** имеет значение **1.560**. При создании счета на предоплату для немедленного заказа эта сумма отображается в счете.  

    В этом сценарии Светлана получила указание предложить общую предоплату по заказу в размере 2 000.  

    > [!IMPORTANT]  
    >  В зависимости от страны/региона, следующий шаг может не применяться.  
10. Измените сумму в поле **Сумма в строке предоплаты без НДС** на **2000** и закройте страницу.  
11. Проверьте поле **Предоплата (%)** в строках продажи. Значение этого поля было пересчитано и теперь оно равно **40,81625**.  

    Пересчет выполняется для всех строк, у которых процент предоплаты больше 0.  

    Теперь клиент спрашивает, нельзя ли установить процент предоплаты на уровне 35 %. Контролер Светланы утверждает изменение.  

12. На странице **Заказ на продажу** в поле **Предоплата (%)** введите **35**.  
13. В отобразившемся окне предупреждения нажмите кнопку **Да**. Будет применена ставка 35% в качестве процента оплаты для всего заказа.  
14. Удостоверьтесь, что строки обновлены соответственно.  

## <a name="creating-a-prepayment-invoice"></a>Создание счета на предоплату  
После ввода правильных значений для предоплаты по заказу Светлана создает счет на предоплату и отправляет его клиенту.  

#### <a name="to-create-a-prepayment-invoice"></a>Процедура создания счета на предоплату  

1.  На странице **Заказ на продажу** выберите действие **Учет счета на предоплату**.  

> [!NOTE]  
>  Светлана выберет **Учет и печать счета на предоплату** и отправит клиенту счет по почте.  

## <a name="creating-an-additional-prepayment-invoice"></a>Создание дополнительного счета на предоплату  
На следующий день клиент звонит Светлане и вносит изменения в заказ. Он хотел бы получить две единицы товара 1100. Светлана открывает заказ повторно и обновляет в нем данные, а затем создает второй счет на предоплату по заказу и отправляет его клиенту.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Процедура создания дополнительного счета на предоплату  

1.  На странице **Заказ на продажу** выберите действие **Открыть повторно**.  
2.  В строке для товара **1100** введите в поле **Кол-во** значение **2**.  

    Перейдите к полям предоплаты. Теперь поле **Сумма в строке предоплаты без НДС** содержит **630**, а поле **Сумм. предопл. для выст. счета без НДС** содержит **315**. Это показывает, что есть дополнительная сумма предоплаты, которая еще не была включена в счет.  
3.  Чтобы учесть счет для дополнительной суммы предоплаты, выберите действие **Учет счета на предоплату**.  

## <a name="applying-the-prepayments"></a>Применение предоплаты  
Клиент оплачивает сумму предоплаты, и Артем, работающий в бухгалтерии, регистрирует платеж и применяет его к счетам на предоплату.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Процедура применения платежа к счетам на предоплату  

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журналы приходных кассовых ордеров**, затем выберите соответствующую ссылку.  
2.  Заполните строку журнала продаж следующими сведениями.  

    |Имя поля|Введите|  
    |----------------|-----------|  
    |**Тип документа**|**Оплата**|  
    |**Тип счета**|**Клиент**|  
    |**Номер счета**|**20000**|  
3. Выберите действие **Применить операции**.  
4.  На странице **Применение операций клиента** выберите первый счет на предоплату, после чего выберите действие **Установить код применения**.  
5.  Повторите предыдущий шаг для второй предоплаты.  
6.  Нажмите кнопку **ОК**.  

    Теперь в поле суммы подставлено значение, равное общей сумме двух счетов на предоплату.  

7.  Выполните учет журнала.  

## <a name="invoicing-the-remaining-amount"></a>Выставление счета на сумму остатка  
Артему сообщили, что заказанные товары отгружены и заказ готов для выставления счета. Теперь ему нужно создать счет для заказа.  

#### <a name="to-invoice-the-remaining-amount"></a>Процедура выставления счета на сумму остатка  
1. Откройте заказ на продажу.  
2. Выберите действие **Отгрузить и учесть счет**, затем выберите кнопку **ОК**.  

> [!NOTE]  
>  Обычно отгрузку учитывает отдел отгрузки продукции.  

Артем может просмотреть историю, чтобы подтвердить, что счет продажи был создан как запланировано.  

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Учтенные счета продаж**, затем выберите соответствующую ссылку.  

## <a name="next-steps"></a>Дальнейшие шаги  
В этом пошаговом руководстве была описана поэтапная настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] для обработки предоплаты. Были настроены проценты предоплаты по умолчанию для клиентов и товаров и продемонстрирована возможность использования нескольких методов для вычисления предоплаты по заказу. Также была рассмотрена процедура назначения заказу одной общей суммы предоплаты и вычисление суммы предоплаты как процента от общей суммы заказа.  

Был размещен счет на предоплату, создан второй счет на предоплату при изменении заказа и размещен окончательный счет на оставшуюся сумму.  

Функциональные возможности для предоплаты в [!INCLUDE[d365fin](includes/d365fin_md.md)] упрощают настройку и обеспечивают выполнение правил в отношении предоплаты для клиентов и товаров, а также позволяют учитывать все платежи по счету.  

## <a name="see-also"></a>См. также  
[Выставление счетов на предоплату](finance-invoice-prepayments.md)  
[Финансы](finance.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Пошаговые описания бизнес-процессов](walkthrough-business-process-walkthroughs.md)
