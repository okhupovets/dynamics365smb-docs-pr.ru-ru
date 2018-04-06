---
title: "Сведения о проектировании — доступность трассировки товара | Microsoft Docs"
description: "В окнах **Строки трассировки товаров** и **Сводка по трассировке товара** содержатся динамические сведения о наличии серийных номеров или номеров партий. Цель этого элемента — повышение прозрачности исходящих документов для пользователей, например заказов на продажу, путем отображения серийных номеров или сведений о том, сколько единиц товара с определенным номером партии в настоящее время назначено в других открытых документах. Это уменьшает неопределенность, вызванную двойным распределением, и вселяет уверенность в специалистов по обработке заказов, что номера трассировки товаров и даты, обещанные на неучтенных заказах продажи, могут быть выполнены."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a58bd4ccc8f31ef0d90bf27f3a89e98bcdb56fe4
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-availability"></a><span data-ttu-id="b42f8-105">Сведения о проектировании: доступность трассировки товара</span><span class="sxs-lookup"><span data-stu-id="b42f8-105">Design Details: Item Tracking Availability</span></span>
<span data-ttu-id="b42f8-106">В окнах **Строки трассировки товаров** и **Сводка по трассировке товара** содержатся динамические сведения о наличии серийных номеров или номеров партий.</span><span class="sxs-lookup"><span data-stu-id="b42f8-106">The **Item Tracking Lines** and **Item Tracking Summary** windows provide dynamic availability information for serial or lot numbers.</span></span> <span data-ttu-id="b42f8-107">Цель этого элемента — повышение прозрачности исходящих документов для пользователей, например заказов на продажу, путем отображения серийных номеров или сведений о том, сколько единиц товара с определенным номером партии в настоящее время назначено в других открытых документах.</span><span class="sxs-lookup"><span data-stu-id="b42f8-107">The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.</span></span> <span data-ttu-id="b42f8-108">Это уменьшает неопределенность, вызванную двойным распределением, и вселяет уверенность в специалистов по обработке заказов, что номера трассировки товаров и даты, обещанные на неучтенных заказах продажи, могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="b42f8-108">This reduces uncertainty that is caused by double allocation and instills confidence in order processors that the item tracking numbers and dates that they are promising on unposted sales orders can be fulfilled.</span></span> <span data-ttu-id="b42f8-109">Дополнительные сведения см. в разделе [Сведения о проектировании: окно "Строки трассировки товаров"](design-details-item-tracking-lines-window.md).</span><span class="sxs-lookup"><span data-stu-id="b42f8-109">For more information, see [Design Details: Item Tracking Lines Window](design-details-item-tracking-lines-window.md).</span></span>  

 <span data-ttu-id="b42f8-110">При открытии окна **Строки трассировки товаров** данные о доступности извлекаются из таблицы **Операция журнала товаров** и таблицы **Операция резервирования** без фильтра дат.</span><span class="sxs-lookup"><span data-stu-id="b42f8-110">When you open the **Item Tracking Lines** window, availability data is retrieved from the **Item Ledger Entry** table and the **Reservation Entry** table, with no date filter.</span></span> <span data-ttu-id="b42f8-111">При выборе поля **Серийный номер** или **Номер партии** открывается окно **Сводка по трассировке товара** и показывается сводка информации о трассировке товаров в таблице **Операция резервирования**.</span><span class="sxs-lookup"><span data-stu-id="b42f8-111">When you choose the **Serial No.** field or the **Lot No.** field, the **Item Tracking Summary** window opens and shows a summary of the item tracking information in the **Reservation Entry** table.</span></span> <span data-ttu-id="b42f8-112">Сводка содержит следующие сведения о каждом из серийных номеров или номеров партии в строке трассировки товаров.</span><span class="sxs-lookup"><span data-stu-id="b42f8-112">The summary contains the following information about each serial or lot number on the item tracking line:</span></span>  

