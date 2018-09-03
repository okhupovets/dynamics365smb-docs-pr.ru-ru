---
title: "Применение платежей к связанным документам и их учет | Microsoft Docs"
description: "Описывается процедура регистрации платежей в адрес поставщиков и возвратов в адрес клиентов."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: ru-ru
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a><span data-ttu-id="a0b92-103">Регистрация платежей и возвратов</span><span class="sxs-lookup"><span data-stu-id="a0b92-103">Record Payments and Refunds</span></span>
<span data-ttu-id="a0b92-104">В окне **Журнал платежей** производится регистрация платежей в адрес поставщиков и возвратов в адрес клиентов.</span><span class="sxs-lookup"><span data-stu-id="a0b92-104">In the **Payment Journal** window, you record payments that you make to vendors and refunds that you make to customers.</span></span> <span data-ttu-id="a0b92-105">При учете строки журнала платежей уплаченная сумма регистрируется на указанном банковском счете в системе.</span><span class="sxs-lookup"><span data-stu-id="a0b92-105">When you post a payment journal line, the paid amount is recorded on the specified system bank account.</span></span> <span data-ttu-id="a0b92-106">После этого необходимо предпринять действия для фактического перевода средств с соответствующего банковского счета.</span><span class="sxs-lookup"><span data-stu-id="a0b92-106">You must then take steps to perform the actual money transfer from the related bank account.</span></span>

<span data-ttu-id="a0b92-107">Если ввести в поле **Примен. к док. - номер** номер счета или кредит-ноты, по которым производится оплата или возврат, при учете журнала соответствующий документ помечается как оплаченный.</span><span class="sxs-lookup"><span data-stu-id="a0b92-107">If you fill in the **Applies-to Doc. No.** field with the invoice or credit memo that must be paid or refunded, then the document in question is set to paid when you post the journal.</span></span> <span data-ttu-id="a0b92-108">Это называется "применением".</span><span class="sxs-lookup"><span data-stu-id="a0b92-108">This is referred to as "applied".</span></span> <span data-ttu-id="a0b92-109">В качестве альтернативы применению во время учета платежей можно использовать окно **Применить операции поставщика** и **Применить операции клиента** после учета платежей.</span><span class="sxs-lookup"><span data-stu-id="a0b92-109">As an alternative to applying during payment posting, you can use the **Apply Vendor Entries** and **Apply Customer Entries** window after you have made the payment posting.</span></span> <span data-ttu-id="a0b92-110">Дополнительные сведения см., например, в разделе [Выверка платежей поставщикам вручную](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="a0b92-110">For more information, see, for example, [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>

<span data-ttu-id="a0b92-111">Функция **Предлож. оплаты поставщикам** может помочь вам автоматически заполнять строки журнала в соответствии с приоритетами поставщиков и сроками оплаты.</span><span class="sxs-lookup"><span data-stu-id="a0b92-111">The **Suggest Vendor Payments** function can help you fill payment journal lines automatically according to vendor prioritization and due dates.</span></span> <span data-ttu-id="a0b92-112">Дополнительные сведения см. в разделе [Предложение оплаты поставщикам](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="a0b92-112">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span> <span data-ttu-id="a0b92-113">При использовании этой функции **Примен. к док. - номер** всегда будет заполнено.</span><span class="sxs-lookup"><span data-stu-id="a0b92-113">With this function, the **Applies-to Doc. No.** field is always filled in.</span></span>

<span data-ttu-id="a0b92-114">Помимо регистрации факта совершения платежа вы можете использовать окно **Журнал платежей** для вывода платежей для дальнейшей обработки вашим банком.</span><span class="sxs-lookup"><span data-stu-id="a0b92-114">In addition to recording that the payment is made, you can also use the **Payment Journal** window to output the payment for further processing by your bank.</span></span> <span data-ttu-id="a0b92-115">Дополнительные сведения см. в разделах [Совершение платежей с помощью платежных документов](payables-how-work-checks.md) и [Совершение электронных платежей](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="a0b92-115">For more information, see [Make Check Payments](payables-how-work-checks.md) and [Make Electronic Payments](payables-how-export-payments-bank-file.md).</span></span>  

1. <span data-ttu-id="a0b92-116">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журналы платежей**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="a0b92-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0b92-117">Откройте раздел журнала, предназначенный для платежей.</span><span class="sxs-lookup"><span data-stu-id="a0b92-117">Open the journal batch that is dedicated to payments.</span></span>
3. <span data-ttu-id="a0b92-118">Если вы знаете, в чей адрес совершается оплата или возврат, заполните поля вручную.</span><span class="sxs-lookup"><span data-stu-id="a0b92-118">If you know who to pay or refund, fill in the fields manually.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="a0b92-119">Чтобы одновременно применить платеж к соответствующему счету или кредит-ноте, выберите поле **Примен. к док. - номер**,</span><span class="sxs-lookup"><span data-stu-id="a0b92-119">To also apply the payment to the related invoice or credit memo, choose the **Applies-to Doc No.**</span></span> <span data-ttu-id="a0b92-120">в окне **Применить операции поставщика** выберите соответствующий счет или кредит-ноту, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0b92-120">field, in the **Apply Vendor Entries** window, select the relevant invoice or credit memo, and then choose the **OK** button.</span></span>

    <span data-ttu-id="a0b92-121">Многие поля, в частности **Сумма** и **Срок**, при этом заполняются информацией из выбранного документа.</span><span class="sxs-lookup"><span data-stu-id="a0b92-121">Many fields, such as the **Amount** and **Due Date** fields, are now filled in with information from the selected document.</span></span>
5. <span data-ttu-id="a0b92-122">Другой вариант — использовать функцию **Предлож. оплаты поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="a0b92-122">Alternatively, use the **Suggest Vendor Payments** function.</span></span> <span data-ttu-id="a0b92-123">В этом случае вся информация о документе, к которому применяется платеж, и суммы также вводятся в строки журнала.</span><span class="sxs-lookup"><span data-stu-id="a0b92-123">All the applies-to information and amounts are then also entered on the journal lines.</span></span> <span data-ttu-id="a0b92-124">Дополнительные сведения см. в разделе [Предложение оплаты поставщикам](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="a0b92-124">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

    <span data-ttu-id="a0b92-125">Будут появляться сообщения, помогающие вам правильно заполнить обязательные поля.</span><span class="sxs-lookup"><span data-stu-id="a0b92-125">Messages will guide you to fill in the required fields correctly.</span></span>
6.  <span data-ttu-id="a0b92-126">Когда все строки журнала платежей будут заполнены, выберите действие **Учет**.</span><span class="sxs-lookup"><span data-stu-id="a0b92-126">When all payment journal lines are completed, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0b92-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a0b92-127">See Also</span></span>
[<span data-ttu-id="a0b92-128">Совершение платежей с помощью платежных документов</span><span class="sxs-lookup"><span data-stu-id="a0b92-128">Make Check Payments</span></span>](payables-how-work-checks.md)  
[<span data-ttu-id="a0b92-129">Совершение электронных платежей</span><span class="sxs-lookup"><span data-stu-id="a0b92-129">Make Electronic Payments</span></span>](payables-how-export-payments-bank-file.md)  
[<span data-ttu-id="a0b92-130">Управление кредиторской задолженностью</span><span class="sxs-lookup"><span data-stu-id="a0b92-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="a0b92-131">Настройка банковских операций</span><span class="sxs-lookup"><span data-stu-id="a0b92-131">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="a0b92-132">Экспорт файла Positive Pay</span><span class="sxs-lookup"><span data-stu-id="a0b92-132">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="a0b92-133">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0b92-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
