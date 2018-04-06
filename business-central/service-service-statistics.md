---
title: "Сервисная статистика | Microsoft Docs"
description: "Получите быстрый обзор содержимого сервисного документа, такого как заказы, предложения, счета или кредит-ноты, сведения по конкретным строкам сервиса и сервисным товарам."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 73d0044308d619f92e0379cc7b678301c72ce31c
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---

# <a name="viewing-service-statistics"></a><span data-ttu-id="74633-103">Просмотр сервисной статистики</span><span class="sxs-lookup"><span data-stu-id="74633-103">Viewing Service Statistics</span></span>
<span data-ttu-id="74633-104">Financials может обеспечить определенную статистику, которую можно использовать для анализа сервисных документов и определения качества управления процессами сервиса.</span><span class="sxs-lookup"><span data-stu-id="74633-104">Financials can provide some statistics that you can use to analyze service documents and determine how well you are managing your service processes.</span></span> <span data-ttu-id="74633-105">Можно анализировать сервисные контракты, товары, предложения, заказы, счета и кредит-ноты, выбрав действия **Статистика**.</span><span class="sxs-lookup"><span data-stu-id="74633-105">You can analyze service contracts, items, quotes, orders, invoices, and credit memos by choosing the **Statistics** action.</span></span> <span data-ttu-id="74633-106">Для сервисных товаров и контрактов можно также использовать **Анализ тренда сервисного товара** или **Анализ тренда контракта** для просмотра сводки операций книги сервиса для конкретного сервисного товара.</span><span class="sxs-lookup"><span data-stu-id="74633-106">For service items and contracts, you can also use the **Service Item Trendscape** or **Contract Trendscape** to view a summary of service ledger entries for a specific service item.</span></span>   

## <a name="viewing-statistics-for-service-orders"></a><span data-ttu-id="74633-107">Просмотр статистики для сервисных заказов</span><span class="sxs-lookup"><span data-stu-id="74633-107">Viewing Statistics for Service Orders</span></span>
<span data-ttu-id="74633-108">Функция статистики сервисного заказа позволяет быстро просмотреть содержимое всего сервисного заказа, подробности о конкретных сервисных строках и информацию, связанную с выставлением счетов, отгрузкой и потреблением, а также балансом клиента.</span><span class="sxs-lookup"><span data-stu-id="74633-108">The service order statistics feature gives you a quick overview of the contents of the entire service order, the details on the specific service lines, and information related to invoicing, shipping and consuming, and the customer's balance.</span></span>  

<span data-ttu-id="74633-109">Статистические данные отображаются для сервисного заказа в окне **Сервисный заказ - статистика** для соответствующего заказа.</span><span class="sxs-lookup"><span data-stu-id="74633-109">The statistical data is displayed for a service order in the **Service Order Statistics** window for the relevant order.</span></span> <span data-ttu-id="74633-110">Соответствующее окно статистики можно открыть из сервисного заказа.</span><span class="sxs-lookup"><span data-stu-id="74633-110">You can open the relevant statistics window from a service order.</span></span> <span data-ttu-id="74633-111">В окне **Сервисные заказы** выберите **Статистика**.</span><span class="sxs-lookup"><span data-stu-id="74633-111">In the **Service Orders** window, choose **Statistics**.</span></span> <span data-ttu-id="74633-112">На экспресс-вкладках в этом окне отображается такая информация, как количество, сумма, НДС, себестоимость, прибыль и кредитный лимит клиента.</span><span class="sxs-lookup"><span data-stu-id="74633-112">The FastTabs in this window show information such as quantity, amount, VAT, cost, profit, and customer credit limit.</span></span> <span data-ttu-id="74633-113">Если не указано иное, суммы в этом окне выражены в валюте сервисного заказа.</span><span class="sxs-lookup"><span data-stu-id="74633-113">The amounts in the window are in the currency of the service order, unless otherwise indicated.</span></span>  

