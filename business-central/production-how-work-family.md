---
title: "Как использовать семейства товаров в производстве | Документы Майкрософт"
description: "Главной задачей при настройке личного календаря для вашей организации или организации-партнера является внесение необходимых изменений статуса рабочих и нерабочих дней."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 51c505decb595f1da3aba61a73a1f2a55608fc22
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-production-families"></a><span data-ttu-id="cc97b-103">Работа с производственными семействами</span><span class="sxs-lookup"><span data-stu-id="cc97b-103">Work with Production Families</span></span>
<span data-ttu-id="cc97b-104">Производственное семейство — это группа отдельных товаров, взаимосвязь которых основана на подобии процессов изготовления.</span><span class="sxs-lookup"><span data-stu-id="cc97b-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="cc97b-105">Формирование производственных семейств позволяет некоторым товарам производиться дважды или более раз в одном производстве, что оптимизирует потребление материалов.</span><span class="sxs-lookup"><span data-stu-id="cc97b-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="cc97b-106">В поле **Количество** окна **Семейство** введите количество, которое будет произведено, если все семейство было произведено единожды.</span><span class="sxs-lookup"><span data-stu-id="cc97b-106">In the **Quantity** field in the **Family** window, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="cc97b-107">Пример</span><span class="sxs-lookup"><span data-stu-id="cc97b-107">Example</span></span>
<span data-ttu-id="cc97b-108">В штамповочных процессах четыре детали одного и того же товара могут производиться из одного листа в то время, как из другого листа за то же время может быть произведено 10 деталей.</span><span class="sxs-lookup"><span data-stu-id="cc97b-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="cc97b-109">Штамповочная машина проштампует все 14 деталей за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="cc97b-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="cc97b-110">Формирование производственных семейств снижает количество отхода, так как то, что обычно является ненужным отходом при производстве крупных деталей, может использоваться для производства мелких деталей.</span><span class="sxs-lookup"><span data-stu-id="cc97b-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="cc97b-111">Настройка производственного семейства</span><span class="sxs-lookup"><span data-stu-id="cc97b-111">To set up a production family</span></span>
1. <span data-ttu-id="cc97b-112">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Семейства**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="cc97b-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="cc97b-113">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="cc97b-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a><span data-ttu-id="cc97b-114">Для производства на основе производственного семейства</span><span class="sxs-lookup"><span data-stu-id="cc97b-114">To produce based on a production familily</span></span>
1. <span data-ttu-id="cc97b-115">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Утвержд. произв. заказы**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="cc97b-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="cc97b-116">Создайте новый производственный заказ.</span><span class="sxs-lookup"><span data-stu-id="cc97b-116">Create a new production order.</span></span> <span data-ttu-id="cc97b-117">Дополнительные сведения см. в разделе [Создание производственных заказов](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="cc97b-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="cc97b-118">В поле **Тип источника** выберите **Семейство**.</span><span class="sxs-lookup"><span data-stu-id="cc97b-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="cc97b-119">В поле **Номер источника** выберите соответствующее производственное семейство.</span><span class="sxs-lookup"><span data-stu-id="cc97b-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc97b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cc97b-120">See Also</span></span>
[<span data-ttu-id="cc97b-121">Создание производственных спецификаций</span><span class="sxs-lookup"><span data-stu-id="cc97b-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="cc97b-122">Настройка производства</span><span class="sxs-lookup"><span data-stu-id="cc97b-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="cc97b-123">[Производство](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="cc97b-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="cc97b-124">[Планирование](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="cc97b-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="cc97b-125">Наличие</span><span class="sxs-lookup"><span data-stu-id="cc97b-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cc97b-126">Покупки</span><span class="sxs-lookup"><span data-stu-id="cc97b-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cc97b-127">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cc97b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
