---
title: "Как преобразовать существующие местоположения в размещения для складов | Документы Майкрософт"
description: "Существующее расположение инвентарного учета можно настроить на использование зон и ячеек и функционирование в качестве склада."
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
ms.openlocfilehash: e519a1628342f7c4711b3266f53ac857d4865e71
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a><span data-ttu-id="03a1c-103">Преобразование существующих местоположений в размещения для складов</span><span class="sxs-lookup"><span data-stu-id="03a1c-103">Convert Existing Locations to Warehouse Locations</span></span>
<span data-ttu-id="03a1c-104">Существующее расположение инвентарного учета можно настроить на использование зон и ячеек и функционирование в качестве склада.</span><span class="sxs-lookup"><span data-stu-id="03a1c-104">You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.</span></span>  

<span data-ttu-id="03a1c-105">Пакетное задание, предназначенное для включения функционирования расположения в качестве склада, создает исходные складские операции для ячейки коррекции склада по всем товарам, для которых зафиксировано наличие в данном расположении.</span><span class="sxs-lookup"><span data-stu-id="03a1c-105">The batch job to enable a location for warehouse operation creates initial warehouse entries for the warehouse adjustment bin for all items that have inventory in the location.</span></span> <span data-ttu-id="03a1c-106">Эти начальные операции балансируются при вводе операций товарного журнала склада после выполнения пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="03a1c-106">These initial entries will be balanced when warehouse physical inventory entries are entered after the batch job is run.</span></span>  

