---
title: "Об оценке себестоимости товаров | Документы Майкрософт"
description: "Управление себестоимостью запасов связано с записью и отчетностью по текущим бизнес-расходам. Он включает в себя отчетность по себестоимости производства и запасов, то есть, по себестоимости товаров."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b36555e2853eb46c49aca4c4737e27d39fee929
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="about-inventory-costing"></a><span data-ttu-id="f7e5b-104">Об оценке себестоимости товаров</span><span class="sxs-lookup"><span data-stu-id="f7e5b-104">About Inventory Costing</span></span>
<span data-ttu-id="f7e5b-105">Управление себестоимостью запасов связано с записью и отчетностью по текущим бизнес-расходам.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-105">Managing inventory costs is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="f7e5b-106">Он включает в себя отчетность по себестоимости производства и запасов, то есть, по себестоимости товаров.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>  

 <span data-ttu-id="f7e5b-107">Необходимо понять такие главные принципы: от выбора метода учета себестоимости зависит, как определяется стоимость товаров, когда они покидают склад; в результате коррекции стоимости стоимость проданных товаров обновляется связанной стоимостью покупки, учтенной после продажи; стоимость товаров должна учитываться в соответствующих счетах ГК через равные интервалы.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>  

 <span data-ttu-id="f7e5b-108">В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="f7e5b-109">**Задача**</span><span class="sxs-lookup"><span data-stu-id="f7e5b-109">**To**</span></span>|<span data-ttu-id="f7e5b-110">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="f7e5b-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="f7e5b-111">Ознакомление с различиями между пятью разными методами учета себестоимости и их влиянием на потоки стоимости.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-111">Distinguish the five different costing methods and their effect on cost flows.</span></span>|[<span data-ttu-id="f7e5b-112">Сведения о проектировании: методы учета себестоимости</span><span class="sxs-lookup"><span data-stu-id="f7e5b-112">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)|  
|<span data-ttu-id="f7e5b-113">Получение сведений о том, какие операции применения товаров динамически связывают уменьшение запасов с увеличением для контроля над потоками стоимости.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-113">Learn how item application entries dynamically link inventory decreases with increases to keep control of cost flows.</span></span>|[<span data-ttu-id="f7e5b-114">Сведения о проектировании: применение товара</span><span class="sxs-lookup"><span data-stu-id="f7e5b-114">Design Details: Item Application</span></span>](design-details-item-application.md)|  
|<span data-ttu-id="f7e5b-115">Получение сведений о том, как себестоимость единицы товара постоянно обновляется стоимостью ее последней транзакции в соответствии с методом учета себестоимости товара.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-115">Learn how an item's unit cost is continuously updated with the cost of its latest transaction according to the item's costing method.</span></span>|[<span data-ttu-id="f7e5b-116">Сведения о проектировании: коррекция себестоимости</span><span class="sxs-lookup"><span data-stu-id="f7e5b-116">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)|  
|<span data-ttu-id="f7e5b-117">Получение сведений о том, как в соответствии с выбранным периодом расчета средней себестоимости динамически вычисляется средняя себестоимость товаров.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-117">Learn how an item's average cost is dynamically calculated according to the selected average cost period.</span></span>|[<span data-ttu-id="f7e5b-118">Сведения о проектировании: средняя себестоимость</span><span class="sxs-lookup"><span data-stu-id="f7e5b-118">Design Details: Average Cost</span></span>](design-details-average-cost.md)|  
|<span data-ttu-id="f7e5b-119">Ознакомление с различиями между ожидаемой себестоимостью (на которую еще не выставлен счет) и фактической себестоимостью, а также получение сведений об управлении ожидаемой себестоимостью в главной книге.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-119">Distinguish expected cost (not yet invoiced) from actual cost and learn how it is managed in the general ledger.</span></span>|[<span data-ttu-id="f7e5b-120">Сведения о проектировании: учет ожидаемой себестоимости</span><span class="sxs-lookup"><span data-stu-id="f7e5b-120">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)|  
|<span data-ttu-id="f7e5b-121">Получение сведений о механизме коррекции себестоимости, гарантирующем перенос себестоимости, даже если транзакции запасов производятся случайным образом.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-121">Understand the cost adjustment mechanism, which ensures that costs are brought forward even if inventory transactions happen in a random manner.</span></span>|[<span data-ttu-id="f7e5b-122">Сведения о проектировании: коррекция себестоимости</span><span class="sxs-lookup"><span data-stu-id="f7e5b-122">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)|  
|<span data-ttu-id="f7e5b-123">Получение сведений о том, почему производители часто используют стандартную себестоимость в качестве базы оценки стоимости для компонентов и конечных товаров.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-123">Read why standard costs are often used by manufacturing companies as a valuation base for components and end items.</span></span>|[<span data-ttu-id="f7e5b-124">О расчете стандартной себестоимости</span><span class="sxs-lookup"><span data-stu-id="f7e5b-124">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="f7e5b-125">Получение сведений о том, как стоимость запасов отражается в главной книге.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-125">Understand how the value of inventory is reflected in the general ledger.</span></span>|[<span data-ttu-id="f7e5b-126">Отчет о затратах и выверка с главной книгой</span><span class="sxs-lookup"><span data-stu-id="f7e5b-126">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="f7e5b-127">Получение сведений о том, как товарные издержки, такие как затраты на перевозку и страхование, могут стать дополнительными компонентами стоимости в себестоимости единицы товара.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-127">Learn how item charges, such as freight and insurance, can assign additional cost components to an item's unit cost.</span></span>|[<span data-ttu-id="f7e5b-128">Использование товарных издержек для учета дополнительных торговых расходов</span><span class="sxs-lookup"><span data-stu-id="f7e5b-128">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|  
|<span data-ttu-id="f7e5b-129">Получение сведений о том, как периоды учета запасов помогают организации управлять стоимостью запасов во времени путем определения более коротких периодов, которые могут закрываться для учета в течение финансового года.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-129">Read how inventory periods help a company to control inventory value over time by defining shorter periods that can be closed for posting as the fiscal year progresses.</span></span>|[<span data-ttu-id="f7e5b-130">Работа с учетными периодами</span><span class="sxs-lookup"><span data-stu-id="f7e5b-130">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="f7e5b-131">Познакомьтесь со всеми механизмами расчета себестоимости, в том числе узнайте, что происходит при учете транзакций сборки и производства.</span><span class="sxs-lookup"><span data-stu-id="f7e5b-131">Understand all mechanisms in the costing engine, including what happens when you post assembly and production transactions.</span></span>|[<span data-ttu-id="f7e5b-132">Сведения о проектировании: себестоимость запасов</span><span class="sxs-lookup"><span data-stu-id="f7e5b-132">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|

## <a name="see-also"></a><span data-ttu-id="f7e5b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f7e5b-133">See Also</span></span>
<span data-ttu-id="f7e5b-134">[Управление себестоимостью товаров](finance-manage-inventory-costs.md)  </span><span class="sxs-lookup"><span data-stu-id="f7e5b-134">[Managing Inventory Costs](finance-manage-inventory-costs.md)  </span></span>  
<span data-ttu-id="f7e5b-135">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7e5b-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
