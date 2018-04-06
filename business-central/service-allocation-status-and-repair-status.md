---
title: "Статус распределения и ремонта | Документы Майкрософт"
description: "Узнайте об отношениях между статусом ремонта сервисных товаров и статусом распределения операций распределения для них."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 014ede5232017bb090fa6cd33816064a6c4b99b8
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="allocation-status-and-repair-status-of-service-items"></a><span data-ttu-id="7d691-103">Статус распределения и статус ремонта сервисных товаров</span><span class="sxs-lookup"><span data-stu-id="7d691-103">Allocation Status and Repair Status of Service Items</span></span>
<span data-ttu-id="7d691-104">Статус ремонта сервисных товаров и статус распределения операций распределения для сервисных товаров имеют определенную связь в области приложения "Сервисное управление".</span><span class="sxs-lookup"><span data-stu-id="7d691-104">The repair status of service items and the allocation status of the allocation entries for the service items have a certain relationship in Service Management.</span></span> <span data-ttu-id="7d691-105">Статус распределения меняется при изменении статуса ремонта сервисного товара на **Завершено** или **Частично обслужено**, а также когда сервисное предложение преобразуется в сервисный заказ.</span><span class="sxs-lookup"><span data-stu-id="7d691-105">The allocation status changes when you change the repair status of the service item to **Finished** or **Partly Serviced** and when you convert a service quote to a service order.</span></span> <span data-ttu-id="7d691-106">Статус ремонта сервисного товара меняется при отмене распределения сервисного товара или перераспределении сервисного товара на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="7d691-106">The repair status of the service item changes when you cancel the service item allocation or reallocate the service item to another resource.</span></span> <span data-ttu-id="7d691-107">Статус ремонта сервисных товаров можно просмотреть в окне **Сервисные задачи** и обновить его в поле **Код статуса ремонта** в окне **Журнал сервисных товаров**.</span><span class="sxs-lookup"><span data-stu-id="7d691-107">You can view the repair status of service items in the **Service Tasks** window and you can update the repair status in the **Repair Status Code** field in the **Service Item Worksheet** window.</span></span> <span data-ttu-id="7d691-108">Статус распределения можно просмотреть в поле **Статус** в окне **Распределение ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="7d691-108">You can view the allocation status in the **Status** field in the **Resource Allocations** window.</span></span>  
  
## <a name="changing-repair-status"></a><span data-ttu-id="7d691-109">Изменение статуса ремонта</span><span class="sxs-lookup"><span data-stu-id="7d691-109">Changing Repair Status</span></span>  
<span data-ttu-id="7d691-110">При изменении статуса ремонта сервисного товара в строке сервисного товара выполняется поиск соответствующей операции распределения этого сервисного товара, которая имеет статус **Активен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-110">When you change the repair status of a service item on a service item line, there is a search for a corresponding allocation entry for this service item that has the status **Active**.</span></span> <span data-ttu-id="7d691-111">Если обнаружена такая операция распределения, статус обновляется одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="7d691-111">If such an allocation entry is found, the status is updated in one of the following ways:</span></span>  
  
* <span data-ttu-id="7d691-112">Если статус ремонта меняется на **Завершен**, то статус распределения изменяется с **Активен** на **Завершен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-112">If you change the repair status to **Finished**, the allocation status is changed from **Active** to **Finished**.</span></span>  
* <span data-ttu-id="7d691-113">Если статус ремонта меняется на **Частично обслужено** (выполнено частичное обслуживание) или **Ссылается** (никакое обслуживание не выполнено), то статус распределения меняется с **Активен** на **Требуется перераспределение**.</span><span class="sxs-lookup"><span data-stu-id="7d691-113">If you change the repair status to **Partly Serviced**, that is, some of the service has been completed, or **Referred**, that is, no service has been done, the allocation status is changed from **Active** to **Reallocation Needed**.</span></span>  
* <span data-ttu-id="7d691-114">Когда для сервисного заказа создается операция распределения, указывающая на отсутствие распределения ресурсов, в поле **Статус** окна **Распределение ресурсов** устанавливается значение **Неактивный**.</span><span class="sxs-lookup"><span data-stu-id="7d691-114">When a service order allocation entry is created that indicates that no resource has been allocated, the **Status** field in the **Resource Allocation** window is set to **Nonactive**.</span></span>  
* <span data-ttu-id="7d691-115">Устанавливается значение **Отменен** для статуса операции распределения, когда выполняется перераспределение соответствующего сервисного товара в операции распределения сервисных заказов, указывая на то, что распределенным ресурсом или группой ресурсов не производилась попытка выполнения сервисной задачи.</span><span class="sxs-lookup"><span data-stu-id="7d691-115">The allocation entry status is set to **Canceled** when you reallocate the referred service item in the service order allocation entry, which indicates that the allocated resource or resource group has not attempted the service task.</span></span>  
  