### <a name="view-totals-for-a-service-order"></a><span data-ttu-id="74633-114">Просмотр итогов для сервисного заказа</span><span class="sxs-lookup"><span data-stu-id="74633-114">View totals for a service order</span></span>  
<span data-ttu-id="74633-115">Можно просмотреть итоговую сумму по сервисным строкам (с НДС и без), долю НДС, себестоимость и прибыль по сервисным строкам.</span><span class="sxs-lookup"><span data-stu-id="74633-115">You can view the total amount on the service lines, including and excluding VAT, VAT part, cost, and profit on the service lines.</span></span> <span data-ttu-id="74633-116">В окне также отображается информация по конкретному товару, такая как вес, объем и количество упаковок.</span><span class="sxs-lookup"><span data-stu-id="74633-116">The window also displays item-specific information, such as weight, volume, and the quantity of parcels.</span></span>  

### <a name="view-shipping-information"></a><span data-ttu-id="74633-117">Просмотр информации по отгрузке</span><span class="sxs-lookup"><span data-stu-id="74633-117">View shipping information</span></span>  
<span data-ttu-id="74633-118">Можно посмотреть информацию о товарах, ресурсах или себестоимости для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="74633-118">You can see information about the items, resources, or costs to be shipped.</span></span> <span data-ttu-id="74633-119">Для предоставления информации программа использует значения, указанные в поле **Кол-во для отгрузки** каждой сервисной строки в заказе.</span><span class="sxs-lookup"><span data-stu-id="74633-119">To provide the information, the values specified in the **Qty. to Ship** field are used on each service line in the order.</span></span>  

### <a name="view-order-details"></a><span data-ttu-id="74633-120">Просмотр сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="74633-120">View order details</span></span>  
<span data-ttu-id="74633-121">Можно просматривать информацию о товарах, времени использования ресурсов и себестоимости для включения в счета и потребления.</span><span class="sxs-lookup"><span data-stu-id="74633-121">You can view information about the items, resource hours, and costs to be invoiced and consumed.</span></span> <span data-ttu-id="74633-122">В следующей таблице описывается эта информация.</span><span class="sxs-lookup"><span data-stu-id="74633-122">The following table describes this information.</span></span>  

|<span data-ttu-id="74633-123">Столбец</span><span class="sxs-lookup"><span data-stu-id="74633-123">Column</span></span> | <span data-ttu-id="74633-124">Описанием</span><span class="sxs-lookup"><span data-stu-id="74633-124">Description</span></span>|  
|------------|---------------------------------------|  
|<span data-ttu-id="74633-125">**Выставление счетов**</span><span class="sxs-lookup"><span data-stu-id="74633-125">**Invoicing**</span></span>|<span data-ttu-id="74633-126">Отображает суммы, подлежащие учету как суммы, включенные в счета, которые выставлены по этому сервисному заказу.</span><span class="sxs-lookup"><span data-stu-id="74633-126">Displays amounts that are to be posted as invoiced from the service order.</span></span>|  
|<span data-ttu-id="74633-127">**Потребление**</span><span class="sxs-lookup"><span data-stu-id="74633-127">**Consuming**</span></span>|<span data-ttu-id="74633-128">Отображает количество и себестоимость товаров или ресурсов, которые будут учтены как потребленные.</span><span class="sxs-lookup"><span data-stu-id="74633-128">Displays the quantity and cost of items, or resources that will be posted as consumed.</span></span>|  
|<span data-ttu-id="74633-129">**Всего**</span><span class="sxs-lookup"><span data-stu-id="74633-129">**Total**</span></span>|<span data-ttu-id="74633-130">Отображает общие суммы по сервисному заказу как результат сложения сумм в выставленных счетах и сумм использования.</span><span class="sxs-lookup"><span data-stu-id="74633-130">Displays the total amounts on the service order that result from adding the invoicing amounts to the consuming amounts.</span></span>|  

### <a name="analyze-service-order-lines"></a><span data-ttu-id="74633-131">Анализ строк сервисного заказа</span><span class="sxs-lookup"><span data-stu-id="74633-131">Analyze service order lines</span></span>  
<span data-ttu-id="74633-132">Можно анализировать информацию по типам сервисных строк, включенных в сервисный заказ.</span><span class="sxs-lookup"><span data-stu-id="74633-132">You can analyze the information by the types of service lines included in the service order.</span></span> <span data-ttu-id="74633-133">Суммы отображаются раздельно для:</span><span class="sxs-lookup"><span data-stu-id="74633-133">The amounts are shown separately for:</span></span>  

