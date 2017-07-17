---
title: "Практическое руководство. Продажа продукции | Документы Майкрософт"
description: "Описывается использование заказов на продажу."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 03/09/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a587a9eab63223f7fab94bc4f513d2b6816f0d14
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-sell-products"></a>Практическое руководство. Продажа продукции
Счет продажи или заказ на продажу создаются для записи соглашения с клиентом о продаже определенных товаров на определенных условиях доставки и оплаты.

**Примечание**. Заказы на продажу следует использовать, если процесс продажи требует, чтобы вы могли отгружать части количества в заказе, например потому, что полное количество недоступно в конкретный момент. Если продажа товаров осуществляется путем непосредственной поставки от поставщика клиенту (прямая поставка), то также необходимо использовать заказы на продажу. Дополнительные сведения см. в разделе [Практическое руководство. Выполнение прямых поставок](sales-how-drop-shipment.md). Во всех других аспектах заказы на продажу аналогичны счетам продажи. Дополнительные сведения см. в разделе [Практическое руководство. Выставление счетов продажи](sales-how-invoice-sales.md).

Можно провести переговоры с клиентом, сначала создав предложение по продаже, которое можно преобразовать в заказ на продажу, когда вы договоритесь о продаже. Дополнительные сведения см. в разделе [Практическое руководство. Создание предложений](sales-how-make-offers.md).

После подтверждения соглашения клиентом, например после процесса предложения, можно отправить подтверждение заказа, чтобы зафиксировать обязательства по доставке продуктов в соответствии с договоренностью.

При поставке продуктов, полностью или частично, вы учитываете заказы на продажу как отгруженные или как отгруженные и с выставленными счетами для создания соответствующих операций книг товаров и клиентов в своей системе. При учете заказа на продажу вы также можете отправить документ по электронной почте в виде вложения PDF. Тело сообщения электронной почты можно заполнить краткой сводкой информации о заказе и платеже, например включить в него ссылку на PayPal. Дополнительные сведения см. в разделе [Практическое руководство. Отправка документов по электронной почте](ui-how-send-documents-email.md).

В бизнес-средах, в которых клиент должен осуществить платеж до доставки продуктов, например в розничной торговле, необходимо подождать получения платежа, прежде чем доставлять продукты. В большинстве случаев вы обрабатываете входящие платежи через несколько недель после отгрузки путем применения платежей к соответствующим учтенным неоплаченным счетам продажи. Дополнительные сведения см. в разделе [Практическое руководство. Выверка платежей с использованием автоматического применения](receivables-how-reconcile-payments-auto-application.md).

Вы можете легко исправить или отменить учтенный счет продажи, являющийся результатом заказа на продажу, до его оплаты. Это используется, если нужно исправить опечатку или клиент запрашивает изменение на раннем этапе обработки заказа. Дополнительные сведения см. в разделе [Практическое руководство. Исправление или отмена неоплаченных счетов продажи](sales-how-correct-cancel-sales-invoice.md). Если учтенный счет продажи оплачен, необходимо создать кредит-ноту продажи для сторнирования продажи. Дополнительные сведения см. в разделе [Практическое руководство. Обработка возвратов продажи или отмен](sales-how-process-sales-returns-cancellations.md)

Товары могут быть и товарами в запасах, и услугами, обозначенными типами **Товар - Запасы** и **Товар - Сервис** в строках продажи. Процедура обработки заказа на продажу такая же для обоих типов товаров. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых товаров](inventory-how-register-new-items.md).

Можно заполнить поля клиента в заказе на продажу двумя способами в зависимости от того, зарегистрирован ли уже клиент. См. шаги 2 и 3 в следующей процедуре.

## <a name="to-create-a-sales-order"></a>Создание заказа на продажу
1. На домашней странице выберите действие **Заказ на продажу**.  
2. В поле **Клиент** введите название существующего клиента.

    Остальные поля в окне **Заказ на продажу** заполнятся стандартными сведениями о выбранном клиенте. Если клиент не зарегистрирован, выполните следующие действия.
3. В поле **Клиент** введите название нового клиента.
4. В диалоговом окне регистрации нового клиента нажмите кнопку **Да**.
5. В окне **Выбор шаблона для нового клиента** выберите шаблон для создания новой карточки клиента и нажмите кнопку **ОК**.

    Откроется новая карточка клиента, предварительно заполненная сведениями из выбранного шаблона клиента. Поле **Название** предварительно заполняется названием нового клиента, введенным в заказ на продажу.
6. Перейдите к заполнению остальных полей в карточке клиента. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых клиентов](sales-how-register-new-customers.md).  
7. Заполнив карточку клиента, нажмите кнопку **ОК**, чтобы вернуться в окно **Заказ на продажу**.

    Несколько полей в заказе на продажу заполняются сведениями, указанными в новой карточке клиента.
8. Заполните остальные поля в окне **Заказ на продажу** по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Теперь вы готовы к заполнению строк заказа на продажу сведениями о товарах в запасах или услугах, которые вы хотите продать клиенту.

    Если заданы строки типовых продаж для клиента, например ежемесячный заказ пополнения заказов, можно вставить эти строки в заказ выбрав действие **Получить строки типовых продаж**.
9. На экспресс-вкладке **Строки** в поле **Товар** введите номер товара в запасах или услуги.  
10. В поле **Кол-во** укажите количество товаров, которые будут проданы.

    **Примечание**. Количество товаров типа "Услуга" измеряется в единицах времени, например часах, как указано в поле **Код единицы измерения** строки.

    Поле **Сумма строки** обновляется и отображает значение в поле **Цена единицы**, умноженное на значение в поле **Кол-во**.

    Значения цены и суммы строки отображаются с налогом или без него в зависимости от выбранного параметра в поле **Цены с учетом налога** на карточке клиента.