<span data-ttu-id="7d691-116">Статус распределения отражает, закончен ли процесс обслуживания, или для завершения обслуживания сервисного товара нужен другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="7d691-116">The allocation status reflects when the service process is finished, or when another resource is necessary in order to finish the service of the service item.</span></span>  
  
## <a name="converting-service-quotes-to-service-orders"></a><span data-ttu-id="7d691-117">Преобразование сервисных предложений в сервисные заказы</span><span class="sxs-lookup"><span data-stu-id="7d691-117">Converting Service Quotes to Service Orders</span></span>  
<span data-ttu-id="7d691-118">При преобразовании сервисного предложения в сервисный заказ сервисный заказ, сервисные товары в заказе и операции распределения обновляются следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7d691-118">When you convert a service quote to a service order, the service order, the service items in the order and their allocation entries are updated in the following ways:</span></span>  
  
* <span data-ttu-id="7d691-119">Статус ремонта сервисных товаров изменяется на **Начальный**.</span><span class="sxs-lookup"><span data-stu-id="7d691-119">The repair status of the service items is changed to **Initial**.</span></span>  
* <span data-ttu-id="7d691-120">Статус сервисного заказа изменяется на **Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="7d691-120">The service order status is changed to **Pending**.</span></span>  
* <span data-ttu-id="7d691-121">Выполняется поиск тех операций распределения для всех сервисных товаров в сервисном заказе, которые имеют статус **Активен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-121">There is a search for allocation entries for all the service items in the service order that have the status **Active**.</span></span> <span data-ttu-id="7d691-122">Если обнаружены такие операции распределения, их статус распределения изменяется с **Активен** на **Требуется перераспределение**.</span><span class="sxs-lookup"><span data-stu-id="7d691-122">If such allocation entries are found, their allocation status is changed from **Active** to **Reallocation Needed**.</span></span>  
  
## <a name="canceling-allocations"></a><span data-ttu-id="7d691-123">Отмена распределений</span><span class="sxs-lookup"><span data-stu-id="7d691-123">Canceling Allocations</span></span>  
<span data-ttu-id="7d691-124">При отмене распределения сервисного товара [!INCLUDE[d365fin](includes/d365fin_md.md)] обновляет статус распределения соответствующей операции распределения с **Активно** на **Требуется перераспределение**</span><span class="sxs-lookup"><span data-stu-id="7d691-124">When you cancel an allocation for a service item, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the allocation status of the corresponding allocation entry from **Active** to **Reallocation Needed**.</span></span>

<span data-ttu-id="7d691-125">Статус ремонта сервисного товара в операции распределения обновляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7d691-125">The repair status of the service item in the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7d691-126">Если статус ремонта **Начальный**, он изменяется на **Ссылается** (обслуживание не начиналось).</span><span class="sxs-lookup"><span data-stu-id="7d691-126">If the repair status is **Initial**, the repair status is changed to **Referred** (no service has been started).</span></span>  
* <span data-ttu-id="7d691-127">Если статус ремонта **В работе**, он изменяется на **Частично обслужено** (обслуживание выполнено частично).</span><span class="sxs-lookup"><span data-stu-id="7d691-127">If the repair status is **In Process**, the repair status is changed to **Partly Serviced** (some service has been completed).</span></span>  
  