* <span data-ttu-id="74633-134">Товаров</span><span class="sxs-lookup"><span data-stu-id="74633-134">Items</span></span>  
* <span data-ttu-id="74633-135">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="74633-135">Resources</span></span>  
* <span data-ttu-id="74633-136">Затраты и счета Главной книги</span><span class="sxs-lookup"><span data-stu-id="74633-136">Costs and general ledger accounts</span></span>  

### <a name="view-customer-information"></a><span data-ttu-id="74633-137">Просмотр информации о клиенте</span><span class="sxs-lookup"><span data-stu-id="74633-137">View customer information</span></span>  
<span data-ttu-id="74633-138">Просматривайте сальдо по счету клиента, а также максимальный кредит клиенту, для которого создан этот сервисный документ.</span><span class="sxs-lookup"><span data-stu-id="74633-138">See the balance on the customer's account, in addition to the maximum credit that can be endued to the customer who you created the service document for.</span></span>

## <a name="viewing-service-item-statistics"></a><span data-ttu-id="74633-139">Просмотр статистики сервисного товара</span><span class="sxs-lookup"><span data-stu-id="74633-139">Viewing Service Item Statistics</span></span>
<span data-ttu-id="74633-140">В окне **Статистика сервисного товара** можно просмотреть актуальную информацию по сервисному товару на основе следующих типов операций книг сервиса:</span><span class="sxs-lookup"><span data-stu-id="74633-140">In the **Service Item Statistics** window, you can see up-to-date information about a service item based the following service ledger entry types:</span></span>  

* <span data-ttu-id="74633-141">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="74633-141">Resources</span></span>  
* <span data-ttu-id="74633-142">Товаров</span><span class="sxs-lookup"><span data-stu-id="74633-142">Items</span></span>  
* <span data-ttu-id="74633-143">Затраты на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="74633-143">Service cost</span></span>  
* <span data-ttu-id="74633-144">Сервисные контракты</span><span class="sxs-lookup"><span data-stu-id="74633-144">Service contracts</span></span>  
* <span data-ttu-id="74633-145">Итог</span><span class="sxs-lookup"><span data-stu-id="74633-145">Total</span></span>  

<span data-ttu-id="74633-146">Для каждого типа операции можно просмотреть сумму выставленного счёта, потребление (сумму), сумму затрат, количество, количество по выставленному счету и потребленное количество, сумму прибыли и процент прибыли.</span><span class="sxs-lookup"><span data-stu-id="74633-146">For each entry type, you can see the invoiced amount, usage (amount), cost amount, quantity, quantity invoiced and quantity consumed, profit amount and profit percentage.</span></span> <span data-ttu-id="74633-147">Процент прибыли рассчитывается по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="74633-147">The profit percentage is calculated according to the following formula:</span></span>  

* <span data-ttu-id="74633-148">(Сумма по выставленным счетам - Потребление (Себестоимость)) x 100 / Сумма по выставленным счетам</span><span class="sxs-lookup"><span data-stu-id="74633-148">(Invoiced Amount - Usage (Cost)) x 100 / Invoiced Amount</span></span>  

## <a name="using-trendscapes"></a><span data-ttu-id="74633-149">Использование анализа трендов</span><span class="sxs-lookup"><span data-stu-id="74633-149">Using Trendscapes</span></span>
<span data-ttu-id="74633-150">Для сервисных товаров и сервисных контрактов окна **Анализ тренда сервисного товара** или **Анализ тренда сервисного контракта** предоставляют прокручиваемую сводную информацию об операциях книги обслуживания за определенный период времени для конкретного сервисного товара или контракта.</span><span class="sxs-lookup"><span data-stu-id="74633-150">For service items and service contracts, the **Service Item Trendscape** or **Service Contract Trendscape** windows provides a scrollable summary of service ledger entries in a period of time for a specific service item or contract.</span></span> <span data-ttu-id="74633-151">Для просмотра анализа тренда откройте сервисный товар или сервисный контракт, выберите действие **Статистика**, затем выберите **Анализ тренда**.</span><span class="sxs-lookup"><span data-stu-id="74633-151">To view the trendscape, open the service item or service contract, choose the **Statistics** action, and then choose **Trendscape**.</span></span>

