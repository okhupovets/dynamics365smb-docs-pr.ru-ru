---
title: "Настройка кредитового перевода SEPA | Microsoft Docs"
description: "Узнайте, как настроить кредитовый перевод SEPA в Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64abd01caa2a2f6845bb3d54c7721333a0a360b3
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-credit-transfer"></a><span data-ttu-id="35053-103">Настройка кредитового перевода SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-103">Set Up SEPA Credit Transfer</span></span>
<span data-ttu-id="35053-104">В окне **Журнал платежей** можно экспортировать платежи в файл для отправки в электронный банк на обработку связанных денежных переводов.</span><span class="sxs-lookup"><span data-stu-id="35053-104">From the **Payment Journal** window, you can export payments to a file for upload to your electronic bank for processing of the related money transfers.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="35053-105"> поддерживает формат кредитового перевода SEPA, но в вашей стране или регионе могут быть доступны другие форматы электронных платежей.</span><span class="sxs-lookup"><span data-stu-id="35053-105"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="35053-106">Чтобы разрешить экспорт форматов банковских файлов, для которых отсутствует готовая поддержка в [!INCLUDE[d365fin](includes/d365fin_md.md)], можно настроить определение обмена данными при помощи платформы обмена данными.</span><span class="sxs-lookup"><span data-stu-id="35053-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="35053-107">Дополнительные сведения см. в разделе [Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="35053-107">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="35053-108">Прежде чем выполнять обработку платежа электронным способом путем экспорта файлов платежей в формате кредитового перевода SEPA, необходимо выполнить следующие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="35053-108">Before you can process payment electronically by exporting payment files in the SEPA Credit Transfer format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="35053-109">Настройка банковского счета для обработки формата кредитового перевода SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-109">Set up the bank account in question to handle the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="35053-110">Настройка карточек поставщика для обработки платежей путем экспорта файлов в формат кредитового перевода SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-110">Set up vendor cards to process payments by exporting files in the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="35053-111">Настройка соответствующего раздела финансового журнала для включения экспорта платежей из окна **Журнал платежей**</span><span class="sxs-lookup"><span data-stu-id="35053-111">Set up the related general journal batch to enable payment export from the **Payment Journal** window</span></span>  
* <span data-ttu-id="35053-112">Подключение определения обмена данными для одного или нескольких типов платежей к соответствующему методу или методам оплаты</span><span class="sxs-lookup"><span data-stu-id="35053-112">Connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a><span data-ttu-id="35053-113">Настройка банковского счета для кредитового перевода SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-113">To set up a bank account for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="35053-114">В поле **Поиск** введите **Банковские счета**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="35053-114">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35053-115">Откройте карточку банковского счета, из которой будут экспортироваться файлы платежей в формате кредитового перевода SEPA.</span><span class="sxs-lookup"><span data-stu-id="35053-115">Open the card of the bank account from which you will export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="35053-116">На экспресс-вкладке **Перемещение** в поле **Формат экспорта платежей**, выберите **SEPADD**.</span><span class="sxs-lookup"><span data-stu-id="35053-116">On the **Transfer** FastTab, in the **Payment Export Format** field, choose **SEPADD**.</span></span>  
4. <span data-ttu-id="35053-117">В поле **Серии номеров ид. сообщ. кред. переводов SEPA** выберите серию номеров, из которой назначаются номера операциями перемещения кредита SEPA.</span><span class="sxs-lookup"><span data-stu-id="35053-117">In the **SEPA CT Msg. ID No. Series** field, choose a number series from which numbers are assigned to SEPA credit transfer entries.</span></span>  
5. <span data-ttu-id="35053-118">Убедитесь, что заполнено поле **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="35053-118">Make sure the **IBAN** field is filled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="35053-119">В поле **Код валюты** должно быть задано значение **Евро**, так как кредитовые переводы SEPA можно выполнить только в евро.</span><span class="sxs-lookup"><span data-stu-id="35053-119">The **Currency Code** field must be set to **EUR**, because SEPA credit transfers can only be made in the EURO currency.</span></span>  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a><span data-ttu-id="35053-120">Настройка карточки поставщика для кредитового перевода SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-120">To set up a vendor card for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="35053-121">В поле **Поиск** введите **Поставщики**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="35053-121">In the **Search** box, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35053-122">Откройте карточку поставщика, платежи которому будут осуществляться электронным способом путем экспорта файлов платежей в формате кредитового перевода SEPA.</span><span class="sxs-lookup"><span data-stu-id="35053-122">Open the card of the vendor whom you will pay electronically by export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="35053-123">На экспресс-вкладке **Платеж** в поле **Код способа оплаты** выберите **БАНК**.</span><span class="sxs-lookup"><span data-stu-id="35053-123">On the **Payment** FastTab, in the **Payment Method Code** field, choose **BANK**.</span></span>  
4. <span data-ttu-id="35053-124">В поле **Предпочтительный банковский счет** выберите банк, в который будут переводиться денежные средства при обработке в электронном банке.</span><span class="sxs-lookup"><span data-stu-id="35053-124">In the **Preferred Bank Account** field, choose the bank to which the money will be transferred when it is processed by your electronic bank.</span></span>  

     <span data-ttu-id="35053-125">Значение в поле **Предпочтительный банковский счет** копируется в поле **Банковский счет получателя** в окне **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="35053-125">The value in the **Preferred Bank Account** field is copied to the **Recipient Bank Account** field in the **Payment Journal** window.</span></span>  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a><span data-ttu-id="35053-126">Настройка журнала платежей для экспорта платежных файлов</span><span class="sxs-lookup"><span data-stu-id="35053-126">To set the payment journal up to export payment files</span></span>  
