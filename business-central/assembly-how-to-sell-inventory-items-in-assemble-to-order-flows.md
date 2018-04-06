---
title: "Практическое руководство. Продажа складских товаров в потоках сборки на заказ | Документы Майкрософт"
description: "Если товар настроен для карточки сборки на заказ, процесс продажи по умолчанию предполагает, что товар отсутствует в запасах и должен быть собран для данного конкретного заказа на продажу. Поэтому связанный сборочный заказ создается автоматически при добавлении товара в строку заказа на продажу."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 97b79683ba6c770912349c772f1f7adb443b94ed
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a><span data-ttu-id="365c1-104">Продажа складских товаров в потоках сборки на заказ</span><span class="sxs-lookup"><span data-stu-id="365c1-104">Sell Inventory Items in Assemble-to-Order Flows</span></span>
<span data-ttu-id="365c1-105">Если поле **Политика сборки** в карточке товара сборочного элемента имеет значение **Сборка на заказ** процесс продажи по умолчанию предполагает, что товар отсутствует в запасах и должен быть собран для данного конкретного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-105">If the **Assembly Policy** field on the item card of an assembly item contains **Assemble-to-Order**, then the default sales order process assumes that the item is not in inventory and must be assembled for that specific sales order.</span></span> <span data-ttu-id="365c1-106">Поэтому связанный сборочный заказ создается автоматически при добавлении товара в строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-106">Therefore, a linked assembly order is automatically created when you add the item to a sales order line.</span></span> <span data-ttu-id="365c1-107">Дополнительные сведения см. в разделе [Продажа товара, собранного на заказ](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="365c1-107">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span> <span data-ttu-id="365c1-108">Если часть (или все) количества заказов на продажу уже доступна на складе, можно создать уменьшение количества сборочного заказа, изменив поле **Количество для сборки на заказ** в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-108">However, if a part of the sales order quantity is already available in inventory, then you can decrease the assembly order quantity by changing the **Qty. to Assemble to Order** field on the sales order line.</span></span>  

<span data-ttu-id="365c1-109">Этот сценарий редок, так как ожидается, что товары для сборки на заказ всегда настраиваются и вероятность того, что они попадут в запас в конфигурации, запрашиваемый другим клиентом, мала.</span><span class="sxs-lookup"><span data-stu-id="365c1-109">This scenario is rare because assemble-to-order items are expected to always be customized, and the chance that they are in inventory in the configuration that is requested by another customer is low.</span></span> <span data-ttu-id="365c1-110">Если в организации существуют количества сборок на заказ на складе из-за возвратов или отмен заказов, эти количества должны быть подобраны и проданы прежде чем будут собраны новые заказы.</span><span class="sxs-lookup"><span data-stu-id="365c1-110">However, if a company does have assemble-to-order quantities in inventory because of returns or order cancellations, then these quantities should be picked and sold before new ones are assembled.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="365c1-111">В заказах на продажу нет функции, которые автоматически предупреждает пользователя или помогает вычесть количества сборочного заказа, которые уже имеются.</span><span class="sxs-lookup"><span data-stu-id="365c1-111">No functionality exists on sales orders that automatically alerts or helps you deduct assembly order quantities that are already available.</span></span> <span data-ttu-id="365c1-112">Вместо этого, необходимо отслеживать сведения о наличии, например сведения на информационной панели **Подробности по строке продажи**.</span><span class="sxs-lookup"><span data-stu-id="365c1-112">Instead, you must monitor availability information, such as in the **Sales Line Details** FactBox.</span></span>  

<span data-ttu-id="365c1-113">Аналогичная функция доступна при продаже сборочных элементов из запасов, если часть или все количество отсутствует и может быть поставлено сборочным заказом.</span><span class="sxs-lookup"><span data-stu-id="365c1-113">Similar functionality is available when you are selling assembly items from inventory and a part or all of the quantity is unavailable and can be supplied by an assembly order.</span></span> <span data-ttu-id="365c1-114">Дополнительные сведения см. в разделе [Совместная продажа товаров, собираемых на заказ, и складских товаров](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span><span class="sxs-lookup"><span data-stu-id="365c1-114">For more information, see [Sell Assemble-to-Order Items and Inventory Items Together](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="365c1-115">Некоторые правила применяются к полю **Кол-во для отгрузки** в строках заказа на продажу, содержащих сочетание количеств сборки на заказ и количеств запасов.</span><span class="sxs-lookup"><span data-stu-id="365c1-115">Certain rules apply to the **Qty. to Ship** field on sales order lines that contain a combination of assemble-to-order quantities and inventory quantities.</span></span> <span data-ttu-id="365c1-116">Дополнительные сведения см. в подразделе "Сценарии комбинации" в разделе [Сборка на заказ и сборка на склад](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="365c1-116">For more information, see the Combination Scenarios section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>  

<span data-ttu-id="365c1-117">В рамках этой процедуры заменяется количество сборки на заказ на количество запасов в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-117">In this procedure, you replace assemble-to-order quantities with inventory quantities on a sales order line.</span></span> <span data-ttu-id="365c1-118">Эти действия включают в себя определение наличия, вычитание этого количество из связанного сборочного заказа и дальнейшее резервирование этого количества товара для обеспечения его подбора и отгрузки по заказу.</span><span class="sxs-lookup"><span data-stu-id="365c1-118">The steps include detecting that availability exists, deducting that quantity from the linked assembly order, and then reserving the inventory quantity to make sure that it is picked and shipped for the order.</span></span>  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><span data-ttu-id="365c1-119">Продажа складских товаров в потоках сборки на заказ</span><span class="sxs-lookup"><span data-stu-id="365c1-119">To sell inventory items in assemble-to-order flows</span></span>  
1.  <span data-ttu-id="365c1-120">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на продажу**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="365c1-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="365c1-121">Создайте заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-121">Create a sales order.</span></span> <span data-ttu-id="365c1-122">Дополнительные сведения см. в разделе [Продажа продукции](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="365c1-122">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3.  <span data-ttu-id="365c1-123">В строке заказа на продажу для товара сборки на заказ в поле **Кол-во** введите требуемое количество.</span><span class="sxs-lookup"><span data-stu-id="365c1-123">On a sales order line for an assemble-to-order item, in the **Quantity** field, enter the demanded quantity.</span></span>  
4.  <span data-ttu-id="365c1-124">На информационной панели **Подробности по строке продажи** укажите, доступна ли некоторая часть или все количество из затребованного.</span><span class="sxs-lookup"><span data-stu-id="365c1-124">In the **Sales Line Details** FactBox, determine if all or some of the demanded quantity is available.</span></span>  
5.  <span data-ttu-id="365c1-125">В поле **Количество для сборки на заказ** определите доступное количество, чтобы только недоступное количество было собрано на заказ.</span><span class="sxs-lookup"><span data-stu-id="365c1-125">In the **Qty. to Assemble to Order** field, deduct the available quantity so that only the unavailable quantity is assembled to the order.</span></span> <span data-ttu-id="365c1-126">Значение в поле **Зарезервированное кол-во** соответственно сокращается для отображения того, что ссылка заказ-на-заказ или резервирование относится только к количеству, которое необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="365c1-126">The **Reserved Quantity** field is decreased accordingly to reflect that the order-to-order link, or reservation, only applies to the quantity to be assembled.</span></span>  
6.  <span data-ttu-id="365c1-127">На экспресс-вкладке **Строки** выберите **Функции**, затем выберите действие **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="365c1-127">On the **Lines** FastTab, choose **Functions**, and then choose the **Reserve** action.</span></span>  
7.  <span data-ttu-id="365c1-128">В окне **Резервирование** выберите строки книги товаров, которые содержат доступные количества, затем выберите действие **Резервировать по текущей строке** и далее нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="365c1-128">In the **Reservation** window, select the item ledger entry line or lines that contain the available quantities, choose the **Reserve from Current Line** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="365c1-129">В окне **Заказ на продажу** поле **Зарезервированное кол-во** показывает, что все количество в строке заказа зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="365c1-129">In the **Sales Order** window, the **Reserved Quantity** field now shows that the whole order line quantity is reserved.</span></span> <span data-ttu-id="365c1-130">Поле **Количество для сборки на заказ** все еще отражает часть этого количества, которую необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="365c1-130">The **Qty. to Assemble to Order** field still reflects the subquantity that has to be assembled.</span></span>  

8.  <span data-ttu-id="365c1-131">Выпуск заказа на продажу для подбора товаров и сборки отсутствующих товаров.</span><span class="sxs-lookup"><span data-stu-id="365c1-131">Release the sales order for picking of the inventory items and for assembly of the unavailable items.</span></span> <span data-ttu-id="365c1-132">Дополнительные сведения см. в разделе [Сборка товаров](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="365c1-132">For more information, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="365c1-133">Поле **Код ячейки** в заказе на продажу может быть предварительно заполнено в соответствии с полем **Код ячейки сборки на заказ** или **Код исходящей сборочн. ячейки** в карточке склада.</span><span class="sxs-lookup"><span data-stu-id="365c1-133">The **Bin Code** field on the sales order may be prefilled according to the **Assemble-to-Order Shpt. Bin Code** or the **From-Assembly Bin Code** field on the location card.</span></span> <span data-ttu-id="365c1-134">В этом случае поле **Код ячейки** в строке заказа продажи может быть неправильным при таком сочетании количества сборки на заказ и сборки на склад.</span><span class="sxs-lookup"><span data-stu-id="365c1-134">In that case, the **Bin Code** field on the sales order line may be incorrect in this combination of assemble-to-order and assemble-to-stock quantities.</span></span> <span data-ttu-id="365c1-135">Рекомендуется также просмотреть поле **Код ячейки** и убедиться, что размещение работает для всех количеств.</span><span class="sxs-lookup"><span data-stu-id="365c1-135">It is a good idea to look in the **Bin Code** field and ensure that the placement works for all quantities.</span></span> <span data-ttu-id="365c1-136">В качестве альтернативы введите два разных количества в отдельных строках заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="365c1-136">Alternatively, enter the two different quantities on separate sales order lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="365c1-137">См. также</span><span class="sxs-lookup"><span data-stu-id="365c1-137">See Also</span></span>  
[<span data-ttu-id="365c1-138">Управление сборкой</span><span class="sxs-lookup"><span data-stu-id="365c1-138">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="365c1-139">Резервирование товаров</span><span class="sxs-lookup"><span data-stu-id="365c1-139">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
[<span data-ttu-id="365c1-140">Работа со спецификациями</span><span class="sxs-lookup"><span data-stu-id="365c1-140">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="365c1-141">Наличие</span><span class="sxs-lookup"><span data-stu-id="365c1-141">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="365c1-142">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="365c1-142">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="365c1-143">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="365c1-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
