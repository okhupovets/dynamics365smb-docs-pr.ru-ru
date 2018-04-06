---
title: "Пошаговое руководство. Получение и складирование в базовых конфигурациях склада | Microsoft Docs"
description: "В Business Central входящие процессы по получению и размещению могут быть выполнены четырьмя способами при помощи различных функций в зависимости от уровня сложности склада."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1b6b57448264bddee9bdfc4a81a2f926a7938c7
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="3bc20-103">Пошаговое руководство. Получение и складирование в базовых конфигурациях склада</span><span class="sxs-lookup"><span data-stu-id="3bc20-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>
<span data-ttu-id="3bc20-104">В [!INCLUDE[d365fin](includes/d365fin_md.md)] входящие процессы по получению и размещению могут быть выполнены четырьмя способами при помощи различных функций в зависимости от уровня сложности склада.</span><span class="sxs-lookup"><span data-stu-id="3bc20-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="3bc20-105">Метод</span><span class="sxs-lookup"><span data-stu-id="3bc20-105">Method</span></span>|<span data-ttu-id="3bc20-106">Входящий процесс</span><span class="sxs-lookup"><span data-stu-id="3bc20-106">Inbound process</span></span>|<span data-ttu-id="3bc20-107">Ячейки</span><span class="sxs-lookup"><span data-stu-id="3bc20-107">Bins</span></span>|<span data-ttu-id="3bc20-108">Прих. накладные</span><span class="sxs-lookup"><span data-stu-id="3bc20-108">Receipts</span></span>|<span data-ttu-id="3bc20-109">Складское размещение</span><span class="sxs-lookup"><span data-stu-id="3bc20-109">Put-aways</span></span>|<span data-ttu-id="3bc20-110">Уровень сложности (см. раздел [Сведения о проектировании: настройка склада](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="3bc20-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="3bc20-111">П</span><span class="sxs-lookup"><span data-stu-id="3bc20-111">A</span></span>|<span data-ttu-id="3bc20-112">Выполните учет приемки и размещения из строки заказа</span><span class="sxs-lookup"><span data-stu-id="3bc20-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="3bc20-113">X</span><span class="sxs-lookup"><span data-stu-id="3bc20-113">X</span></span>|||<span data-ttu-id="3bc20-114">2</span><span class="sxs-lookup"><span data-stu-id="3bc20-114">2</span></span>|  
|<span data-ttu-id="3bc20-115">Б</span><span class="sxs-lookup"><span data-stu-id="3bc20-115">B</span></span>|<span data-ttu-id="3bc20-116">Выполните учет приемки и размещения из документа складского размещения</span><span class="sxs-lookup"><span data-stu-id="3bc20-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="3bc20-117">X</span><span class="sxs-lookup"><span data-stu-id="3bc20-117">X</span></span>|<span data-ttu-id="3bc20-118">3</span><span class="sxs-lookup"><span data-stu-id="3bc20-118">3</span></span>|  
|<span data-ttu-id="3bc20-119">C</span><span class="sxs-lookup"><span data-stu-id="3bc20-119">C</span></span>|<span data-ttu-id="3bc20-120">Выполните учет приемки и размещения из документа складской приемки</span><span class="sxs-lookup"><span data-stu-id="3bc20-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="3bc20-121">X</span><span class="sxs-lookup"><span data-stu-id="3bc20-121">X</span></span>||<span data-ttu-id="3bc20-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="3bc20-122">4/5/6</span></span>|  
|<span data-ttu-id="3bc20-123">D</span><span class="sxs-lookup"><span data-stu-id="3bc20-123">D</span></span>|<span data-ttu-id="3bc20-124">Выполните учет приемки из документа складской приемки и учет размещения из документа складского размещения</span><span class="sxs-lookup"><span data-stu-id="3bc20-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="3bc20-125">X</span><span class="sxs-lookup"><span data-stu-id="3bc20-125">X</span></span>|<span data-ttu-id="3bc20-126">X</span><span class="sxs-lookup"><span data-stu-id="3bc20-126">X</span></span>|<span data-ttu-id="3bc20-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="3bc20-127">4/5/6</span></span>|  

