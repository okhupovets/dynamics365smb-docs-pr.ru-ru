---
title: "Практическое руководство. Обновление стандартных себестоимостей | Microsoft Docs"
description: "Необходимо периодически обновлять стандартные себестоимости компонентов и развертывать новые стоимости вплоть до родительского товара."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c59977f847a020fbcda490893dbe15ed88ac1e5a
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="update-standard-costs"></a><span data-ttu-id="a25ff-103">Обновление стандартных себестоимостей</span><span class="sxs-lookup"><span data-stu-id="a25ff-103">Update Standard Costs</span></span>
<span data-ttu-id="a25ff-104">Необходимо периодически обновлять стандартные себестоимости компонентов и развертывать новые стоимости вплоть до родительского товара.</span><span class="sxs-lookup"><span data-stu-id="a25ff-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="a25ff-105">Процесс обычно состоит из следующих четырех этапов:</span><span class="sxs-lookup"><span data-stu-id="a25ff-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="a25ff-106">Обновите себестоимости на уровне компонента и производственных мощностей.</span><span class="sxs-lookup"><span data-stu-id="a25ff-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="a25ff-107">Дополнительные сведения см. в пакетном задании **Предложить станд. себестоимость товара**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="a25ff-108">Консолидация и свертывание компонентов и производственных мощностей для расчета общей себестоимости производства или сборки товаров.</span><span class="sxs-lookup"><span data-stu-id="a25ff-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="a25ff-109">Применение стандартной себестоимости, введенной при запуске предыдущих пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="a25ff-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="a25ff-110">Стандартные себестоимости не вступают в силу до ввода их в действие.</span><span class="sxs-lookup"><span data-stu-id="a25ff-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="a25ff-111">Дополнительные сведения см. в пакетном задании Выполнить изменения станд. себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a25ff-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="a25ff-112">Внедрение изменений для обновления поля **Себестоимость единицы** в карточке товара и выполнение переоценки товара на складе.</span><span class="sxs-lookup"><span data-stu-id="a25ff-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="a25ff-113">Дополнительные сведения см. в разделе [Переоценка запасов](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="a25ff-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="a25ff-114">Дополнительные сведения см. в разделе [Расчет стандартной себестоимости](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="a25ff-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="a25ff-115">Обновление стандартных себестоимостей</span><span class="sxs-lookup"><span data-stu-id="a25ff-115">To update standard costs</span></span>  
1.  <span data-ttu-id="a25ff-116">Запустите пакетное задание **Коррекция себест. запасов**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="a25ff-117">Запустите пакетное задание **Учет себест. запасов в ГК**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="a25ff-118">Откройте **Журнал станд. себестоимостей** и воспользуйтесь одной или несколькими из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="a25ff-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="a25ff-119">Запустите пакетное задание **Предложить станд. себестоимость товара**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="a25ff-120">Просмотрите результаты и внесите изменения, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="a25ff-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="a25ff-121">Запустите пакетное задание **Предложить стандартную себестоимость объема**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="a25ff-122">Просмотрите результаты и внесите изменения, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="a25ff-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="a25ff-123">Запустите пакетное задание **Свернуть стандартную себестоимость**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="a25ff-124">Просмотрите результаты и внесите изменения, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="a25ff-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="a25ff-125">Запустите пакетное задание **Выполнить изменения станд. себестоимости**.</span><span class="sxs-lookup"><span data-stu-id="a25ff-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="a25ff-126">Просмотрите и учтите окно **Журнал переоценки**, который был заполнен операциями с предыдущих шагов этого процесса.</span><span class="sxs-lookup"><span data-stu-id="a25ff-126">Review and post the **Revaluation Journal** window, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a25ff-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a25ff-127">See Also</span></span>  
 <span data-ttu-id="a25ff-128">[О расчете стандартной себестоимости](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="a25ff-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="a25ff-129">[Управление себестоимостью товаров](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="a25ff-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="a25ff-130">[Сведения о проектировании: методы учета себестоимости](design-details-costing-methods.md) [[Финансы](finance.md)</span><span class="sxs-lookup"><span data-stu-id="a25ff-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="a25ff-131">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a25ff-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
