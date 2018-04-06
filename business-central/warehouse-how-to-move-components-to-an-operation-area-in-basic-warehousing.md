---
title: "Как перемещать компоненты в производственную зону в основных конфигурациях склада | Документы Майкрософт"
description: "Если производственные операции выполняются на складе, необходимо переместить товары между внутренними ячейками, чтобы ответить на внутренние документы-источники, например продукцию, сборку или сервисные заказы на складе."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5e271b160d8a4969be296861f6746163fcfea6ba
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a><span data-ttu-id="2d68e-103">Перемещение компонентов в производственную зону в базовых конфигурациях склада</span><span class="sxs-lookup"><span data-stu-id="2d68e-103">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>
<span data-ttu-id="2d68e-104">Если производственные операции выполняются на складе, необходимо переместить товары между внутренними ячейками, чтобы ответить на внутренние документы-источники, например продукцию, сборку или сервисные заказы на складе.</span><span class="sxs-lookup"><span data-stu-id="2d68e-104">If item processing operations occur at your warehouse location, then you may have to move items between internal bins to respond to internal source documents, such as production, assembly, or service orders at the location.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d68e-105">Для получения информации о перемещении товаров между ячейками без документов-источников см. раздел Внутреннее перемещение.</span><span class="sxs-lookup"><span data-stu-id="2d68e-105">For information about moving items between bins without source documents, see Internal Movement.</span></span>  