<span data-ttu-id="3bc20-128">Дополнительные сведения см. в разделе [Сведения о проектировании: входящий складской поток](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="3bc20-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="3bc20-129">В следующем пошаговом руководстве показан метод B в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="3bc20-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="3bc20-130">Об этом пошаговом руководстве</span><span class="sxs-lookup"><span data-stu-id="3bc20-130">About This Walkthrough</span></span>  
<span data-ttu-id="3bc20-131">В базовых конфигурациях склада, если настройки склада таковы, что требуется обработка размещения, но не требуется обработка приемки, то для регистрации и учета информации о размещении и приемке для входящих документов-источников следует использовать окно **Размещение запасов**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** window to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="3bc20-132">Входящим документом-источником может быть заказ на покупку, заказ на возврат продажи, входящий заказ на перемещение или производственный заказ, готовая продукция которого готова для размещения.</span><span class="sxs-lookup"><span data-stu-id="3bc20-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="3bc20-133">Хотя эти параметры называются **Требуется подбор** и **Требуется размещение**, все равно можно учитывать приходы и отгрузки непосредственно из исходных бизнес-документов на складах, для которых установлены эти флажки.</span><span class="sxs-lookup"><span data-stu-id="3bc20-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="3bc20-134">В этом пошаговом руководстве демонстрируются следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="3bc20-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="3bc20-135">Настройка склада "СЕРЕБРЯНЫЙ" для размещений.</span><span class="sxs-lookup"><span data-stu-id="3bc20-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="3bc20-136">Настройка склада "СЕРЕБРЯНЫЙ" для обработки ячейки.</span><span class="sxs-lookup"><span data-stu-id="3bc20-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="3bc20-137">Определение стандартной ячейки для товара LS-81.</span><span class="sxs-lookup"><span data-stu-id="3bc20-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="3bc20-138">(LS-75 уже настроен в CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="3bc20-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="3bc20-139">Создание заказа на покупку для поставщика 10000 на 40 громкоговорителей.</span><span class="sxs-lookup"><span data-stu-id="3bc20-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="3bc20-140">Проверка соответствия ячеек складирования настройкам.</span><span class="sxs-lookup"><span data-stu-id="3bc20-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="3bc20-141">Выпуск заказа на покупку для обработки на складе.</span><span class="sxs-lookup"><span data-stu-id="3bc20-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="3bc20-142">Создание складского размещения на основании выпущенного документа-источника.</span><span class="sxs-lookup"><span data-stu-id="3bc20-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="3bc20-143">Удостоверьтесь, что ячейки складирования наследуются из заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="3bc20-144">Регистрация складского перемещения в склад с одновременным учетом приходной накладной покупки для исходного заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="3bc20-145">Роли</span><span class="sxs-lookup"><span data-stu-id="3bc20-145">Roles</span></span>  
<span data-ttu-id="3bc20-146">В этом пошаговом руководстве демонстрируются задачи, выполняемые исполнителями следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="3bc20-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="3bc20-147">Заведующий складом</span><span class="sxs-lookup"><span data-stu-id="3bc20-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="3bc20-148">Агент по закупкам</span><span class="sxs-lookup"><span data-stu-id="3bc20-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="3bc20-149">Работник склада</span><span class="sxs-lookup"><span data-stu-id="3bc20-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="3bc20-150">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="3bc20-150">Prerequisites</span></span>  
<span data-ttu-id="3bc20-151">Для выполнения данного пошагового руководства необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3bc20-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="3bc20-152">Установлен "Cronus Россия ЗАО".</span><span class="sxs-lookup"><span data-stu-id="3bc20-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="3bc20-153">Чтобы назначить себя работником СЕРЕБРЯНОГО склада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3bc20-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="3bc20-154">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Сотрудники склада**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-154">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="3bc20-155">Выберите поле **ИД пользователя** и укажите свою учетную запись пользователя в окне **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-155">Choose the **User ID** field, and select your own user account in the **Users** window.</span></span>  
    3.  <span data-ttu-id="3bc20-156">В поле **Код склада** введите "СЕРЕБР".</span><span class="sxs-lookup"><span data-stu-id="3bc20-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="3bc20-157">Выберите поле **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="3bc20-158">Сюжет</span><span class="sxs-lookup"><span data-stu-id="3bc20-158">Story</span></span>  
<span data-ttu-id="3bc20-159">Элен, менеджер склада в CRONUS Россия ЗАО, создает заказ на покупку на 10 единиц товара LS-75 и 30 единиц товара LS-81 от поставщика 10000, которые должны быть доставлены на СЕРЕБРЯНЫЙ склад.</span><span class="sxs-lookup"><span data-stu-id="3bc20-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="3bc20-160">Когда товар будет доставлен на склад, работник склада Вадим убирает товары в стандартные ячейки, обозначенные для товаров.</span><span class="sxs-lookup"><span data-stu-id="3bc20-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="3bc20-161">Когда Вадим учитывает размещение, товары учитываются в запасах как полученные товары и доступны для продажи или других потребностей.</span><span class="sxs-lookup"><span data-stu-id="3bc20-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="3bc20-162">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="3bc20-162">Setting up the Location</span></span>  
 <span data-ttu-id="3bc20-163">Настройка окна **Карточка склада** определяет потоки склада организации.</span><span class="sxs-lookup"><span data-stu-id="3bc20-163">The setup of the **Location Card** window defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="3bc20-164">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="3bc20-164">To set up the location</span></span>  

1.  <span data-ttu-id="3bc20-165">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Склады**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3bc20-166">Откройте карточку склада СЕРЕБРЯНЫЙ.</span><span class="sxs-lookup"><span data-stu-id="3bc20-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="3bc20-167">Установите флажок **Требуется размещение**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="3bc20-168">Перейти к настройке стандартной ячейки для двух кодов товара с целью контроля, где они размещаются.</span><span class="sxs-lookup"><span data-stu-id="3bc20-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="3bc20-169">Выберите действие **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="3bc20-170">Выберите первую строку, для ячейки S-01-0001, а затем выберите действие **Содержимое**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="3bc20-171">Обратите внимание, что товар LS-75 уже настроен в качестве содержимого в ячейке S-01-0001 в окне **Содержимое ячейки**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-171">Notice in the **Bin Content** window that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="3bc20-172">Выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="3bc20-173">Выберите поля **Фиксир.** и **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="3bc20-174">В поле **Номер товара** введите LS-81.</span><span class="sxs-lookup"><span data-stu-id="3bc20-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="3bc20-175">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="3bc20-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="3bc20-176">Заказы на покупку — это наиболее распространенный тип входящего приходного документа.</span><span class="sxs-lookup"><span data-stu-id="3bc20-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="3bc20-177">Порядок создания заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="3bc20-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="3bc20-178">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Заказы на покупку**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-178">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3bc20-179">Выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="3bc20-180">Создайте заказ на покупку для поставщика 10000 на рабочую дату (23 января) со следующими строками заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="3bc20-181">Товар</span><span class="sxs-lookup"><span data-stu-id="3bc20-181">Item</span></span>|<span data-ttu-id="3bc20-182">Код склада</span><span class="sxs-lookup"><span data-stu-id="3bc20-182">Location code</span></span>|<span data-ttu-id="3bc20-183">Код ячейки</span><span class="sxs-lookup"><span data-stu-id="3bc20-183">Bin code</span></span>|<span data-ttu-id="3bc20-184">Количество</span><span class="sxs-lookup"><span data-stu-id="3bc20-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="3bc20-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="3bc20-185">LS_75</span></span>|<span data-ttu-id="3bc20-186">СЕРЕБР.</span><span class="sxs-lookup"><span data-stu-id="3bc20-186">SILVER</span></span>|<span data-ttu-id="3bc20-187">С-01-0001</span><span class="sxs-lookup"><span data-stu-id="3bc20-187">S-01-0001</span></span>|<span data-ttu-id="3bc20-188">10</span><span class="sxs-lookup"><span data-stu-id="3bc20-188">10</span></span>|  
    |<span data-ttu-id="3bc20-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="3bc20-189">LS-81</span></span>|<span data-ttu-id="3bc20-190">СЕРЕБР.</span><span class="sxs-lookup"><span data-stu-id="3bc20-190">SILVER</span></span>|<span data-ttu-id="3bc20-191">С-01-0001</span><span class="sxs-lookup"><span data-stu-id="3bc20-191">S-01-0001</span></span>|<span data-ttu-id="3bc20-192">30</span><span class="sxs-lookup"><span data-stu-id="3bc20-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="3bc20-193">Код ячейки вводится автоматически в соответствии с настройками в разделе "Настройка склада".</span><span class="sxs-lookup"><span data-stu-id="3bc20-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="3bc20-194">Перейти к уведомлению склада, что заказ на покупку готов для обработки на складе при поступлении товара.</span><span class="sxs-lookup"><span data-stu-id="3bc20-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="3bc20-195">Выберите действие **Выпустить**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="3bc20-196">Громкоговорители были доставлены от поставщика 10000 на СЕРЕБРЯНЫЙ склад, и Вадим начинает их размещать.</span><span class="sxs-lookup"><span data-stu-id="3bc20-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="3bc20-197">Приемка и размещение товаров</span><span class="sxs-lookup"><span data-stu-id="3bc20-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="3bc20-198">В окне **Размещение запасов** можно управлять всеми входящими складскими операциями для конкретного документа-источника, такого как заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-198">In the **Inventory Put-away** window, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="3bc20-199">Приемка и размещение товаров</span><span class="sxs-lookup"><span data-stu-id="3bc20-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="3bc20-200">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Размещения запасов**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-200">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3bc20-201">Выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="3bc20-202">Выберите поле **Документ-источник**, а затем выберите **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="3bc20-203">Выберите поле **Номер источника**, выберите строку для покупки у поставщика 10000, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="3bc20-204">В качестве альтернативы на вкладке **Действия** в группе **Функции** выберите **Получить источник документа**, а затем выберите заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="3bc20-204">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="3bc20-205">Выберите действие **Автозаполнение кол-ва для обработки**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="3bc20-206">В качестве альтернативы в поле **Кол-во для обработки** введите 10 и 30 соответственно в двух строках складского размещения.</span><span class="sxs-lookup"><span data-stu-id="3bc20-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="3bc20-207">Выберите действие **Учет**, выберите параметр **Получить** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3bc20-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="3bc20-208">Теперь 40 громкоговорителей зарегистрированы как размещенные в ячейке С-01-0001, и создана положительная операция товарной книги, отражающая учтенную приходную накладную покупки.</span><span class="sxs-lookup"><span data-stu-id="3bc20-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3bc20-209">См. также</span><span class="sxs-lookup"><span data-stu-id="3bc20-209">See Also</span></span>  
 <span data-ttu-id="3bc20-210">[Размещение товаров с помощью складского размещения](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="3bc20-211">[Настройка базовых складов с помощью зон операций](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="3bc20-212">[Перемещение компонентов в производственную зону в базовых конфигурациях склада](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="3bc20-213">[Подбор для производства или сборки](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="3bc20-214">[Перемещение специальных товаров в базовых конфигурациях склада](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="3bc20-215">[Сведения о проектировании: входящий складской поток](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="3bc20-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="3bc20-216">Пошаговые описания бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="3bc20-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="3bc20-217">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3bc20-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
