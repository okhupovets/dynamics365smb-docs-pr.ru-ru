---
title: "Как планировать складские перемещения в журналах | Документы Майкрософт"
description: "Перемещения планируются в журнале с использованием функции пополнения ячейки или путем планирования строк, необходимых для создания инструкций по передвижению, вручную."
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
ms.openlocfilehash: 0f518b96cb21a9637ae9b6e64e4c9e22a5fc6512
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="ad9cd-103">Планирование складских перемещений в журналах</span><span class="sxs-lookup"><span data-stu-id="ad9cd-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="ad9cd-104">Перемещения планируются в журнале с использованием функции пополнения ячейки или путем планирования строк, необходимых для создания инструкций по передвижению, вручную.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="ad9cd-105">Расчет передвижения для пополнения</span><span class="sxs-lookup"><span data-stu-id="ad9cd-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="ad9cd-106">По мере того, как склад отгружает товары клиентам, в ячейках с наибольшим рейтингом остается меньше и меньше товаров.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="ad9cd-107">Для того чтобы заполнить эти ячейки с высоким рейтингом товарами из других ячеек, используется функция **Расчет пополнения ячеек** в окне **Журнал перемещения**</span><span class="sxs-lookup"><span data-stu-id="ad9cd-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="ad9cd-108">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал перемещения**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ad9cd-109">Выберите действие **Расчет пополнения ячеек**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    <span data-ttu-id="ad9cd-110">В [!INCLUDE[d365fin](includes/d365fin_md.md)] создаются строки, которые точно указывают, каким образом товары из ячеек с более низким рейтингом перемещаются в ячейки с более высоким рейтингом.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-110">[!INCLUDE[d365fin](includes/d365fin_md.md)] creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ad9cd-111">Предлагается перемещение согласно методу FEFO при активации функции **Создать передвижение**, если для товара удовлетворяются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="ad9cd-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="ad9cd-112">Указан срок годности товара.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="ad9cd-113">Установлен флажок **Выбрать по методу FEFO** в карточке склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ad9cd-114">Установлен флажок **Ячейка обязательна** в карточке склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ad9cd-115">Поля **Из зоны** и **Из ячейки** пусты.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="ad9cd-116">Дополнительные сведения см. в разделе [Подбор по методу FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="ad9cd-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="ad9cd-117">Просмотрите строки и, при необходимости, выберите их или удалите некоторые из них, если нет времени обработать их все.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="ad9cd-118">Выберите действие **Создать передвижение**, чтобы создать складскую инструкцию для работников склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="ad9cd-119">Перемещение всего содержимого одной или нескольких ячеек с помощью функции "Получить содержимое ячейки"</span><span class="sxs-lookup"><span data-stu-id="ad9cd-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="ad9cd-120">Журнал перемещений используется также для планирования других перемещений товаров внутри склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="ad9cd-121">Например, если товар нужно поместить в ячейку для контроля качества, то для планирования этого действия можно воспользоваться журналом передвижений, а затем создать передвижение, чтобы сформировать инструкции для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="ad9cd-122">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал перемещения**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ad9cd-123">Выберите действие **Получить содержимое ячейки**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="ad9cd-124">С помощью окна запроса можно отфильтровать те ячейки и товары, которые должны быть отображены в строках журнала перемещений.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="ad9cd-125">Заполните соответствующие поля в окне запроса пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="ad9cd-126">Например, если требуется просмотреть содержимое всех ячеек определенной складской зоны, заполните поле **Код зоны**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="ad9cd-127">Если требуется получить строки для всех ячеек, содержащих определенный товар, заполните поле **Код товара**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ad9cd-128">Невозможно переместить вручную товары в ячейку или из нее, если у этой ячейки тип ПОЛУЧЕНИЕ, поскольку товары, находящиеся в ячейке с этим типом, должны быть зарегистрированы как размещенные до того, как станут частью доступных складских запасов.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="ad9cd-129">Если получено много строк, выберите **Сортировка**, чтобы определить способ сортировки для упорядочивания строк, отображаемых в журнале, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ad9cd-130">Строки перемещения извлекаются согласно методу FEFO при активации функции **Получить содержимое ячейки**, если для товара выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="ad9cd-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="ad9cd-131">Указан срок годности товара.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="ad9cd-132">Установлен флажок **Выбрать по методу FEFO** в карточке склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ad9cd-133">Установлен флажок **Ячейка обязательна** в карточке склада.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ad9cd-134">Поля **Из зоны** и **Из ячейки** пусты.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="ad9cd-135">Чтобы отразить изменения, которые предполагается сделать, внесите недостающую информацию в некоторые из полученных строк.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="ad9cd-136">Для каждого перемещаемого товара необходимо заполнить поля **Номер товара**, **Из кода ячейки**, **В код ячейки** и **Кол-во**.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="ad9cd-137">Удалите незаполненные строки, которые служили для информационных целей.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="ad9cd-138">Когда в строках журнала будут точно отражено, каким образом работник склада должен выполнять перемещение, выберите действие **Создать передвижение**, чтобы создать инструкции для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ad9cd-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ad9cd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ad9cd-139">See Also</span></span>  
[<span data-ttu-id="ad9cd-140">Управление складом</span><span class="sxs-lookup"><span data-stu-id="ad9cd-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ad9cd-141">Наличие</span><span class="sxs-lookup"><span data-stu-id="ad9cd-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ad9cd-142">[Настройка управления складом](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ad9cd-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ad9cd-143">[Управление сборкой](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ad9cd-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ad9cd-144">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="ad9cd-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ad9cd-145">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ad9cd-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