<span data-ttu-id="74633-152">При прокручивании списка вычисляются суммы в локальной валюте, соответствующие указанному интервалу времени.</span><span class="sxs-lookup"><span data-stu-id="74633-152">When you scroll the list, the amounts are calculated in the local currency according to the specified time interval.</span></span> <span data-ttu-id="74633-153">Все суммы рассчитываются на основе операций книги сервиса, то есть операций, создаваемых при учете сервисных заказов или сервисных счетов.</span><span class="sxs-lookup"><span data-stu-id="74633-153">All amounts are calculated from service ledger entries, which are entries that are created when you post service orders or service invoices.</span></span>

<span data-ttu-id="74633-154">Список можно фильтровать, указав включаемые сервисные товары.</span><span class="sxs-lookup"><span data-stu-id="74633-154">You can filter the list by specifing the service items to include.</span></span>  

> [!Tip]  
>  <span data-ttu-id="74633-155">Если задан интервал **День**, и необходимо просмотреть длительный период, можно ускорить эту операцию, переключившись на более широкий интервал, например **Квартал**.</span><span class="sxs-lookup"><span data-stu-id="74633-155">If you have set the time interval to **Day** and you want to scroll over a long period, you can do it faster by shifting to a larger interval such as **Quarter**.</span></span> <span data-ttu-id="74633-156">После обнаружения нужного периода можно переключиться обратно на исходный интервал, чтобы просмотреть более подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="74633-156">When you have found the desired period, you can shift back to the original interval to see the data in more detail.</span></span>   

## <a name="viewing-gains-and-losses-on-contracts"></a><span data-ttu-id="74633-157">Просмотр прибылей и убытков по контрактам</span><span class="sxs-lookup"><span data-stu-id="74633-157">Viewing Gains and Losses on Contracts</span></span>  
<span data-ttu-id="74633-158">Операция контрактной прибыли или убытка создается во время преобразования предложения по контракту в сервисный контракт, при добавлении или удалении строк контракта из сервисного контракта и при отмене контракта.</span><span class="sxs-lookup"><span data-stu-id="74633-158">A contract gain or loss entry is generated when a contract quote is converted to a service contract, when contract lines are added or removed from a service contract, or when a contract is canceled.</span></span> <span data-ttu-id="74633-159">Прибыли или убытки по контракту можно просматривать на следующих страницах.</span><span class="sxs-lookup"><span data-stu-id="74633-159">You can view contract gains or losses on the following pages.</span></span>  

|<span data-ttu-id="74633-160">Стр.</span><span class="sxs-lookup"><span data-stu-id="74633-160">Page</span></span> | <span data-ttu-id="74633-161">Описанием</span><span class="sxs-lookup"><span data-stu-id="74633-161">Description</span></span>|  
|----------------|---------------------------------------|  
|<span data-ttu-id="74633-162">**Прибыли/убытки по контракту (контракты)**</span><span class="sxs-lookup"><span data-stu-id="74633-162">**Contract Gain/Loss (Contracts)**</span></span>|<span data-ttu-id="74633-163">Просмотр прибылей/убытков по контракту по сервисным контрактам</span><span class="sxs-lookup"><span data-stu-id="74633-163">To view the contract gain/loss by service contract.</span></span>|  
|<span data-ttu-id="74633-164">**Прибыли/убытки по контракту (группы)**</span><span class="sxs-lookup"><span data-stu-id="74633-164">**Contract Gain/Loss (Groups)**</span></span>|<span data-ttu-id="74633-165">Просмотр прибылей/убытков по контракту по группам сервисных контрактов</span><span class="sxs-lookup"><span data-stu-id="74633-165">To view the contract gain/loss by service contract group.</span></span>|  
|<span data-ttu-id="74633-166">**Прибыли/убытки по контракту (клиенты)**</span><span class="sxs-lookup"><span data-stu-id="74633-166">**Contract Gain/Loss (Customers)**</span></span>|<span data-ttu-id="74633-167">Просмотр прибылей/убытков по контракту по клиентам</span><span class="sxs-lookup"><span data-stu-id="74633-167">To view the contract gain/loss by customer.</span></span>|  
|<span data-ttu-id="74633-168">**Прибыли/убытки по контракту (основание)**</span><span class="sxs-lookup"><span data-stu-id="74633-168">**Contract Gain/Loss (Reasons)**</span></span>|<span data-ttu-id="74633-169">Просмотр прибылей/убытков по контракту по кодам причины</span><span class="sxs-lookup"><span data-stu-id="74633-169">To view the contract gain/loss by reason code.</span></span>|  
|<span data-ttu-id="74633-170">**Прибыли/убытки по контракту (центр отв.)**</span><span class="sxs-lookup"><span data-stu-id="74633-170">**Contract Gain/Loss (Resp.Ctr)**</span></span>|<span data-ttu-id="74633-171">Просмотр прибылей/убытков по контракту по центрам ответственности</span><span class="sxs-lookup"><span data-stu-id="74633-171">To view the contract gain/loss by responsibility center.</span></span>|  