|<span data-ttu-id="b42f8-113">Поле</span><span class="sxs-lookup"><span data-stu-id="b42f8-113">Field</span></span>|<span data-ttu-id="b42f8-114">Описанием</span><span class="sxs-lookup"><span data-stu-id="b42f8-114">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="b42f8-115">**Всего (кол-во)**</span><span class="sxs-lookup"><span data-stu-id="b42f8-115">**Total Quantity**</span></span>|<span data-ttu-id="b42f8-116">Общее количество номера партии или серийного номера, находящееся в настоящий момент в запасах.</span><span class="sxs-lookup"><span data-stu-id="b42f8-116">The total quantity of the serial or lot number that is currently in inventory.</span></span>|  
|<span data-ttu-id="b42f8-117">**Общее требуемое кол-во**</span><span class="sxs-lookup"><span data-stu-id="b42f8-117">**Total Requested Quantity**</span></span>|<span data-ttu-id="b42f8-118">Общее количество номера партии или серийного номера, запрошенное в настоящий момент во всех документах.</span><span class="sxs-lookup"><span data-stu-id="b42f8-118">The total quantity of the serial or lot number that is currently requested in all documents.</span></span>|  
|<span data-ttu-id="b42f8-119">**Текущее незаверш. количество**</span><span class="sxs-lookup"><span data-stu-id="b42f8-119">**Current Pending Quantity**</span></span>|<span data-ttu-id="b42f8-120">Количество, вводимое в текущем экземпляре окна **Строки трассировки товаров**, но еще не подтвержденное в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b42f8-120">The quantity that is entered in the current instance of the **Item Tracking Lines** window but is not yet committed to the database.</span></span>|  
|<span data-ttu-id="b42f8-121">**Общее доступное кол-во**</span><span class="sxs-lookup"><span data-stu-id="b42f8-121">**Total Available Quantity**</span></span>|<span data-ttu-id="b42f8-122">Количество серийных номеров или номеров партий, доступное для запроса пользователем.</span><span class="sxs-lookup"><span data-stu-id="b42f8-122">The quantity of the serial or lot number that is available for the user to request.</span></span><br /><br /> <span data-ttu-id="b42f8-123">Это количество вычисляется из других полей в окне следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b42f8-123">This quantity is calculated from other fields in the window as follows:</span></span><br /><br /> <span data-ttu-id="b42f8-124">общее количество - (общее запрошенное количество + текущее ожидающее количество).</span><span class="sxs-lookup"><span data-stu-id="b42f8-124">total quantity – (total requested quantity + current pending quantity).</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="b42f8-125">Информацию также можно просматривать в предыдущей таблице, используя функцию **Выбрать операции** в окне **Строки трассировки товаров**.</span><span class="sxs-lookup"><span data-stu-id="b42f8-125">You can also see the information in the preceding table by using the **Select Entries** function in the **Item Tracking Lines** window.</span></span>  

 <span data-ttu-id="b42f8-126">Для сохранения производительности базы данных данные о доступности извлекаются из базы данных однократно при открытии окна **Строки трассировки товаров** и при использовании функции **Обновить наличие** в окне.</span><span class="sxs-lookup"><span data-stu-id="b42f8-126">To preserve database performance, availability data is only retrieved once from the database when you open the **Item Tracking Lines** window and when you use the **Refresh Availability** function in the window.</span></span>  

## <a name="calculation-formula"></a><span data-ttu-id="b42f8-127">Формула расчета</span><span class="sxs-lookup"><span data-stu-id="b42f8-127">Calculation Formula</span></span>  
 <span data-ttu-id="b42f8-128">Как описано в таблице выше, наличие определенного серийного номера или номера партии рассчитывается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b42f8-128">As described in the preceding table, the availability of a given serial or lot number is calculated as follows.</span></span>  

 <span data-ttu-id="b42f8-129">общее доступное кол-во = кол-во на складе – (все требования + количество, еще не зафиксированное в базе данных)</span><span class="sxs-lookup"><span data-stu-id="b42f8-129">total available quantity = quantity in inventory – (all demands + quantity not yet committed to the database)</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="b42f8-130">Эта формула подразумевает, что при вычислении доступности серийного номера или номера партии учитываются только запасы, а прогнозированные приемки — нет.</span><span class="sxs-lookup"><span data-stu-id="b42f8-130">This formula implies that the serial or lot number availability calculation considers only inventory and ignores projected receipts.</span></span> <span data-ttu-id="b42f8-131">Соответственно, поставка, которая еще не учтена в запасах, не влияет на наличие трассировки товаров в отличие от обычного наличия товаров, включающего прогнозируемый приход.</span><span class="sxs-lookup"><span data-stu-id="b42f8-131">Accordingly, supply that is not yet posted to inventory does not affect item tracking availability, as opposed to regular item availability where projected receipts are included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b42f8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b42f8-132">See Also</span></span>  
 [<span data-ttu-id="b42f8-133">Сведения о проектировании: трассировка товара</span><span class="sxs-lookup"><span data-stu-id="b42f8-133">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)