11. В поле **Скидка строки (%)** введите процентное значение, если требуется предоставить клиенту скидку на продукт. Значение в поле **Сумма строки** обновляется соответствующим образом.

    Если настроены специальные цены товара на экспресс-вкладке **Цены продажи и скидки по строкам продаж** в карточке клиента или товара, цена и сумма в строке предложения автоматически обновляются, если выполняются условия согласованных критериев цены. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).
12. Чтобы добавить комментарий о строке предложения, которую клиент может просмотреть в напечатанном предложении по продаже, текст в поле **Описание** нужно записать в пустой строке.  
13. Повторите шаги с 10 по 13 для каждого товара, который требуется предложить клиенту.

    Итоги под строками автоматически вычисляются по мере создания или изменения строк.
6. В новой карточке клиента отобразится информация из выбранного шаблона клиента. Заполните остальные поля. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация новых клиентов](sales-how-register-new-customers.md).  
7. Заполнив карточку клиента, нажмите кнопку **ОК**, чтобы вернуться в окно **Заказ на продажу**.

   Несколько полей в заказе на продажу заполняются сведениями, указанными в новой карточке клиента.  
8. Заполните остальные поля в окне **Заказ на продажу** по мере необходимости. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Теперь вы готовы заполнить строки заказа на продажу для продуктов, которые вы продаете клиенту, или для всех транзакций с клиентом, которые необходимо записать на счете ГК.   

   Если заданы строки типовых продаж для клиента, например ежемесячный заказ пополнения заказов, можно вставить эти строки в заказ выбрав действие **Получить строки типовых продаж**.  
9. На экспресс-вкладке **Строки** в поле **Тип** выберите тип продукта, издержки или транзакцию, которая будет учтена для клиента в строке продажи.
10. В поле **Номер** выберите запись для учета согласно значению в поле **Тип**.

    Поле **Номер** не заполняется в следующих случаях: -Если строка предназначена для комментариев. Напишите комментарий в поле **Описание**.
    -Если строка предназначена для нескладируемого товара. Выберите действие **Выбрать нескладируемые товары**. Дополнительные сведения см. в разделе [Практическое руководство. Работа с нескладируемыми товарами](inventory-how-work-nonstock-items.md).

11. В поле **Количество** укажите, сколько единиц продукта, издержек или транзакции будет регистрироваться в этой строке для клиента.  

    **Примечание.** Если товар принадлежит к типу **Товар - Сервис** или **Ресурс**, количество измеряется в единицах времени, например в часах, как указано в поле **Код единицы измерения** строки.  

    Значение в поле **Сумма строки** рассчитывается как *Цена единицы* х *Количество*.  

    Значения цены и суммы строки отображаются с налогом или без него в зависимости от выбранного параметра в поле **Цены с учетом налога** в карточке клиента.  
12. Если необходимо предоставлять скидку, введите процент в поле **Скидка строки (%)**. Значение в поле **Сумма строки** обновляется соответствующим образом.  

    Если настроены специальные цены товара на экспресс-вкладке **Цены продажи и скидки по строкам продаж** в карточке клиента или товара, цена и сумма в строке продажи автоматически обновляются, если выполняются условия критериев цены. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Повторите шаги с 9 по 12 для каждого продукта или издержки, которые требуется продать клиенту.  

    Итоги под строками автоматически вычисляются по мере создания или изменения строк.  
14. В поле **Сумма скидки по счету** введите сумму, которую нужно вычесть из значения, отображенного в поле **Всего с учетом налога**.

    Если установлены скидки по счету для клиента, то указанное значение процента автоматически вводится в поле **Скидка по счету, %**, если соблюдены условия, а связанная сумма вводится в поле **Сумма скидки по счету без налога**. Дополнительные сведения см. в разделе [Регистрация соглашений о цене продажи, скидках и платежах](sales-how-record-sales-price-discount-payment-agreements.md).
15. Для отгрузки только части количества заказа введите это количество в поле **Кол-во для отгрузки**. Значение копируется поля **Кол-во для выставления счета**.
16. Для выставления счета только на часть отгружаемого количества введите это количество в поле **Кол-во выставления счета**. Количество должно быть меньше значения в поле **Кол-во для отгрузки**.   
17. Когда строки заказа на продажу готовы, выберите действие **Учесть и отправить**.

В диалоговом окне **Учесть и отправить подтверждение** отобразится предпочтительный способ получения документов клиента. Можно изменить метод отправки, нажав кнопку поиска у поля **Кому отправить документ**. Дополнительные сведения см. в разделе [Практическое руководство. Настройка профилей отправки документов](sales-how-setup-document-send-profiles.md).

Связанные операции книги товаров и клиентов будут созданы в вашей системе, а заказ на продажу сформирован в виде PDF-документа. Когда заказ продажи будет полностью учтен, он будет удален из списка заказов на продажу и заменен новыми документами в списке учтенных счетов продажи и учтенных расходных накладных продажи.

## <a name="see-also"></a>См. также
[Продажи](sales-manage-sales.md)  
[Настройка продаж](sales-setup-sales.md)  
[Запасы](inventory-manage-inventory.md)  
[Практическое руководство. Отправка документов по электронной почте](ui-how-send-documents-email.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)