1. <span data-ttu-id="74633-172">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите название страницы, которую требуется показать, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="74633-172">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the page to display, and then choose the related link.</span></span>  
2. <span data-ttu-id="74633-173">Заполните критерии фильтрации, которые нужно применить.</span><span class="sxs-lookup"><span data-stu-id="74633-173">Fill in the filter criteria you want to apply.</span></span> <span data-ttu-id="74633-174">Например, в окне **Прибыли/убытки по контракту (основание)** выберите значение для поля **Фильтр по коду причины**.</span><span class="sxs-lookup"><span data-stu-id="74633-174">For example, in the **Contract Gain/Loss (Reasons)** window, choose a value for **Reason Code Filter**.</span></span>  
3. <span data-ttu-id="74633-175">Выберите действие **Показать матрицу**.</span><span class="sxs-lookup"><span data-stu-id="74633-175">Choose the **Show Matrix** action.</span></span>

## <a name="viewing-statistics-for-posted-service-documents"></a><span data-ttu-id="74633-176">Просмотр статистики для учтенных сервисных документов</span><span class="sxs-lookup"><span data-stu-id="74633-176">Viewing Statistics for Posted Service Documents</span></span>
<span data-ttu-id="74633-177">Функция сервисной статистики позволяет получить статистический обзор содержимого учтенных сервисных документов, таких как учтенные расходные накладные, учтенные счета и учтенные кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="74633-177">The service statistics feature lets you gain a statistical overview of the contents of posted service documents, such as a posted shipment, posted invoice, and posted credit memo.</span></span>  

<span data-ttu-id="74633-178">Статистическая информация отображается в окне статистики соответствующего учтенного сервисного документа.</span><span class="sxs-lookup"><span data-stu-id="74633-178">The statistical information is displayed in the statistics window for the corresponding posted service document.</span></span> <span data-ttu-id="74633-179">Соответствующее окно статистики можно открыть из учтенной сервисной расходной накладной, учтенной сервисной накладной или учтенной сервисной кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="74633-179">You can open the relevant statistics window from posted service shipment, posted service invoice, or posted service credit memo documents.</span></span> <span data-ttu-id="74633-180">Для каждого из этих типов документов на вкладке **Главная** в группе **Процесс** выберите **Статистика**.</span><span class="sxs-lookup"><span data-stu-id="74633-180">For each of these document types, on the **Home** tab, in the **Process** group, choose **Statistics**.</span></span> <span data-ttu-id="74633-181">Например, в окне **Отправленные сервисные счета** на вкладке **Главная** в группе **Процесс** выберите **Статистика**.</span><span class="sxs-lookup"><span data-stu-id="74633-181">For example, from the **Posted Service Invoices** window, on the **Home** tab, in the **Process** group, choose **Statistics**.</span></span>  

### <a name="posted-service-shipment-statistics"></a><span data-ttu-id="74633-182">Учтенная сервисная расх. накладная - статистика</span><span class="sxs-lookup"><span data-stu-id="74633-182">Posted Service Shipment Statistics</span></span>  
<span data-ttu-id="74633-183">В окне **Статистика сервисной расх. накладной** представлен обзор учтенных сервисных расходных накладных.</span><span class="sxs-lookup"><span data-stu-id="74633-183">The **Service Shipment Statistics** window provides an overview of a posted service shipment.</span></span> <span data-ttu-id="74633-184">Сюда входит информация о физических параметрах отгрузки, например количестве отгруженных товаров, времени использования ресурсов или себестоимости, а также о весе и объеме отгруженных товаров.</span><span class="sxs-lookup"><span data-stu-id="74633-184">This includes information about the physical contents of the shipment, such as quantity of the shipped items, resource hours or costs, and weight and volume of the shipped items.</span></span>  

