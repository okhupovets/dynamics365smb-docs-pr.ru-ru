---
title: "Учет в пакетном режиме выпуска продукции и времени работы | Документы Майкрософт"
description: "Количество выхода отражает выполнение работы в единицах завершенного количества."
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
ms.openlocfilehash: d1813ab3105023e56347c9321fbbb10944e7f09f
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="7f0da-103">Учет в пакетном режиме выпуска продукции и времени работы</span><span class="sxs-lookup"><span data-stu-id="7f0da-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="7f0da-104">Количество выхода отражает выполнение работы в единицах завершенного количества.</span><span class="sxs-lookup"><span data-stu-id="7f0da-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="7f0da-105">Только при учете количества выхода в последней операции товарные запасы обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="7f0da-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="7f0da-106">Учет количества выпущенной продукции для одной или нескольких строк производственного заказа</span><span class="sxs-lookup"><span data-stu-id="7f0da-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="7f0da-107">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал выхода продукции**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7f0da-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7f0da-108">Заполните поля данными производственного заказа и данными о выпуске продукции.</span><span class="sxs-lookup"><span data-stu-id="7f0da-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7f0da-109">Если операция была завершена, выберите поле **Завершен**.</span><span class="sxs-lookup"><span data-stu-id="7f0da-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="7f0da-110">Если склад, на котором должны размещаться товары, использует ячейки, но не требует обработки размещения, присвойте код ячейки строке журнала для указания места на складе, где должны размещаться товары.</span><span class="sxs-lookup"><span data-stu-id="7f0da-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="7f0da-111">Дополнительные сведения см. в разделе [Размещение выпуска продукции или сборки](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="7f0da-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="7f0da-112">Выберите действие **Учесть**, чтобы учесть операции.</span><span class="sxs-lookup"><span data-stu-id="7f0da-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="7f0da-113">Учет количества выхода продукции выполнен.</span><span class="sxs-lookup"><span data-stu-id="7f0da-113">The output quantity will be posted.</span></span> <span data-ttu-id="7f0da-114">Теперь этот товар доступен для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="7f0da-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="7f0da-115">Учет времени работы для одной или нескольких строк производственного заказа</span><span class="sxs-lookup"><span data-stu-id="7f0da-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="7f0da-116">Время работы отражает выполнение работы в единицах необходимого рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="7f0da-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="7f0da-117">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал выхода продукции**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="7f0da-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7f0da-118">Заполните поля данными производственного заказа и данными о выпуске продукции.</span><span class="sxs-lookup"><span data-stu-id="7f0da-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="7f0da-119">Если операция завершена, выберите поле **Завершен**.</span><span class="sxs-lookup"><span data-stu-id="7f0da-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="7f0da-120">Выберите действие **Учет** для учета времени, затраченного на операцию.</span><span class="sxs-lookup"><span data-stu-id="7f0da-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="7f0da-121">Операции в книге производственных мощностей обновляются для используемых производственных или машинных центров.</span><span class="sxs-lookup"><span data-stu-id="7f0da-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f0da-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7f0da-122">See Also</span></span>  
<span data-ttu-id="7f0da-123">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7f0da-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7f0da-124">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="7f0da-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7f0da-125">[Планирование](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="7f0da-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="7f0da-126">Наличие</span><span class="sxs-lookup"><span data-stu-id="7f0da-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7f0da-127">Покупки</span><span class="sxs-lookup"><span data-stu-id="7f0da-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7f0da-128">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7f0da-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
