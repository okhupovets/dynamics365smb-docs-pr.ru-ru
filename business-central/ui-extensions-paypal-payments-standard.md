---
title: "Использование расширения PayPal Payments Standard | Microsoft Docs"
description: "Описывается порядок использования расширения, чтобы клиенты могли совершать платежи через PayPal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 356f01706f40bdb8fd46871e3dbde73577a78117
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="the-paypal-payments-standard-extension-to-business-central"></a><span data-ttu-id="2c42e-103">Расширение PayPal Payments Standard для Business Central</span><span class="sxs-lookup"><span data-stu-id="2c42e-103">The PayPal Payments Standard Extension to Business Central</span></span> 
<span data-ttu-id="2c42e-104">Клиенты постоянно требуют более высокого качества обслуживания как с точки зрения качества продукции, так и с точки зрения вариантов доставки и оплаты.</span><span class="sxs-lookup"><span data-stu-id="2c42e-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="2c42e-105">Служба стандарта платежей PayPal помогает улучшить качество обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2c42e-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="2c42e-106">В качестве альтернативы сбору платежей через банковские переводы или кредитные карты вы можете предложить клиентам оплату через учетную запись PayPal.</span><span class="sxs-lookup"><span data-stu-id="2c42e-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="2c42e-107">Когда вы отправляете счет продажи или заказ на продажу по электронной почте, в содержании сообщения эл. почты и во вложенном PDF-документе имеется ссылка PayPal.</span><span class="sxs-lookup"><span data-stu-id="2c42e-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="2c42e-108">Когда клиент выбирает эту ссылку, открывается страница сервиса для его учетной записи PayPal, содержащая сведения об оплате этой продажи.</span><span class="sxs-lookup"><span data-stu-id="2c42e-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="2c42e-109">Затем клиент может оплатить счет как любой другой платеж PayPal.</span><span class="sxs-lookup"><span data-stu-id="2c42e-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="2c42e-110">Служба стандарта платежей PayPal предоставляет следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="2c42e-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="2c42e-111">Платежи клиентов быстрее поступают на ваш банковский счет.</span><span class="sxs-lookup"><span data-stu-id="2c42e-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="2c42e-112">У клиентов есть больше способов оплачивать счета.</span><span class="sxs-lookup"><span data-stu-id="2c42e-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="2c42e-113">PayPal предлагает надежную службу платежей, которой клиенты отдают предпочтение по сравнению с вводом данных кредитных карт на веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="2c42e-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="2c42e-114">PayPal предлагает несколько способов обработки платежей, в том числе обработку кредитных карт, счета PayPal и другие источники.</span><span class="sxs-lookup"><span data-stu-id="2c42e-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="2c42e-115">Ссылку PayPal можно автоматически добавить в документы продажи или пользователем вручную.</span><span class="sxs-lookup"><span data-stu-id="2c42e-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="2c42e-116">Служба стандарта платежей PayPal не включает ежемесячные расходы или сборы за установку.</span><span class="sxs-lookup"><span data-stu-id="2c42e-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="2c42e-117">Поскольку она является расширением, вы можете легко включать службу стандарта платежей PayPal только тогда, когда она нужна для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="2c42e-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="2c42e-118">Дополнительные сведения см. в разделе [Включение платежей клиентов через PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="2c42e-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c42e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2c42e-119">See Also</span></span>
<span data-ttu-id="2c42e-120">[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2c42e-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2c42e-121">Настройка продаж</span><span class="sxs-lookup"><span data-stu-id="2c42e-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="2c42e-122">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c42e-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