### <a name="posted-service-invoice-statistics"></a><span data-ttu-id="74633-185">Учтенная статистика сервисного счета</span><span class="sxs-lookup"><span data-stu-id="74633-185">Posted Service Invoice Statistics</span></span>  
<span data-ttu-id="74633-186">В окне **Сервисный счет - статистика** представлена статистическая сводка по учтенному сервисному счету.</span><span class="sxs-lookup"><span data-stu-id="74633-186">You can see a statistical summary on a posted service invoice in the **Service Invoice Statistics** window.</span></span> <span data-ttu-id="74633-187">Можно просматривать итоговые суммы учтенного сервисного счета.</span><span class="sxs-lookup"><span data-stu-id="74633-187">You can view the totals of the posted service invoice.</span></span> <span data-ttu-id="74633-188">Эти данные включают итоговую сумму по сервисным строкам (с НДС и без), которая была учтена как включенная в счет, долю НДС, себестоимость и прибыль по учтенному счету.</span><span class="sxs-lookup"><span data-stu-id="74633-188">The data includes total amount on the service lines (including and excluding VAT) that has been posted as invoiced, VAT part, cost, and profit on the posted invoice.</span></span> <span data-ttu-id="74633-189">В окне также отображается приведенная ниже информация:</span><span class="sxs-lookup"><span data-stu-id="74633-189">The window also displays information about the following:</span></span>  

* <span data-ttu-id="74633-190">Товары в строках сервисного счета, например вес, объем и количество упаковок.</span><span class="sxs-lookup"><span data-stu-id="74633-190">The items on the service invoice lines, such as weight, volume, and the quantity of parcels.</span></span>  
* <span data-ttu-id="74633-191">Сальдо по счету клиента, а также максимальный кредит, который вы можете предоставить этому клиенту.</span><span class="sxs-lookup"><span data-stu-id="74633-191">The balance on the customer's account, and the maximum credit that you can extend the customer.</span></span>  

### <a name="posted-service-credit-memo-statistics"></a><span data-ttu-id="74633-192">Учтенная сервисная кредит-нота - статистика</span><span class="sxs-lookup"><span data-stu-id="74633-192">Posted Service Credit Memo Statistics</span></span>  
<span data-ttu-id="74633-193">Окно **Сервисная кредит-нота - статистика** можно использовать, чтобы получить статистический обзор строк учтенной сервисной кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="74633-193">You can use the **Service Credit Memo Statistics** window to get a statistical overview of the lines in a posted service credit memo.</span></span> <span data-ttu-id="74633-194">Обзор может включать:</span><span class="sxs-lookup"><span data-stu-id="74633-194">The overview can include:</span></span>

* <span data-ttu-id="74633-195">Итоговые суммы по учтенной кредит-ноте, отображаемые как количество, сумма, НДС, себестоимость и прибыль.</span><span class="sxs-lookup"><span data-stu-id="74633-195">The total amounts on the posted credit memo, displayed as quantity, amount, VAT, cost and profit.</span></span> <span data-ttu-id="74633-196">Также содержится информация о товарах из сервисных строк учтенной кредит-ноты, например количество, вес и объем.</span><span class="sxs-lookup"><span data-stu-id="74633-196">There is also information about the items on the service lines of the posted credit memo, such as quantity, weight, and volume.</span></span>  
* <span data-ttu-id="74633-197">Общая информация о клиенте, такая как кредитный лимит клиента и сальдо счета.</span><span class="sxs-lookup"><span data-stu-id="74633-197">General information about the customer, such as the customer's credit limit and balance on the account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="74633-198">См. также</span><span class="sxs-lookup"><span data-stu-id="74633-198">See Also</span></span>  
<span data-ttu-id="74633-199">[Создание сервисных заказов](service-how-to-create-service-orders.md) </span><span class="sxs-lookup"><span data-stu-id="74633-199">[Create Service Orders](service-how-to-create-service-orders.md) </span></span>  
<span data-ttu-id="74633-200">[Создание сервисных товаров](service-how-to-create-service-items.md) </span><span class="sxs-lookup"><span data-stu-id="74633-200">[Create Service Items](service-how-to-create-service-items.md) </span></span>  
[<span data-ttu-id="74633-201">Планирование сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="74633-201">Planning Service</span></span>](service-plan-service.md)  