## <a name="reallocating-an-active-allocation-entry"></a><span data-ttu-id="7d691-128">Перераспределение активной операции распределения</span><span class="sxs-lookup"><span data-stu-id="7d691-128">Reallocating an Active Allocation Entry</span></span>  
<span data-ttu-id="7d691-129">При перераспределении сервисного товара в операции распределения, имеющей статус **Активен**, операция распределения обновляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7d691-129">When you reallocate a service item in an allocation entry that is **Active**, the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7d691-130">Если обслуживание началось, когда распределение имело статус **Активен** (т.е. статус ремонта сервисного товара в операции был изменен на статус **В работе**), то статус распределения меняется с **Активен** на **Завершен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-130">If service was started when the allocation was **Active** (that is, if the repair status of the service item in the entry was changed to **In Process**), the allocation status is changed from **Active** to **Finished**.</span></span>  
* <span data-ttu-id="7d691-131">Если обслуживание не было начато, когда распределение имело статус **Активен**, то статус распределения меняется с **Активен** на **Отменен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-131">If service was not started when the allocation was **Active**, the allocation status is changed from **Active** to **Canceled**.</span></span>  
  
<span data-ttu-id="7d691-132">Статус ремонта сервисного товара в операции распределения обновляется тем же способом, что и при отмене распределения:</span><span class="sxs-lookup"><span data-stu-id="7d691-132">The repair status of the service item in the allocation entry is updated in the same way as if you had canceled the allocation:</span></span>  
  
* <span data-ttu-id="7d691-133">Если статус ремонта **Начальный**, он изменяется на **Ссылается** (обслуживание не начиналось).</span><span class="sxs-lookup"><span data-stu-id="7d691-133">If the repair status is **Initial**, the repair status is changed to **Referred** (no service has been started).</span></span>  
* <span data-ttu-id="7d691-134">Если статус ремонта **В работе**, он изменяется на **Частично обслужено** (обслуживание выполнено частично).</span><span class="sxs-lookup"><span data-stu-id="7d691-134">If the repair status is **In Process**, the repair status is changed to **Partly Serviced** (some service has been completed).</span></span>  
  
<span data-ttu-id="7d691-135">Создается новая операция распределения, содержащая новый ресурс и имеющая статус **Активно**.</span><span class="sxs-lookup"><span data-stu-id="7d691-135">A new allocation entry that contains the new resource is created that has the status **Active**.</span></span>  
  
## <a name="reallocating-a-service-item"></a><span data-ttu-id="7d691-136">Перераспределение сервисного товара</span><span class="sxs-lookup"><span data-stu-id="7d691-136">Reallocating a Service Item</span></span>  
<span data-ttu-id="7d691-137">При перераспределении сервисного товара в операции распределения, имеющей статус **Требуется перераспределение**, операция распределения обновляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7d691-137">When you reallocate a service item in an allocation entry that has the status **Reallocation Needed**, the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7d691-138">Если обслуживание началось, когда распределение имело статус **Активен** (т.е. статус ремонта сервисного товара в операции был изменен на статус **В работе**), то статус распределения меняется с **Требуется перераспределение** на **Завершен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-138">If service was started when the allocation was **Active** (that is, if the repair status of the service item in the entry was changed to **In Process**), the allocation status is changed from **Reallocation Needed** to **Finished**.</span></span>  
* <span data-ttu-id="7d691-139">Если обслуживание не начиналось, когда распределение имело статус **Активна**, статус распределения меняется с **Нужно перераспределение** на **Отменен**.</span><span class="sxs-lookup"><span data-stu-id="7d691-139">If service was not started when the allocation was **Active**, the allocation status is changed from **Reallocation Needed** to **Canceled**.</span></span>  
  
<span data-ttu-id="7d691-140">Создается новая операция распределения, содержащая новый ресурс и имеющая статус **Активно**.</span><span class="sxs-lookup"><span data-stu-id="7d691-140">A new allocation entry that contains the new resource is created that has the status **Active**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d691-141">См. также</span><span class="sxs-lookup"><span data-stu-id="7d691-141">See Also</span></span>  
[<span data-ttu-id="7d691-142">Настройка распределений ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d691-142">Set Up Resource Allocations</span></span>](service-how-setup-resource-allocation.md)  
[<span data-ttu-id="7d691-143">Распределение ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d691-143">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  

