---
title: "Расчет даты для продаж | Документы Майкрософт"
description: "Программа автоматически вычисляет дату, когда следует заказать товар, чтобы иметь его на складе на определенную дату. Это дата, когда можно ожидать, что товары, заказанные на конкретную дату, будут доступны для подбора."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cc73a03c44896bda5d1fdf789a8b349f796c6e58
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="e2304-104">Расчет даты для продаж</span><span class="sxs-lookup"><span data-stu-id="e2304-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e2304-105"> автоматически вычисляет наиболее раннюю дату, на которую может быть произведена отгрузка товара, указанного в строке заказа за продажу.</span><span class="sxs-lookup"><span data-stu-id="e2304-105"> automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="e2304-106">Если клиент потребовал, чтобы поставка была произведена на конкретную дату, то дата, на которую товар должен быть в наличии для того, чтобы обеспечить выполнение этого требования, также будет вычислена.</span><span class="sxs-lookup"><span data-stu-id="e2304-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="e2304-107">Если клиент не запрашивает, чтобы поставка была произведена на определенную дату, то будет автоматически рассчитана дата, на которую может быть произведена поставка товара, начиная с даты, когда товар будет в наличии.</span><span class="sxs-lookup"><span data-stu-id="e2304-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="e2304-108">Вычисление требуемой даты доставки</span><span class="sxs-lookup"><span data-stu-id="e2304-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="e2304-109">Если в строке заказа продажи задана требуемая дата отгрузки, эта дата будет использована в качестве отправной точки для следующих расчетов.</span><span class="sxs-lookup"><span data-stu-id="e2304-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="e2304-110">требуемая дата доставки - время отгрузки = плановая дата поставки</span><span class="sxs-lookup"><span data-stu-id="e2304-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="e2304-111">плановая дата поставки - исходящие - время обработки склада = дата поставки</span><span class="sxs-lookup"><span data-stu-id="e2304-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="e2304-112">Если на дату отгрузки товар имеется в наличии, процесс продажи может быть продолжен.</span><span class="sxs-lookup"><span data-stu-id="e2304-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="e2304-113">Если на дату отгрузки товар отсутствует, отображается предупреждение контроля склада.</span><span class="sxs-lookup"><span data-stu-id="e2304-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="e2304-114">Расчет наиболее ранней возможной даты доставки</span><span class="sxs-lookup"><span data-stu-id="e2304-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="e2304-115">Если не указать требуемую дату доставки в строке заказа продажи, либо если соблюсти требуемая дата доставки невозможно, вычисляется самая ранняя дата, на которую доступны товары.</span><span class="sxs-lookup"><span data-stu-id="e2304-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="e2304-116">Затем эта дата вводится в поле Дата отгрузки в строке, и дата, в которую планируется отгрузки товаров, а также дата, в которую они будут доставлены клиенту, рассчитываются по следующим формулам.</span><span class="sxs-lookup"><span data-stu-id="e2304-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="e2304-117">дата отгрузки + исходящие - время обработки склада = плановая дата отгрузки</span><span class="sxs-lookup"><span data-stu-id="e2304-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="e2304-118">плановая дата поставки + время отгрузки = плановая дата доставки</span><span class="sxs-lookup"><span data-stu-id="e2304-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="e2304-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e2304-119">See Also</span></span>  
 <span data-ttu-id="e2304-120">[Расчет даты для покупок](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="e2304-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="e2304-121">Расчет сроков планирования заказов</span><span class="sxs-lookup"><span data-stu-id="e2304-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="e2304-122">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2304-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
