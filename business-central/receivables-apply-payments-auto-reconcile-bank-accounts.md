---
title: Выверка банковских счетов и применение платежей | Документация Майкрософт
description: Описываются задачи по выверке банковских счетов, счетов расчетов с клиентами и поставщиками, учету приходных кассовых поступлений и расходов и автоматическому применению платежей.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2eb195d194ae2091a10f2d85d1b802577239b268
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781464"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Автоматическое применение платежей и выверка банковских счетов
Следует регулярно выверять банковский, дебетовый и кредитовый счета путем применения платежей, зарегистрированных на банковском счете, к связанным открытым (неоплаченным) счетам и кредит-нотам либо к другим открытым операциям в [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Эту задачу можно выполнить на странице **Журнал выверки платежей**, например, импортировав файл банковской выписки для быстрой регистрации платежей. Платежи применяются к открытым операциям книги поставщиков или клиентов на основании совпадений текста платежа и информации операции. В можете просматривать и изменять автоматические применения перед учетом журнала. Вы можете закрыть любую открытую операцию книги банковских счетов, связанную с примененными операциями книги, при учете журнала. Банковский счет автоматически выверяется после применения всех платежей.

Логика, которая определяет, как текст платежа автоматически сопоставляется с информацией о записи, настраивается на странице **Правила применения платежей** в виде набора приоритизированных правил, которые вы можете редактировать.

Также можно производить выверку банковских счетов без одновременного применения платежей. Эта работа выполняется на странице **Выверка банковского счета**. Дополнительные сведения см. в разделе [Выверка банковских счетов](bank-how-reconcile-bank-accounts-separately.md).   

Чтобы импортировать банковские выписки в электронном виде, необходимо сначала настроить и включить службу банковских выписок Envestnet Yodlee, а затем связать свои банковские счета с соответствующими счетами интернет-банка. Дополнительные сведения см. в разделе [Настройка службы Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

Кроме того, можно воспользоваться расширением AMC Banking 365 Fundamentals, чтобы преобразовать файл банковской выписки в любом формате в поток данных для импорта в [!INCLUDE[d365fin](includes/d365fin_md.md)]. Дополнительные сведения см. в разделе [Использование расширения AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.  

| Действие | Ссылка |
| --- | --- |
| Применение платежей к открытым операциям книги клиентов и поставщиков путем импорта банковской выписки и выверка банковского счета, когда все платежи применены. |[Выверка платежей с использованием автоматического применения](receivables-how-reconcile-payments-auto-application.md) |
| Применение платежей вручную путем просмотра подробны сведений о сопоставленных данных и предложениях для открытых операций кандидатов, к которым применяется платеж. |[Проверка или применение платежей после автоматического применения](receivables-how-review-apply-payments-auto-application.md) |
| Разрешение платежей, которые не могут быть применены автоматически к соответствующим открытым операциям книг. Например, из-за расхождений в суммах или отсутствия соответствующих операций в книгах. |[Выверка платежей, которые не могут быть применены автоматически](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Свяжите текст платежей с конкретным счетом клиента, поставщика или счетом ГК, чтобы всегда учитывать типовые приходные кассовые ордеры или расходы на этих счетах, когда нет документов, к которым их можно было бы применить. |[Сопоставление текста на типовых платежах со счетами для автоматической выверки](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Настройте правила, определяющие, как платежи/банковские транзации должны автоматически применяться к соответствующим открытым операциям книг при использовании функции **Применить автоматически** на странице **Журнал выверки платежей**.|[Настройка правил для автоматического применения платежей](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>См. соответствующее обучение на странице [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>См. также
[Выверка банковских счетов](bank-how-reconcile-bank-accounts-separately.md)  
[Управление дебиторской задолженностью](receivables-manage-receivables.md)  
[Продажи](sales-manage-sales.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
