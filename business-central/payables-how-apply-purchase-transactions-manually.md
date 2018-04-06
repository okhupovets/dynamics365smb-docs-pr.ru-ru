---
title: "Выверка платежей поставщикам вручную | Документы Майкрософт"
description: "Для обработки, сопоставления и выверки платежей клиентов и возмещений вручную вы применяете сумму к одной или нескольким открытым операциям поставщика."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f6b0ab4131f26a91953b28991276d3a19a8918ad
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-vendor-payments-manually"></a><span data-ttu-id="68378-103">Выверка платежей поставщикам вручную</span><span class="sxs-lookup"><span data-stu-id="68378-103">Reconcile Vendor Payments Manually</span></span>
<span data-ttu-id="68378-104">При отправке платежа или получении возмещения от поставщика требуется решить, следует ли применять эту оплату или возмещение к одной или нескольким открытым операциям.</span><span class="sxs-lookup"><span data-stu-id="68378-104">When you send a payment or receive a refund from a vendor, you must decide whether to apply the payment or refund to one or more open entries.</span></span> <span data-ttu-id="68378-105">Можно определить точную сумму, которую требуется применить, например к денежным поступлениям или возмещениям, и тем самым только частично применить операции книги поставщиков.</span><span class="sxs-lookup"><span data-stu-id="68378-105">You can specify the exact amount that you want to apply to the payment receipt or refund, and then only partially apply vendor ledger entries.</span></span> <span data-ttu-id="68378-106">Важно также применить все операции книги поставщиков, чтобы получить правильную статистику поставщика, а также выписки по счету и процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="68378-106">You must apply all vendor ledger entries to obtain correct vendor statistics and reports of the account statements and finance charges.</span></span>

> [!NOTE]  
>   <span data-ttu-id="68378-107">Поставщики иногда могут предоставлять возмещение оплаты, а не кредит-ноту для компенсации будущих счетов, особенно в случаях, когда возвращаются товары после их оплаты или переплаты по счету.</span><span class="sxs-lookup"><span data-stu-id="68378-107">Vendors may sometimes give a payment refund instead of a credit memo to offset against future invoices, especially when you return items that you have already paid for or when you have overpaid an invoice.</span></span>

<span data-ttu-id="68378-108">Операции книги поставщиков можно применять тремя различными способами:</span><span class="sxs-lookup"><span data-stu-id="68378-108">You can apply vendor ledger entries in three different ways:</span></span>

* <span data-ttu-id="68378-109">Вводя информацию в специальные окнах, например в окно **Журнал платежей** и в окно **Журнал выверки платежей**.</span><span class="sxs-lookup"><span data-stu-id="68378-109">By entering information in dedicated windows, such as the **Payment Journal** window and the **Payment Reconciliation Journal** window.</span></span>
* <span data-ttu-id="68378-110">Из документов кредит-нот покупки.</span><span class="sxs-lookup"><span data-stu-id="68378-110">From purchase credit memo documents.</span></span>
* <span data-ttu-id="68378-111">Из операций книги поставщиков после того как документы покупки будут учтены, но не применены.</span><span class="sxs-lookup"><span data-stu-id="68378-111">From vendor ledger entries after purchase documents are posted but not applied.</span></span>

> [!NOTE]  
>   <span data-ttu-id="68378-112">Если поле **Метод применения** в карточке поставщика содержит параметр **Применить к самым старым**, платежи будут автоматически применены к самой старой открытой кредитовой операции, если вы вручную не укажете операцию, к которой нужно применить платеж.</span><span class="sxs-lookup"><span data-stu-id="68378-112">If the **Application Method** field on the vendor card contains **Apply to Oldest**, then payments will automatically be applied to the oldest open credit entry if you do not manually specify which entry to apply to.</span></span> <span data-ttu-id="68378-113">Если в качестве метода применения для клиента выбрано **Вручную**, операции должны применяться вручную.</span><span class="sxs-lookup"><span data-stu-id="68378-113">If the application method for a customer is **Manual**, then you must apply entries manually.</span></span>

