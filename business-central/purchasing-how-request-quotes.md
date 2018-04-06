---
title: "Создание предложения по покупке для запроса предложения | Документы Майкрософт"
description: "Описывается процесс создание предложения по продаже или запроса предложения (RFQ) для записи вашего предложения клиенту для продажи продуктов на определенных условиях."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 19e7b8e55d3276730c16401b1d5d0d8203b7e7c9
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="request-quotes"></a><span data-ttu-id="dc537-103">Запрос предложений</span><span class="sxs-lookup"><span data-stu-id="dc537-103">Request Quotes</span></span>
<span data-ttu-id="dc537-104">Предложение по покупке может использоваться в качестве предварительного предложения по заказу на покупку, а заказ затем может быть преобразован в счет или заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="dc537-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="dc537-105">Создание предложения по покупке</span><span class="sxs-lookup"><span data-stu-id="dc537-105">To create a purchase quote</span></span>
1. <span data-ttu-id="dc537-106">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Предложения по покупке**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="dc537-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="dc537-107">Создайте новый документ, так же, как это делается для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="dc537-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="dc537-108">Дополнительные сведения см. в разделе [Регистрация покупок](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dc537-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="dc537-109">Преобразование предложения по покупке в заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="dc537-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="dc537-110">Когда вы приняли предложение поставщика, можно преобразовать его в счет или заказ покупки для обработки покупки.</span><span class="sxs-lookup"><span data-stu-id="dc537-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="dc537-111">Откройте предложение по покупке, которое готово к преобразованию, затем выберите действие **Сделать заказ**.</span><span class="sxs-lookup"><span data-stu-id="dc537-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="dc537-112">Предложение по покупке удаляется из базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc537-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="dc537-113">Создается счет покупки или заказ на покупку на основе сведений в предложении по покупке, в котором можно обработать покупку.</span><span class="sxs-lookup"><span data-stu-id="dc537-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="dc537-114">В поле **Номер предложения** в счете покупке или заказе покупки отображается номер предложения по покупки, из которого он создан.</span><span class="sxs-lookup"><span data-stu-id="dc537-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc537-115">См. также</span><span class="sxs-lookup"><span data-stu-id="dc537-115">See Also</span></span>
[<span data-ttu-id="dc537-116">Покупки</span><span class="sxs-lookup"><span data-stu-id="dc537-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="dc537-117">Настройка покупки</span><span class="sxs-lookup"><span data-stu-id="dc537-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="dc537-118">Отправка документов по электронной почте</span><span class="sxs-lookup"><span data-stu-id="dc537-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="dc537-119">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc537-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