<span data-ttu-id="03a1c-107">Зоны и ячейки могут быть созданы до или после преобразования.</span><span class="sxs-lookup"><span data-stu-id="03a1c-107">You can create zones and bins either before or after the conversion.</span></span> <span data-ttu-id="03a1c-108">Перед преобразованием должна быть создана единственная ячейка, которая будет служить в качестве ячейки коррекции.</span><span class="sxs-lookup"><span data-stu-id="03a1c-108">The only bin that you must create before the conversion is the one that is to be used as the future adjustment bin.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="03a1c-109">Чтобы очистить все запасы с отрицательным значением и открытые складские документы, прежде чем изменить местоположение для складской обработки, создайте отчет для выявления на этом складе товаров с отрицательным значением и открытых складских документов.</span><span class="sxs-lookup"><span data-stu-id="03a1c-109">To clear all negative inventory and any open warehouse documents before you convert the location for warehouse handling, run a report to identify the items with negative inventory and open warehouse documents for the location.</span></span> <span data-ttu-id="03a1c-110">Дополнительные сведения см. в разделе Проверка на отрицательные остатки.</span><span class="sxs-lookup"><span data-stu-id="03a1c-110">For more information, see Check on Negative Inventory.</span></span>  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><span data-ttu-id="03a1c-111">Включение функционирования существующего расположения в качестве складской площадки</span><span class="sxs-lookup"><span data-stu-id="03a1c-111">To enable an existing location to operate as a warehouse location</span></span>  
1.  <span data-ttu-id="03a1c-112">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Создать склад**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="03a1c-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Warehouse Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="03a1c-113">В поле **Код склада** укажите местоположение, которое требуется включить для обработки склада.</span><span class="sxs-lookup"><span data-stu-id="03a1c-113">In the **Location Code** field, specify the location that you want to enable for warehouse processing.</span></span>  
3.  <span data-ttu-id="03a1c-114">В поле **Код ячейки коррекции** укажите ячейку на складе, где хранятся несинхронизированные складские операции.</span><span class="sxs-lookup"><span data-stu-id="03a1c-114">In the **Adjustment Bin Code** field, specify the bin at the location where unsynchronized warehouse entries are stored.</span></span> <span data-ttu-id="03a1c-115">Дополнительные сведения см. в пункте "Синхронизация скорректированных складских операций с соответствующими операциями книги товаров" в разделе [Подсчет, корректировка и повторная классификация запасов](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="03a1c-115">For more information, see the "To synchronize the adjusted warehouse entries with the related item ledger entries" section in [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

    <span data-ttu-id="03a1c-116">С помощью открытых операций книги товаров для заданного расположения создаются строки складского журнала, в которых суммируется каждая комбинация значений "Код товара", "Код варианта", "Код единицы измерения" и, в случае необходимости, "Номер партии" и "Серийный номер" журнала учтенных товарных операций.</span><span class="sxs-lookup"><span data-stu-id="03a1c-116">Using the open item ledger entries for the specified location, warehouse journal lines are created that sum up every combination of Item No., Variant Code, Unit of Measure Code, and, if necessary, Lot No. and Serial No. in the item ledger entries.</span></span> <span data-ttu-id="03a1c-117">Затем эти строки складского журнала учитываются.</span><span class="sxs-lookup"><span data-stu-id="03a1c-117">The warehouse journal lines are then posted.</span></span> <span data-ttu-id="03a1c-118">При выполнении этого учета создаются складские операции, выполняющие занесение остатков в ячейку коррекции склада.</span><span class="sxs-lookup"><span data-stu-id="03a1c-118">This posting creates warehouse entries that place the inventory in the warehouse adjustment bin.</span></span> <span data-ttu-id="03a1c-119">Кроме того, в карточку склада записывается **Код ячейки коррекции**.</span><span class="sxs-lookup"><span data-stu-id="03a1c-119">The **Adjustment Bin Code** on the location card is also set.</span></span>  

4.  <span data-ttu-id="03a1c-120">Чтобы просмотреть товары, добавленные к ячейке коррекции пакетным заданием, можно запустить отчет **Складская ячейка коррекции**.</span><span class="sxs-lookup"><span data-stu-id="03a1c-120">To see which items were added to the adjustment bin during the batch job, run the **Warehouse Adjustment Bin** report.</span></span>  
5.  <span data-ttu-id="03a1c-121">По завершении работы пакетного задания **Создать склад** необходимо произвести и учесть инвентаризацию на складе.</span><span class="sxs-lookup"><span data-stu-id="03a1c-121">When the **Create Warehouse Location** batch job has completed, perform and post a warehouse physical inventory.</span></span> <span data-ttu-id="03a1c-122">Дополнительные сведения см. в разделе [Подсчет, корректировка и повторная классификация запасов](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="03a1c-122">For more information, see [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="03a1c-123">Для запуска пакетного задания **Создать склад** рекомендуется выбирать время, когда это не будет мешать основной работе в системе.</span><span class="sxs-lookup"><span data-stu-id="03a1c-123">It is recommended that you run the **Create Warehouse Location** batch job at a time when it will not impact the daily work in the system.</span></span> <span data-ttu-id="03a1c-124">Это задание обрабатывает каждую операцию в таблице **Операции книги товаров**, и если таких операций много, их обработка может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="03a1c-124">This job processes each entry in the **Item Ledger Entry** table, and if there are a large number of item ledger entries, the job can last several hours.</span></span>  

 <span data-ttu-id="03a1c-125">Для расположений, в которых до преобразования не использовались документы управления складом, перед преобразованием необходимо повторно открыть и освободить все исходные документы, в которых содержится частично учтенная приемка или отгрузка.</span><span class="sxs-lookup"><span data-stu-id="03a1c-125">For those locations that did not use warehouse management documents before the conversion, you must re-open and release any source documents that were partially received or partially shipped before the conversion.</span></span>  

## <a name="see-also"></a><span data-ttu-id="03a1c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="03a1c-126">See Also</span></span>  
[<span data-ttu-id="03a1c-127">Управление складом</span><span class="sxs-lookup"><span data-stu-id="03a1c-127">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="03a1c-128">Наличие</span><span class="sxs-lookup"><span data-stu-id="03a1c-128">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="03a1c-129">[Настройка управления складом](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="03a1c-129">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="03a1c-130">[Управление сборкой](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="03a1c-130">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="03a1c-131">Сведения о проектировании: управление складом</span><span class="sxs-lookup"><span data-stu-id="03a1c-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="03a1c-132">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03a1c-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