<span data-ttu-id="68378-114">Платежи поставщику можно применить вручную к соответствующим документам покупки при учете платежей в окне **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="68378-114">You can apply vendor payments manually to their related purchase documents when you post the payments in the **Payment Journal** window.</span></span> <span data-ttu-id="68378-115">Дополнительные сведения о заполнении журнала платежей см. в разделе [Осуществление платежей](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="68378-115">For information about filling the payment journal, see [Making Payments](payables-make-payments.md).</span></span>

<span data-ttu-id="68378-116">Кроме того, платежи поставщикам и платежи клиентов можно применять после того как платежи появятся в виде отрицательных банковских транзакций в банке.</span><span class="sxs-lookup"><span data-stu-id="68378-116">You can also apply vendor payments, and customer payments, after the payments appear as negative bank transactions in your bank.</span></span> <span data-ttu-id="68378-117">В окне **Журнал выверки платежей** можно воспользоваться функциями импорта банковской выписки, автоматического применения и выверки банковского счета.</span><span class="sxs-lookup"><span data-stu-id="68378-117">In the **Payment Reconciliation Journal** window, you can use functions for bank statement import, automatic application, and bank account reconciliation.</span></span> <span data-ttu-id="68378-118">Дополнительные сведения см. в разделе [Выверка платежей с использованием автоматического применения](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="68378-118">For more information, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a><span data-ttu-id="68378-119">Применение платежа к одной или нескольким операциям книги поставщиков</span><span class="sxs-lookup"><span data-stu-id="68378-119">To apply a payment to a single or multiple vendor ledger entries</span></span>
1. <span data-ttu-id="68378-120">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал платежей**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="68378-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="68378-121">В окне **Журнал платежей** в первой строке журнала укажите нужную информацию об операции платежа.</span><span class="sxs-lookup"><span data-stu-id="68378-121">In the **Payment Journal** window, on the first journal line, enter the relevant information about the payment entry.</span></span>
3. <span data-ttu-id="68378-122">Применение одной операции книги поставщиков:</span><span class="sxs-lookup"><span data-stu-id="68378-122">To apply a single vendor ledger entry:</span></span>
   1. <span data-ttu-id="68378-123">В поле **Примен. к док. - номер** выберите поле для открытия окна **Применить операции поставщика**.</span><span class="sxs-lookup"><span data-stu-id="68378-123">In the **Applies-to Doc. No.** field, choose the field to open the **Apply Vendor Entries** window.</span></span>
   2. <span data-ttu-id="68378-124">В окне **Применить операции поставщика** выберите операцию, к которой нужно применить платеж.</span><span class="sxs-lookup"><span data-stu-id="68378-124">In the **Apply Vendor Entries** window, select the entry to apply the payment to.</span></span>
   3. <span data-ttu-id="68378-125">В строке в поле **Сумма для применения** введите сумму, которую требуется применить к операции.</span><span class="sxs-lookup"><span data-stu-id="68378-125">On the line in the **Amount to Apply** field, enter the amount to apply to the entry.</span></span>
4. <span data-ttu-id="68378-126">Применение нескольких операций книги клиентов:</span><span class="sxs-lookup"><span data-stu-id="68378-126">Or, to apply multiple vendor ledger entries:</span></span>

   1. <span data-ttu-id="68378-127">Выберите действие **Применить операции**.</span><span class="sxs-lookup"><span data-stu-id="68378-127">Choose the **Apply Entries** action.</span></span>
   2. <span data-ttu-id="68378-128">В окне **Применение операций поставщика** выберите строки с операциями, к которым нужно применить оплату.</span><span class="sxs-lookup"><span data-stu-id="68378-128">In the **Apply Vendor Entries** window, select the lines with the entries to apply the payment to.</span></span>
   3. <span data-ttu-id="68378-129">Выберите действие **Установить код применения**.</span><span class="sxs-lookup"><span data-stu-id="68378-129">Choose the **Set Applies-to ID** action.</span></span>  
   4. <span data-ttu-id="68378-130">В каждой строке в поле **Сумма для применения** введите сумму, которую требуется применить к отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="68378-130">On each line in the **Amount to Apply** field, enter the amount to apply to the individual entry.</span></span>

      <span data-ttu-id="68378-131">Если сумма не введена, автоматически применяется максимальная сумма.</span><span class="sxs-lookup"><span data-stu-id="68378-131">If you do not enter an amount, then the maximum amount is automatically applied.</span></span> <span data-ttu-id="68378-132">В нижней части окна **Применить операции поставщика** можно увидеть конкретную сумму в поле "Примененная сумма", а также увидеть, является ли применение сбалансированным.</span><span class="sxs-lookup"><span data-stu-id="68378-132">At the bottom of the **Apply Vendor Entries** window, you can see the amount in the Applied Amount field, and you can see whether the application balances.</span></span>
5. <span data-ttu-id="68378-133">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68378-133">Choose the **OK** button.</span></span>
6. <span data-ttu-id="68378-134">Выберите действие **Учесть**, чтобы учесть журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="68378-134">Choose the **Post** action to post the payment journal.</span></span>

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a><span data-ttu-id="68378-135">Применение кредит-ноты к одной или нескольким операциям в книге поставщиков</span><span class="sxs-lookup"><span data-stu-id="68378-135">To apply a credit memo to a single or multiple vendor ledger entries</span></span>
1. <span data-ttu-id="68378-136">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Кредит-нота покупки**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="68378-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Credit Memo**, and then choose the related link.</span></span>
2. <span data-ttu-id="68378-137">Откройте кредит-ноту, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="68378-137">Open the credit memo that you want to apply.</span></span>
3. <span data-ttu-id="68378-138">Введите соответствующую информацию в заголовок.</span><span class="sxs-lookup"><span data-stu-id="68378-138">Enter the relevant information in the header.</span></span>
4. <span data-ttu-id="68378-139">Чтобы применить одну операцию в книге поставщика, на экспресс-вкладке **Применение** в поле **Примен. к док. - номер** выберите операцию, к которой требуется применить кредит, а затем, в поле **Сумма для применения**, введите сумму, которую требуется применить к этой операции.</span><span class="sxs-lookup"><span data-stu-id="68378-139">To apply a single vendor ledger entry, on the **Application** FastTab, in the **Applies-to Doc. No.** field, select the entry to apply the credit to, and then, in the **Amount to Apply** field, enter the amount to apply to the entry.</span></span>
5. <span data-ttu-id="68378-140">Применение нескольких операций книги клиентов:</span><span class="sxs-lookup"><span data-stu-id="68378-140">Or, to apply multiple vendor ledger entries:</span></span>

   1. <span data-ttu-id="68378-141">Выберите действие **Применить операции**.</span><span class="sxs-lookup"><span data-stu-id="68378-141">Choose the **Apply Entries** action.</span></span>
   2. <span data-ttu-id="68378-142">Выберите строки с записями, к которым нужно применить кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="68378-142">Select the lines with the entries to apply the credit memo to.</span></span>
   3. <span data-ttu-id="68378-143">Выберите действие **Установить код применения**.</span><span class="sxs-lookup"><span data-stu-id="68378-143">Choose the **Set Applies-to ID** action.</span></span>  
   4. <span data-ttu-id="68378-144">В каждой строке в поле **Сумма для применения** введите сумму, которую требуется применить к отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="68378-144">On each line in the **Amount to Apply** field, enter the amount to apply to the individual entry.</span></span>

       <span data-ttu-id="68378-145">Если сумма не введена, автоматически применяется максимальная сумма.</span><span class="sxs-lookup"><span data-stu-id="68378-145">If you do not enter an amount, then the maximum amount is automatically applied.</span></span> <span data-ttu-id="68378-146">В нижней части окна **Применить операции поставщика** можно увидеть конкретную сумму в поле **Примененная сумма**, а также увидеть, является ли применение сбалансированным.</span><span class="sxs-lookup"><span data-stu-id="68378-146">At the bottom of the **Apply Vendor Entries** window, you can see the amount in the **Applied Amount** field, and you can see whether the application balances.</span></span>
6. <span data-ttu-id="68378-147">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68378-147">Choose the **OK** button.</span></span>  
   <span data-ttu-id="68378-148">В окне **Кредит-нота покупки** теперь операция, выбранная в полях **Примен. к док. - тип** и **Примен. к док. - номер**.</span><span class="sxs-lookup"><span data-stu-id="68378-148">The **Purchase Credit Memo** window shows the entry that you have selected in the **Applies-to Doc. Type** field and the **Applies-to Doc. No.** field.</span></span> <span data-ttu-id="68378-149">В окне также отображается сумма учитываемой кредит-ноты, скорректированная для любых скидок оплаты.</span><span class="sxs-lookup"><span data-stu-id="68378-149">The window also shows the amount of the credit memo to be posted, adjusted for any payment discounts.</span></span>
7. <span data-ttu-id="68378-150">Нажмите кнопку **Учесть**, чтобы учесть кредит-ноту покупки.</span><span class="sxs-lookup"><span data-stu-id="68378-150">Choose the **Post** button to post the purchase credit memo.</span></span>

## <a name="to-apply-posted-vendor-ledger-entries"></a><span data-ttu-id="68378-151">Применение учтенных операций книги поставщиков</span><span class="sxs-lookup"><span data-stu-id="68378-151">To apply posted vendor ledger entries</span></span>
1. <span data-ttu-id="68378-152">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Поставщики**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="68378-152">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="68378-153">Откройте соответствующего поставщика с уже учтенными операциями.</span><span class="sxs-lookup"><span data-stu-id="68378-153">Open the relevant vendor with entries that have already been posted.</span></span>
3. <span data-ttu-id="68378-154">Выберите действие **Книга операций**, а затем выберите действие **Применить операции**.</span><span class="sxs-lookup"><span data-stu-id="68378-154">Choose the **Ledger Entries** action, and then choose the **Apply Entries** action.</span></span>
4. <span data-ttu-id="68378-155">В окне **Применить операции поставщика** можно видеть открытые операции для поставщика.</span><span class="sxs-lookup"><span data-stu-id="68378-155">In the **Apply Vendor Entries** window, you can see the open entries for the vendor.</span></span>
5. <span data-ttu-id="68378-156">Выберите строку с применяемой операцией.</span><span class="sxs-lookup"><span data-stu-id="68378-156">Select the line with the entry that will be applied.</span></span>
6. <span data-ttu-id="68378-157">Выберите действие **Установить код применения**.</span><span class="sxs-lookup"><span data-stu-id="68378-157">Choose the **Set Applies-to ID** action.</span></span>

    <span data-ttu-id="68378-158">Поле **Код применения** содержит три звездочки, если используется система с одним пользователем, или код пользователя, если используется система с несколькими пользователям.</span><span class="sxs-lookup"><span data-stu-id="68378-158">The **Applies-to ID** field displays three asterisks if you work in a single-user system or your user ID if you work in a multiuser system.</span></span>  
7. <span data-ttu-id="68378-159">В каждой строке в поле **Сумма для применения** введите сумму, которую требуется применить к отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="68378-159">For each line in the **Amount to Apply** field, enter the amount to apply to the individual entry.</span></span>

    <span data-ttu-id="68378-160">Если сумма не введена, автоматически применяется максимальная сумма.</span><span class="sxs-lookup"><span data-stu-id="68378-160">If you do not enter an amount, then the maximum amount is automatically applied.</span></span> <span data-ttu-id="68378-161">В нижней части окна **Применить операции поставщика** можно увидеть сумму в поле **Примененная сумма** .</span><span class="sxs-lookup"><span data-stu-id="68378-161">You can see the amount in the **Applied Amount** field at the bottom of the **Apply Vendor Entries** window.</span></span>
8. <span data-ttu-id="68378-162">Выберите действие **Учет применения**.</span><span class="sxs-lookup"><span data-stu-id="68378-162">Choose the **Post Application** action.</span></span>  

    <span data-ttu-id="68378-163">Откроется окно **Учет применения** с номером документа применяемой операции и самой последней датой учета операции.</span><span class="sxs-lookup"><span data-stu-id="68378-163">The **Post Application** window opens with the document number of the applying entry and the posting date of the entry with the most recent posting date.</span></span>
9. <span data-ttu-id="68378-164">Нажмите кнопку **ОК** для учета применения.</span><span class="sxs-lookup"><span data-stu-id="68378-164">Choose the **OK** button to post the application.</span></span>

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a><span data-ttu-id="68378-165">Применение операций книги поставщиков в различных валютах друг к другу</span><span class="sxs-lookup"><span data-stu-id="68378-165">To apply vendor ledger entries in different currencies to one another</span></span>
<span data-ttu-id="68378-166">В случае, если покупка у поставщика была произведена в одной валюте, а оплата проходит в другой валюте, вы все равно можете применить счет к платежу.</span><span class="sxs-lookup"><span data-stu-id="68378-166">If you buy from a vendor in one currency and make payment in another currency, you can still apply the invoice to the payment.</span></span>

<span data-ttu-id="68378-167">Если операция (Операция 1) в одной валюте применяется к операции (Операция 2) в другой валюте, используется дата учета Операции 1 для поиска соответствующего обменного курса для преобразования сумм в Операции 2.</span><span class="sxs-lookup"><span data-stu-id="68378-167">If you apply an entry (Entry 1) in one currency to an entry (Entry 2) in a different currency, the posting date on Entry 1 is used to find the relevant exchange rate to convert amounts on Entry 2.</span></span> <span data-ttu-id="68378-168">Поиск соответствующих обменных курсов осуществляется в окне **Валютные курсы**.</span><span class="sxs-lookup"><span data-stu-id="68378-168">The relevant exchange rate is found in the **Currency Exchange Rates** window.</span></span> <span data-ttu-id="68378-169">В этом случае необходимо включить применения операций книги поставщиков в различных валютах.</span><span class="sxs-lookup"><span data-stu-id="68378-169">In that case, you must enable application of vendor ledger entries in different currencies.</span></span> <span data-ttu-id="68378-170">Дополнительные сведения см. в разделе [Включение операций книги в разных валютах](finance-how-enable-application-ledger-entries-different-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="68378-170">For more information, see [Enable Application of Ledger Entries in Different Currencies](finance-how-enable-application-ledger-entries-different-currencies.md)</span></span>

1. <span data-ttu-id="68378-171">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал платежей**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="68378-171">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="68378-172">Откройте необходимый журнал и заполните первую пустую строку журнала, используя код валюты.</span><span class="sxs-lookup"><span data-stu-id="68378-172">Open the journal you want, and fill in the first empty journal line using a currency code.</span></span>
3. <span data-ttu-id="68378-173">Выберите действие **Применить операции**.</span><span class="sxs-lookup"><span data-stu-id="68378-173">Choose the **Apply Entries** action.</span></span>
4. <span data-ttu-id="68378-174">Выберите строку с операцией, которую требуется применить к операции в журнале платежей, выберите действие **Установить код применения**, а затем выберите операцию, к которой требуется применить платеж.</span><span class="sxs-lookup"><span data-stu-id="68378-174">Select the line with the entry you want to apply to the entry in the payment journal, choose the **Set Applies-to ID** action, and then select the entry you want to apply to.</span></span>
5. <span data-ttu-id="68378-175">Нажмите кнопку **ОК** для возвращения в журнал оплаты поставщикам.</span><span class="sxs-lookup"><span data-stu-id="68378-175">Choose the **OK** button to return to the payment journal.</span></span>
6. <span data-ttu-id="68378-176">Учет журнала оплат.</span><span class="sxs-lookup"><span data-stu-id="68378-176">Post the payment journal.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="68378-177">Если операции в разных валютах применяются друг к другу, эти операции преобразуются в рубли.</span><span class="sxs-lookup"><span data-stu-id="68378-177">When you apply entries in different currencies to one another, the entries are converted to USD.</span></span> <span data-ttu-id="68378-178">Даже в том случае, когда курсы обмена для соответствующих валют фиксированы, например, между немецкой маркой и евро, при преобразовании этих иностранных валют в рубли возможно появление небольшой остаточной суммы.</span><span class="sxs-lookup"><span data-stu-id="68378-178">Even though the exchange rates for the two relevant currencies are fixed, for example between USD and EUR, there may be a small residual amount when these foreign-currency amounts are converted to USD.</span></span> <span data-ttu-id="68378-179">Эти суммы остатка учитываются как прибыль и убыток на счет, указанный в поле **Счет реализованной прибыли** или **Счет реализованного убытка** в окне **Валюты**.</span><span class="sxs-lookup"><span data-stu-id="68378-179">These small residual amounts are posted as gains and losses to the account specified in the **Realized Gains Account** or **Realized Losses Account** field in the **Currencies** window.</span></span> <span data-ttu-id="68378-180">Поле **Сумма (руб.)** также корректируется по соответствующим операциям книги поставщиков.</span><span class="sxs-lookup"><span data-stu-id="68378-180">The **Amount (USD)** field is also adjusted on the relevant vendor ledger entries.</span></span>

## <a name="to-unapply-an-application-of-vendor-entries"></a><span data-ttu-id="68378-181">Отмена применения операций поставщика</span><span class="sxs-lookup"><span data-stu-id="68378-181">To unapply an application of vendor entries</span></span>
<span data-ttu-id="68378-182">При отмене ошибочного применения создаются и учитываются корректирующие операции, то есть операции, которые идентичны исходной операции, но с противоположным знаком в поле суммы, для всех операций, включая все операции учета в главной книге, связанные с данным применением, такие как скидка оплаты и прибыли или убытки от колебаний валютного курса.</span><span class="sxs-lookup"><span data-stu-id="68378-182">When you unapply an erroneous application, correcting entries that are identical to the original entry but with opposite sign in the amount field are created and posted for all entries, including all general ledger posting derived from the application, such as payment discount and currency gains/losses.</span></span> <span data-ttu-id="68378-183">Операции, которые были закрыты приложением, открываются повторно.</span><span class="sxs-lookup"><span data-stu-id="68378-183">The entries that were closed by the application are reopened.</span></span>

1. <span data-ttu-id="68378-184">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Поставщики**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="68378-184">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="68378-185">Откройте соответствующую карточку поставщика.</span><span class="sxs-lookup"><span data-stu-id="68378-185">Open the relevant vendor card.</span></span>
3. <span data-ttu-id="68378-186">Выберите действие **Книга операций**.</span><span class="sxs-lookup"><span data-stu-id="68378-186">Choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="68378-187">Выберите нужную операцию книги и выберите действие **Отменить применение операций**.</span><span class="sxs-lookup"><span data-stu-id="68378-187">Select the relevant ledger entry, and then choose the **Unapply Entries** action.</span></span>
5. <span data-ttu-id="68378-188">Альтернативный вариант — выберите действие **Подробные операции**.</span><span class="sxs-lookup"><span data-stu-id="68378-188">Alternatively, choose the **Detailed Ledger Entry** action.</span></span>
6. <span data-ttu-id="68378-189">Выберите операцию применения и выберите действие **Отменить применение операций**.</span><span class="sxs-lookup"><span data-stu-id="68378-189">Select the application entry, and then choose the **Unapply Entries** action.</span></span>
7. <span data-ttu-id="68378-190">Заполните поля в заголовке и выберите действие **Отменить применение**.</span><span class="sxs-lookup"><span data-stu-id="68378-190">Fill in the fields in the header, and then choose the **Unapply** action.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="68378-191">Если операция была применена в нескольких операциях применения, следует начать отмену с самой поздней операции применения.</span><span class="sxs-lookup"><span data-stu-id="68378-191">If an entry has been applied by more than one application entry, you must unapply the latest application entry first.</span></span>

## <a name="see-also"></a><span data-ttu-id="68378-192">См. также</span><span class="sxs-lookup"><span data-stu-id="68378-192">See Also</span></span>
[<span data-ttu-id="68378-193">Кредиторская задолженность</span><span class="sxs-lookup"><span data-stu-id="68378-193">Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="68378-194">Покупки</span><span class="sxs-lookup"><span data-stu-id="68378-194">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="68378-195">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="68378-195">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