<span data-ttu-id="2d68e-106">В расширенных конфигурациях склада, где склады используют поле настройки **Расширенный подбор и размещение**, можно использовать окно **Журнал перемещений** для перемещения товаров между ячейками. Для получения дополнительной информации см. раздел [Перемещение товаров в расширенных конфигурациях склада](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="2d68e-106">In advanced warehouse configurations, which are locations that use the **Directed Put-away and Pick** setup field, you can use the **Movement Worksheet** window to move items between bins. For more information, see [Move Items in Advanced warehouse Configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="2d68e-107">В рамках базовой конфигурации склада, в котором используется поле настройки **Ячейка обязательна** и поле настройки **Требуется подбор**, можно ввести перемещение товаров в область внутренних операций на основе внутренних документов-источников одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="2d68e-107">In basic warehouse configurations, which are locations that use the **Bin Mandatory** setup field and the **Require Pick** setup field, you can register movement of items to internal operation areas based on internal source documents in the following ways:</span></span>  

-   <span data-ttu-id="2d68e-108">С помощью окна **Перемещение запасов**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-108">With the **Inventory Movement** window.</span></span>  
-   <span data-ttu-id="2d68e-109">С помощью окна **Подбор запасов**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-109">With the **Inventory Pick** window.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d68e-110">Складские подборы также учитывают отрицательные операции в главной книге как потребление товаров и поддерживаются только для производственных компонентов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-110">Inventory picks also post negative item ledger entries as consumption and are only supported for production components.</span></span> <span data-ttu-id="2d68e-111">Дополнительные сведения см. в окне Подбор запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-111">For more information, see the Inventory Pick window.</span></span>  

<span data-ttu-id="2d68e-112">Дополнительные сведения о перемещениях запасов см. в окне Перемещение запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-112">For detailed information about inventory movements, see the Inventory Movement window.</span></span>  

<span data-ttu-id="2d68e-113">Две различных роли могут создать первоначальное перемещение запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-113">Two different roles can create the initial inventory movement.</span></span> <span data-ttu-id="2d68e-114">Работник отдела сборки, например, может создать его из выпущенного сборочного заказа таким образом, чтобы он отображался в списке предстоящих работ работника склада.</span><span class="sxs-lookup"><span data-stu-id="2d68e-114">An assembly worker, for example, can create it from a released assembly order so that it shows up in the warehouse worker’s list of work to do.</span></span> <span data-ttu-id="2d68e-115">Чтобы создать перемещение запасов для строк сборочного заказа, подготовленных для того, чтобы переместить компоненты к конкретным ячейкам, работник по сборке использует функцию **Создать перемещение запасов**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-115">To create an inventory movement for assembly order lines that are ready to have components moved to their specified bins, the assembly worker uses the **Create Inventory Movement** function.</span></span>  

<span data-ttu-id="2d68e-116">В качестве альтернативы работник склада может создать его, указав требуемый выпущенный сборочный заказ.</span><span class="sxs-lookup"><span data-stu-id="2d68e-116">Alternatively, a warehouse worker can create it by pointing to the released assembly order in question.</span></span> <span data-ttu-id="2d68e-117">Это описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="2d68e-117">This is described in the following procedure.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d68e-118">Если перемещения предназначено для сборочного заказа, в котором товар собран для заказа на продажу, то можно указать, что при создании документа подбора, который берет собранный товар и учитывает отгрузку, автоматически создается документ перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-118">If the movement is for an assembly order where the item is assembled to a sales order, then you can define that the inventory movement document is automatically created when you create the inventory pick document that takes the finished assembly item and posts the shipment.</span></span> <span data-ttu-id="2d68e-119">Чтобы настроить это, выберите поле **Создавать перемещения автоматически** в окне **Настройка сборки**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-119">To set this up, select the **Create Movements Automatically** field in the **Assembly Setup** window</span></span>  
>   
>  <span data-ttu-id="2d68e-120">Дополнительные сведения о сборочных заказах и базовых конфигурациях склада см. в пункте "Обработка сборок на заказ с подборками запасов" см. в разделе [Подбор для производства или сборки](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="2d68e-120">For more information about assembly orders and basic warehouse configurations, see the "Handling Assemble-to-Order Items with Inventory Picks" section in [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  

<span data-ttu-id="2d68e-121">Эта процедура описывает способ создания перемещения запасов из окна **Перемещение запасов** путем отсылки к выпущенному сборочному заказу как документу-источнику.</span><span class="sxs-lookup"><span data-stu-id="2d68e-121">This procedure shows how to create an inventory movement from the **Inventory Movement** window by referencing a released assembly order as a source document.</span></span> <span data-ttu-id="2d68e-122">Процедура такая же, как при перемещении компонентов для производственных заказов и сервисных заказов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-122">The procedure is the same when you move components for production orders and service orders.</span></span>  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a><span data-ttu-id="2d68e-123">Перемещение компонентов в производственную зону в основных конфигурациях склада</span><span class="sxs-lookup"><span data-stu-id="2d68e-123">To move components to an operation area in basic warehouse configurations</span></span>  
1.  <span data-ttu-id="2d68e-124">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Перемещение запасов**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="2d68e-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Movement**, and choose the relevant link.</span></span>  
2.  <span data-ttu-id="2d68e-125">На экспресс-вкладке **Общее** заполните поле **Номер**</span><span class="sxs-lookup"><span data-stu-id="2d68e-125">On the **General** FastTab, fill in the **No.**</span></span> <span data-ttu-id="2d68e-126">.</span><span class="sxs-lookup"><span data-stu-id="2d68e-126">field.</span></span> <span data-ttu-id="2d68e-127">Можно нажать клавишу "Ввод", чтобы выбрать серии номеров.</span><span class="sxs-lookup"><span data-stu-id="2d68e-127">You can press the Enter key  to select from the number series.</span></span>  
3.  <span data-ttu-id="2d68e-128">В поле **Код склада** введите склад, где происходит перемещение.</span><span class="sxs-lookup"><span data-stu-id="2d68e-128">In the **Location Code** field, enter the location where the movement occurs.</span></span>  
4.  <span data-ttu-id="2d68e-129">Выберите действие **Получить исходные документы**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-129">Choose the **Get Source Documents** action.</span></span> <span data-ttu-id="2d68e-130">В качестве альтернативы заполните поле **Документ-источник**, а затем нажмите кнопку **AssistEdit** в поле **Номер источника**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-130">Alternatively, fill in the **Source Document** field, and then choose the **AssistEdit** button in the **Source No.** field.</span></span>  
5.  <span data-ttu-id="2d68e-131">В окне **Документы-источники** выберите сборочный заказ, для которого требуется переместить компоненты, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-131">In the **Source Documents** window, select the assembly order that you want to move components for, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="2d68e-132">Для каждого необходимого компонента, который можно переместить, в окне **Перемещения запасов** формируются одна строка "Взять" и одна строка "Поместить".</span><span class="sxs-lookup"><span data-stu-id="2d68e-132">For each needed component that can be moved, one Take line and one Place line are generated in the **Inventory Movements** window.</span></span> <span data-ttu-id="2d68e-133">Все поля, за исключением поля **Кол-во для обработки**, предварительно заполняются в соответствии со строками документа-источника.</span><span class="sxs-lookup"><span data-stu-id="2d68e-133">All fields except the **Qty. to Handle** field are prefilled according to the source document lines.</span></span> <span data-ttu-id="2d68e-134">В поле **Кол-во для обработки** находится нулевое значение, пока не будет введено фактическое перемещенное количество.</span><span class="sxs-lookup"><span data-stu-id="2d68e-134">The **Qty. to Handle** field is set to zero until you enter the quantity that you have actually moved.</span></span>  

    <span data-ttu-id="2d68e-135">Можно изменять код ячейки в строке "Поместить", но только в соответствии с наличием.</span><span class="sxs-lookup"><span data-stu-id="2d68e-135">You can change the bin code on a Take line but only according to availability.</span></span> <span data-ttu-id="2d68e-136">При выборе кнопки **AssistEdit** в поле **Код ячейки** строки "Взять" откроется окно **Содержимое ячейки**, в котором отображаются только ячейки с доступным компонентом.</span><span class="sxs-lookup"><span data-stu-id="2d68e-136">If you choose the **AssistEdit** button in the **Bin Code** field on a Take line, then the **Bin Contents** window opens and only shows bins where the component is available.</span></span>  

    <span data-ttu-id="2d68e-137">Нельзя изменить код ячейки в строке размещения.</span><span class="sxs-lookup"><span data-stu-id="2d68e-137">You cannot change the bin code on a Place line.</span></span> <span data-ttu-id="2d68e-138">Принимается только код ячейки, которой указан в строке компонента документа-источника.</span><span class="sxs-lookup"><span data-stu-id="2d68e-138">Only the bin code that is defined on the component line of the source document is accepted.</span></span> <span data-ttu-id="2d68e-139">Поддерживается принцип, что роль, запрашивающая компонент (работник отдела сборки в рамках этой процедуры), знает, где должен быть размещен этот компонент.</span><span class="sxs-lookup"><span data-stu-id="2d68e-139">This supports the principle that the role who requests a component, which is an assembly worker in this procedure, knows where the component must be placed.</span></span> <span data-ttu-id="2d68e-140">Если нужно настроить компоненты в другой ячейке, то сначала нужно изменить код ячейки в строке компонента, а затем повторно создать строки перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-140">If you want to place the components in a different bin, then you must first change the bin code on the component line and then re-create the inventory movement lines.</span></span>  
6.  <span data-ttu-id="2d68e-141">В поле **Кол-во для обработки** полное или частичное количество, которое реально перемещено.</span><span class="sxs-lookup"><span data-stu-id="2d68e-141">In the **Qty. to Handle** field, enter the full or partial quantity that you have actually moved.</span></span> <span data-ttu-id="2d68e-142">Значения в строках "Взять" и "Поместить" должны быть равными.</span><span class="sxs-lookup"><span data-stu-id="2d68e-142">The value on the Take and the Place lines must be the same.</span></span> <span data-ttu-id="2d68e-143">В противном случае невозможно зарегистрировать передвижение.</span><span class="sxs-lookup"><span data-stu-id="2d68e-143">Otherwise, you cannot register the movement.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2d68e-144">Как и в других складских операциях, можно разделить строку места, выбрав действие **Действия**, затем выберите действие **Разделить строку**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-144">As in other warehouse activities, you can split the Place line by selecting the **Actions** action and then choosing the **Split Line** action.</span></span> <span data-ttu-id="2d68e-145">В этом случае сумма двух разделенных строк "Место" должна равняться количеству в строке "Взять".</span><span class="sxs-lookup"><span data-stu-id="2d68e-145">In that case, the sum of the two split Place lines must equal the quantity on the Take line.</span></span>  

7.  <span data-ttu-id="2d68e-146">Когда все будет готово к регистрации выполненных перемещений, выберите действие **Товарный регистр Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="2d68e-146">When you are ready to register the movements that you have performed, choose the **Register Invt. Movement** action.</span></span>  

    <span data-ttu-id="2d68e-147">Создаются складские операции, отражающие, что компоненты теперь размещены в ячейках, указанных в строках сборочного заказа.</span><span class="sxs-lookup"><span data-stu-id="2d68e-147">Warehouse entries are created reflecting that the components now exist in the bins specified on the assembly order lines.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2d68e-148">В отличие перемещения компонентов со складским подбором потребление не учитывается при регистрации перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="2d68e-148">Unlike when you move components with an inventory pick, consumption is not posted when you register an inventory movement.</span></span> <span data-ttu-id="2d68e-149">Этот шаг должен быть выполнен отдельно с помощью учета результата сборочного заказа и потребления.</span><span class="sxs-lookup"><span data-stu-id="2d68e-149">That step must be performed separately by posting the assembly order output and consumption.</span></span> <span data-ttu-id="2d68e-150">Дополнительные сведения см. в разделе Заказ на сборку.</span><span class="sxs-lookup"><span data-stu-id="2d68e-150">For more information, see Assembly Order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d68e-151">См. также</span><span class="sxs-lookup"><span data-stu-id="2d68e-151">See Also</span></span>  
[<span data-ttu-id="2d68e-152">Управление складом</span><span class="sxs-lookup"><span data-stu-id="2d68e-152">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2d68e-153">Наличие</span><span class="sxs-lookup"><span data-stu-id="2d68e-153">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2d68e-154">[Настройка управления складом](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2d68e-154">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2d68e-155">[Управление сборкой](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2d68e-155">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2d68e-156">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="2d68e-156">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2d68e-157">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d68e-157">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