1. <span data-ttu-id="35053-127">В поле **Поиск** введите **Журналы платежей**, а затем выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="35053-127">In the **Search** box, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35053-128">Откройте журнал платежей, который используется для обработки платежей путем экспорта файлов в формате кредитового перевода SEPA.</span><span class="sxs-lookup"><span data-stu-id="35053-128">Open the payment journal that you use to process payments by exporting files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="35053-129">В поле **Код раздела** нажмите кнопку раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="35053-129">In the **Batch Name** field, choose the drop\-down button.</span></span>  
4. <span data-ttu-id="35053-130">В окне **Разделы финансового журнала** на вкладке **Главная** в группе **Управление** выберите **Изменить список**.</span><span class="sxs-lookup"><span data-stu-id="35053-130">In the **General Journal Batches** window, on the **Home** tab, in the **Manage** group, choose **Edit List**.</span></span>  
5. <span data-ttu-id="35053-131">В строке журнала платежей, который будет использоваться для экспорта платежей, установите флажок **Разрешить экспорт платежей**.</span><span class="sxs-lookup"><span data-stu-id="35053-131">On the line for the payment journal that you will use to export payments, select the **Allow Payment Export** check box.</span></span>  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a><span data-ttu-id="35053-132">Подключение определения обмена данными для одного или нескольких типов платежей к соответствующему методу или методам оплаты</span><span class="sxs-lookup"><span data-stu-id="35053-132">To connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  
1. <span data-ttu-id="35053-133">В поле **Поиск** введите **Способы оплаты**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="35053-133">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35053-134">В окне **Способы платежа** выберите способ оплаты, используемый для экспорта платежей, а затем выберите поле **Определение строки экспорта платежа**.</span><span class="sxs-lookup"><span data-stu-id="35053-134">In the **Payment Methods** window, select the payment method that is used to export payments from, and then choose the **Pmt. Export Line Definition** field.</span></span>  
3. <span data-ttu-id="35053-135">В окне **Определение строки экспорта платежа** выберите код, который вы указали в поле **Код** на экспресс-вкладке **Определения строк** на шаге 4 раздела “Описание форматирования строк и столбцов в файле” процедуры [Настройка определений обмена данными](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="35053-135">In the **Pmt. Export Line Definitions** window, select the code that you specified in the **Code** field on the **Line Definitions** FastTab in step 4 in the “To describe the formatting of lines and columns in the file” section in the [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) procedure.</span></span>  

    <span data-ttu-id="35053-136">Мандат прямого дебета автоматически вставляется в поле **Идентификатор поручения на прямое дебетование** при создании счета продажи для клиента, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="35053-136">The direct-debit mandate is automatically inserted in the **Direct Debit Mandate ID** field when you create a sales invoice for the customer that you selected in step 2.</span></span> <span data-ttu-id="35053-137">Дополнительные сведения см. в разделе [Создание типовых строк продажи и покупки](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="35053-137">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="35053-138">См. также</span><span class="sxs-lookup"><span data-stu-id="35053-138">See Also</span></span>  
[<span data-ttu-id="35053-139">Сбор платежей с прямым дебетом SEPA</span><span class="sxs-lookup"><span data-stu-id="35053-139">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="35053-140">Настройка определений обмена данными</span><span class="sxs-lookup"><span data-stu-id="35053-140">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="35053-141">Создание типовых строк продажи и покупки</span><span class="sxs-lookup"><span data-stu-id="35053-141">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
[<span data-ttu-id="35053-142">Электронный обмен данными</span><span class="sxs-lookup"><span data-stu-id="35053-142">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
