---
title: Синхронизация Business Central и Dynamics 365 for Sales | Документы Майкрософт
description: Узнайте о синхронизации данных между Business Central и Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: b3fb3d2680cd85da8b2def7e82fbf62c0046fcc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247425"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a><span data-ttu-id="fd4d7-103">Планирование синхронизации между Business Central и Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-103">Scheduling a Synchronization between Business Central and Dynamics 365 for Sales</span></span>
<span data-ttu-id="fd4d7-104">Можно синхронизировать [!INCLUDE[d365fin](includes/d365fin_md.md)] с [!INCLUDE[crm_md](includes/crm_md.md)] для запланированных интервалов путем настройки заданий в очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-104">You can synchronize [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)] on scheduled intervals by setting up jobs in the job queue.</span></span> <span data-ttu-id="fd4d7-105">Задания синхронизации выполнят синхронизацию данных в записях [!INCLUDE[d365fin](includes/d365fin_md.md)] и записях [!INCLUDE[crm_md](includes/crm_md.md)], которые ранее были связаны.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-105">The synchronization jobs synchronize data in [!INCLUDE[d365fin](includes/d365fin_md.md)] records and [!INCLUDE[crm_md](includes/crm_md.md)] records that have been previously coupled together.</span></span> <span data-ttu-id="fd4d7-106">Или для записей, которые еще не связаны, в зависимости от направления синхронизации и правил, задания синхронизации могут создать и связать новые записи в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-106">Or for records that are not already coupled, depending on the synchronization direction and rules, the synchronization jobs can create and couple new records in the destination system.</span></span> <span data-ttu-id="fd4d7-107">Имеется несколько заданий синхронизации, которые доступны в готовом виде.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-107">There are several synchronization jobs that are available out-of-the-box.</span></span> <span data-ttu-id="fd4d7-108">Их можно просмотреть на странице **Операции очереди работ**.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-108">You can view them on the **Job Queue Entries** page.</span></span> <span data-ttu-id="fd4d7-109">Дополнительные сведения см. в разделе [Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a><span data-ttu-id="fd4d7-110">Процесс синхронизации</span><span class="sxs-lookup"><span data-stu-id="fd4d7-110">Synchronization Process</span></span>  
<span data-ttu-id="fd4d7-111">Каждая операция очереди заданий синхронизации использует соответствующее сопоставление таблицы интеграции, задающее таблицу [!INCLUDE[d365fin](includes/d365fin_md.md)] и объект [!INCLUDE[crm_md](includes/crm_md.md)], которые должны быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-111">Each synchronization job queue entry uses a specific integration table mapping that specifies which [!INCLUDE[d365fin](includes/d365fin_md.md)] table and [!INCLUDE[crm_md](includes/crm_md.md)] entity to synchronize.</span></span> <span data-ttu-id="fd4d7-112">Сопоставления таблиц также включают ряд настроек, управляющих записями в таблице [!INCLUDE[d365fin](includes/d365fin_md.md)] и объекте [!INCLUDE[crm_md](includes/crm_md.md)], которые должны быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-112">The table mappings also include some settings that control which records in the [!INCLUDE[d365fin](includes/d365fin_md.md)] table and [!INCLUDE[crm_md](includes/crm_md.md)] entity to synchronize.</span></span>  

<span data-ttu-id="fd4d7-113">Чтобы синхронизировать данные, записи объекта [!INCLUDE[crm_md](includes/crm_md.md)] должны быть связаны с записями [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-113">To synchronize data, [!INCLUDE[crm_md](includes/crm_md.md)] entity records must be coupled to [!INCLUDE[d365fin](includes/d365fin_md.md)] records.</span></span> <span data-ttu-id="fd4d7-114">Например, клиент [!INCLUDE[d365fin](includes/d365fin_md.md)] должен быть связан с организацией [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-114">For example, a [!INCLUDE[d365fin](includes/d365fin_md.md)] customer must be coupled to a [!INCLUDE[crm_md](includes/crm_md.md)] account.</span></span> <span data-ttu-id="fd4d7-115">Связи можно настроить вручную перед выполнением заданий синхронизации или позволить заданиям синхронизации автоматически настроить связи.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-115">You can set up couplings manually, before running the synchronization jobs, or let the synchronization jobs set up couplings automatically.</span></span> <span data-ttu-id="fd4d7-116">В следующем списке указан способ синхронизации данных между [!INCLUDE[crm_md](includes/crm_md.md)] и [!INCLUDE[d365fin](includes/d365fin_md.md)] при использовании операций очереди заданий синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-116">The following list describes how data is synchronized between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] when you are using the synchronization job queue entries.</span></span> <span data-ttu-id="fd4d7-117">Дополнительные сведения см. в разделе [Связывание и синхронизация записей вручную](admin-how-to-couple-and-synchronize-records-manually.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-117">For more information, see [Couple and Synchronize Records Manually](admin-how-to-couple-and-synchronize-records-manually.md).</span></span> 

-   <span data-ttu-id="fd4d7-118">По умолчанию синхронизируются только записи в [!INCLUDE[d365fin](includes/d365fin_md.md)], связанные с записями в [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-118">By default, only records in [!INCLUDE[d365fin](includes/d365fin_md.md)] that are coupled to records in [!INCLUDE[crm_md](includes/crm_md.md)] are synchronized.</span></span> <span data-ttu-id="fd4d7-119">Сопоставление таблицы между операцией [!INCLUDE[crm_md](includes/crm_md.md)] и таблицей [!INCLUDE[d365fin](includes/d365fin_md.md)] можно изменить, чтобы задания синхронизации интеграции создавали новые записи в целевой базе данных для каждой записи в исходной базе, которая не связана.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-119">You can change the table mapping between a [!INCLUDE[crm_md](includes/crm_md.md)] entity and a [!INCLUDE[d365fin](includes/d365fin_md.md)] table so that the integration synchronization jobs will create new records in the destination database for each record in the source database that is not coupled.</span></span> <span data-ttu-id="fd4d7-120">Новые записи также связываются с соответствующими записями в источнике.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-120">The new records are also coupled to the corresponding records in the source.</span></span> <span data-ttu-id="fd4d7-121">Например, при синхронизации клиентов с организациями [!INCLUDE[crm_md](includes/crm_md.md)] создается новая запись организации для каждого клиента в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-121">For example, when you synchronize customers with [!INCLUDE[crm_md](includes/crm_md.md)] accounts, a new account record is created for each customer in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fd4d7-122">Новые счета автоматически связываются с клиентами в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-122">The new accounts are automatically coupled to customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fd4d7-123">Поскольку синхронизация в этом случае является двунаправленной, новый клиент создается и связывается для каждой организации [!INCLUDE[crm_md](includes/crm_md.md)], которая еще не связана.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-123">Because the synchronization in this case is bidirectional, a new customer is created and coupled for each [!INCLUDE[crm_md](includes/crm_md.md)] account that is not already coupled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="fd4d7-124">Имеются правила и фильтры, которые определяют, какие данные синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-124">There are rules and filters that determine what data is synchronized.</span></span> <span data-ttu-id="fd4d7-125">Для получения дополнительной информации см. [Правила синхронизации](admin-synchronizing-business-central-and-sales.md#synchronization-rules).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-125">For more information, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules).</span></span>

-   <span data-ttu-id="fd4d7-126">Когда новые записи создаются в [!INCLUDE[d365fin](includes/d365fin_md.md)], записи используют шаблон, определенный для сопоставления таблиц интеграции, или шаблон по умолчанию, доступный для этого типа записей.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-126">When new records are created in [!INCLUDE[d365fin](includes/d365fin_md.md)], the records use the either the template that is defined for the integration table mapping or the default template that is available for the record type.</span></span> <span data-ttu-id="fd4d7-127">Поля заполняются данными из [!INCLUDE[d365fin](includes/d365fin_md.md)] или [!INCLUDE[crm_md](includes/crm_md.md)] в зависимости от направления синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-127">Fields are populated with data from [!INCLUDE[d365fin](includes/d365fin_md.md)] or [!INCLUDE[crm_md](includes/crm_md.md)] depending on the synchronization direction.</span></span> <span data-ttu-id="fd4d7-128">Дополнительные сведения см. в разделе [Практическое руководство. Изменение сопоставлений таблицы для синхронизации](admin-how-to-modify-table-mappings-for-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-128">For more information, see [How to: Modify Table Mappings for Synchronization](admin-how-to-modify-table-mappings-for-synchronization.md).</span></span>  

-   <span data-ttu-id="fd4d7-129">При последующих синхронизациях обновляются только те записи, которые были изменены или добавлены после последнего успешного задания синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-129">With subsequent synchronizations, only records that have been modified or added after the last successful synchronization job for the entity will be updated.</span></span>  

     <span data-ttu-id="fd4d7-130">Новые записи в [!INCLUDE[crm_md](includes/crm_md.md)] добавляются в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-130">New records in [!INCLUDE[crm_md](includes/crm_md.md)] are added in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fd4d7-131">Если данные в полях в записях [!INCLUDE[crm_md](includes/crm_md.md)] изменены, данные копируются в соответствующее поле в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-131">If data in fields in [!INCLUDE[crm_md](includes/crm_md.md)] records has changed, the data is copied to the corresponding field in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

-   <span data-ttu-id="fd4d7-132">При двунаправленной синхронизации задание выполняет синхронизацию из [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)], а затем из [!INCLUDE[crm_md](includes/crm_md.md)] в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-132">With bidirectional synchronization, the job synchronizes from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)], and then from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="default-synchronization-job-queue-entries"></a><span data-ttu-id="fd4d7-133">Операции очереди заданий синхронизации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd4d7-133">Default Synchronization Job Queue Entries</span></span>  
<span data-ttu-id="fd4d7-134">В следующей таблице описываются задания синхронизации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-134">The following table describes the default synchronization jobs.</span></span>  

|<span data-ttu-id="fd4d7-135">Операция очереди работ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-135">Job Queue Entry</span></span>|<span data-ttu-id="fd4d7-136">Описанием</span><span class="sxs-lookup"><span data-stu-id="fd4d7-136">Description</span></span>|<span data-ttu-id="fd4d7-137">Направление</span><span class="sxs-lookup"><span data-stu-id="fd4d7-137">Direction</span></span>|<span data-ttu-id="fd4d7-138">Сопоставление таблиц интеграции</span><span class="sxs-lookup"><span data-stu-id="fd4d7-138">Integration Table Mapping</span></span>|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|<span data-ttu-id="fd4d7-139">Задание синхронизации КОНТАКТ — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-139">CONTACT - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-140">Синхронизирует контакты [!INCLUDE[crm_md](includes/crm_md.md)] с контактами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-140">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] contacts with [!INCLUDE[d365fin](includes/d365fin_md.md)] contacts.</span></span>|<span data-ttu-id="fd4d7-141">Двунаправленная</span><span class="sxs-lookup"><span data-stu-id="fd4d7-141">Bidirectional</span></span>|<span data-ttu-id="fd4d7-142">КОНТАКТ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-142">CONTACT</span></span>|  
|<span data-ttu-id="fd4d7-143">Задание синхронизации ВАЛЮТА — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-143">CURRENCY - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-144">Синхронизирует валюты транзакций [!INCLUDE[crm_md](includes/crm_md.md)] с валютами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-144">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] transaction currencies with [!INCLUDE[d365fin](includes/d365fin_md.md)] currencies.</span></span>|<span data-ttu-id="fd4d7-145">Из [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-145">From [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>|<span data-ttu-id="fd4d7-146">ВАЛЮТА</span><span class="sxs-lookup"><span data-stu-id="fd4d7-146">CURRENCY</span></span>|  
|<span data-ttu-id="fd4d7-147">Задание синхронизации КЛИЕНТ — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-147">CUSTOMER - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-148">Синхронизирует организации [!INCLUDE[crm_md](includes/crm_md.md)] с клиентами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-148">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] accounts with [!INCLUDE[d365fin](includes/d365fin_md.md)] customers.</span></span>|<span data-ttu-id="fd4d7-149">Двунаправленная</span><span class="sxs-lookup"><span data-stu-id="fd4d7-149">Bidirectional</span></span>|<span data-ttu-id="fd4d7-150">КЛИЕНТ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-150">CUSTOMER</span></span>|  
|<span data-ttu-id="fd4d7-151">Задание синхронизации CUSTPRCGRP-PRICE — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-151">CUSTPRCGRP-PRICE - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-152">Синхронизирует прайс-листы продаж [!INCLUDE[crm_md](includes/crm_md.md)] с ценовыми группами клиентов [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-152">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] sales price lists with [!INCLUDE[d365fin](includes/d365fin_md.md)] customer price groups.</span></span>| |<span data-ttu-id="fd4d7-153">ЦЕНОВЫЕ ГРУППЫ КЛИЕНТОВ — ПРАЙС-ЛИСТЫ ПРОДАЖ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-153">CUSTOMER PRICE GROUPS-SALES PRICE LISTS</span></span>|
|<span data-ttu-id="fd4d7-154">Задание синхронизации ТОВАР - ПРОДУКТ — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-154">ITEM - PRODUCT - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-155">Синхронизирует продукты [!INCLUDE[crm_md](includes/crm_md.md)] с товарами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-155">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] products with [!INCLUDE[d365fin](includes/d365fin_md.md)] items.</span></span>|<span data-ttu-id="fd4d7-156">Из [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-156">From [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>|<span data-ttu-id="fd4d7-157">ТОВАР-ПРОДУКТ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-157">ITEM-PRODUCT</span></span>|
|<span data-ttu-id="fd4d7-158">Задание синхронизации POSTEDSALESINV-INV — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-158">POSTEDSALESINV-INV - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-159">Синхронизирует счета [!INCLUDE[crm_md](includes/crm_md.md)] с учтенными счетами продаж [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-159">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] invoices with [!INCLUDE[d365fin](includes/d365fin_md.md)] posted sales invoices.</span></span>|<span data-ttu-id="fd4d7-160">Из [!INCLUDE[crm_md](includes/crm_md.md)] в [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-160">From [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>|<span data-ttu-id="fd4d7-161">СЧЕТА — УЧТЕННЫЕ СЧЕТА ПРОДАЖ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-161">INVOICES-POSTED SALES INVOICES</span></span>|
|<span data-ttu-id="fd4d7-162">Задание синхронизации "РЕСУРС-ПРОДУКТ — Dynamics 365 for Sales"</span><span class="sxs-lookup"><span data-stu-id="fd4d7-162">RESOURCE-PRODUCT - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-163">Синхронизирует продукты [!INCLUDE[crm_md](includes/crm_md.md)] с ресурсами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-163">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] products with [!INCLUDE[d365fin](includes/d365fin_md.md)] resources.</span></span>|<span data-ttu-id="fd4d7-164">Из [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-164">From [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>|<span data-ttu-id="fd4d7-165">РЕСУРС-ПРОДУКТ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-165">RESOURCE-PRODUCT</span></span>|  
|<span data-ttu-id="fd4d7-166">Задание синхронизации "ПРОДАВЦЫ — Dynamics 365 for Sales"</span><span class="sxs-lookup"><span data-stu-id="fd4d7-166">SALESPEOPLE - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-167">Синхронизирует продавцов [!INCLUDE[d365fin](includes/d365fin_md.md)] с пользователями [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-167">Synchronizes [!INCLUDE[d365fin](includes/d365fin_md.md)] salespeople with [!INCLUDE[crm_md](includes/crm_md.md)] users.</span></span>|<span data-ttu-id="fd4d7-168">Из [!INCLUDE[crm_md](includes/crm_md.md)] в [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-168">From [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>|<span data-ttu-id="fd4d7-169">ПРОДАВЦЫ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-169">SALESPEOPLE</span></span>|
|<span data-ttu-id="fd4d7-170">Задание синхронизации SALESPRC-PRODUCTPRICE — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-170">SALESPRC-PRODUCTPRICE - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-171">Синхронизирует цены продуктов [!INCLUDE[crm_md](includes/crm_md.md)] с ценами продажи [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-171">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] product prices with [!INCLUDE[d365fin](includes/d365fin_md.md)] sales prices.</span></span>||<span data-ttu-id="fd4d7-172">ЦЕНА ПРОДУКТА — ЦЕНА ПРОДАЖ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-172">PRODUCT PRICE-SALES PRICE</span></span>|
|<span data-ttu-id="fd4d7-173">Задание синхронизации "ЕДИНИЦА ИЗМЕРЕНИЯ — Dynamics 365 for Sales"</span><span class="sxs-lookup"><span data-stu-id="fd4d7-173">UNITOFMEASURE - Dynamics 365 for Sales synchronization job</span></span>|<span data-ttu-id="fd4d7-174">Синхронизирует группы единиц [!INCLUDE[crm_md](includes/crm_md.md)] с единицами измерения [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-174">Synchronizes [!INCLUDE[crm_md](includes/crm_md.md)] unit groups with [!INCLUDE[d365fin](includes/d365fin_md.md)] units of measure.</span></span>|<span data-ttu-id="fd4d7-175">Из [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4d7-175">From [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>|<span data-ttu-id="fd4d7-176">ЕДИНИЦА ИЗМЕРЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd4d7-176">UNIT OF MEASURE</span></span>|  
|<span data-ttu-id="fd4d7-177">Синхронизация статистики по клиенту — Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-177">Customer Statistics - Dynamics 365 for Sales synchronization</span></span>|<span data-ttu-id="fd4d7-178">Обновление организаций [!INCLUDE[crm_md](includes/crm_md.md)] с новейшими данными клиентов [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-178">Updates [!INCLUDE[crm_md](includes/crm_md.md)] accounts with the latest [!INCLUDE[d365fin](includes/d365fin_md.md)] customer data.</span></span> <span data-ttu-id="fd4d7-179">В [!INCLUDE[crm_md](includes/crm_md.md)] данная информация отображается в форме быстрого просмотра **Статистика организации Business Central** организаций, которые связаны с клиентами [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-179">In [!INCLUDE[crm_md](includes/crm_md.md)], this information appears in **Business Central Account Statistics** quick view form of accounts that are coupled to [!INCLUDE[d365fin](includes/d365fin_md.md)] customers.</span></span><br /><br /> <span data-ttu-id="fd4d7-180">Эти данные можно также обновлять вручную из каждой записи клиента.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-180">This data can also be updated manually from each customer record.</span></span> <span data-ttu-id="fd4d7-181">Дополнительные сведения см. в разделе [Практическое руководство. Связывание и синхронизация записей вручную](admin-how-to-couple-and-synchronize-records-manually.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-181">For more information, see [How to: Couple and Synchronize Records Manually](admin-how-to-couple-and-synchronize-records-manually.md).</span></span> </BR></BR><span data-ttu-id="fd4d7-182">**Примечание.** Эта запись очереди заданий используется только в случае установки решения интеграции [!INCLUDE[d365fin](includes/d365fin_md.md)] в [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd4d7-182">**Note:**  This job queue entry is relevant only if the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution is installed in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="fd4d7-183">Дополнительные сведения см. в разделе [О решении интеграции Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).</span><span class="sxs-lookup"><span data-stu-id="fd4d7-183">For more information, see [About the Business Central Integration Solution](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).</span></span>|<span data-ttu-id="fd4d7-184">Неприменимо.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-184">Not applicable.</span></span>|<span data-ttu-id="fd4d7-185">Неприменимо.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-185">Not applicable.</span></span>|   

## <a name="to-view-the-synchronization-job-log"></a><span data-ttu-id="fd4d7-186">Просмотр журнала заданий синхронизации</span><span class="sxs-lookup"><span data-stu-id="fd4d7-186">To view the synchronization job log</span></span>  
1. <span data-ttu-id="fd4d7-187">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал синхронизации интеграции**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-187">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Integration Synchronization Log**, and then choose the related link.</span></span>
2.  <span data-ttu-id="fd4d7-188">Если при выполнении задания синхронизации произошла одна или несколько ошибок, количество ошибок отображается в столбце **Ошибки**.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-188">If one or more error occurred for a synchronization job, the number of errors appears in the **Failed** column.</span></span> <span data-ttu-id="fd4d7-189">Для просмотра ошибок по заданию выберите номер.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-189">To view the errors for the job, choose the number.</span></span>  

    > [!TIP]  
    >  <span data-ttu-id="fd4d7-190">Можно просмотреть все ошибки задания синхронизации, открыв журнал ошибок задания синхронизации вручную.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-190">You can view all synchronization job errors by opening the synchronization job error log directly.</span></span>

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a><span data-ttu-id="fd4d7-191">Просмотр журнала заданий синхронизации из сопоставлений таблиц</span><span class="sxs-lookup"><span data-stu-id="fd4d7-191">To view the synchronization job log from the table mappings</span></span>  
1. <span data-ttu-id="fd4d7-192">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Сопоставления таблиц интеграции**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-192">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Integration Table Mappings**, and then choose the related link.</span></span>
2.  <span data-ttu-id="fd4d7-193">На странице **Сопоставления таблиц интеграции** выберите запись, затем выберите **Журнал заданий синхронизации интеграции**.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-193">In the **Integration Table Mappings** page, select an entry, and then choose **Integration Synch. Job Log**.</span></span>  

## <a name="to-view-the-synchronization-error-log"></a><span data-ttu-id="fd4d7-194">Просмотр журнала ошибок синхронизации</span><span class="sxs-lookup"><span data-stu-id="fd4d7-194">To view the synchronization error log</span></span>  
* <span data-ttu-id="fd4d7-195">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Ошибки синхронизации интеграции**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="fd4d7-195">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Integration Synchronization Errors**, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd4d7-196">См. также</span><span class="sxs-lookup"><span data-stu-id="fd4d7-196">See Also</span></span>  
[<span data-ttu-id="fd4d7-197">Синхронизация данных в Business Central и Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-197">Synchronizing Data in Business Central and Dynamics 365 for Sales</span></span>](admin-synchronizing-business-central-and-sales.md)  
[<span data-ttu-id="fd4d7-198">Ручная синхронизация сопоставлений таблиц</span><span class="sxs-lookup"><span data-stu-id="fd4d7-198">Manually Synchronize Table Mappings</span></span>](admin-manual-synchronization-of-table-mappings.md)  
[<span data-ttu-id="fd4d7-199">Планирование синхронизации между Business Central и Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-199">Scheduling a Synchronization between Business Central and Dynamics 365 for Sales</span></span>](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[<span data-ttu-id="fd4d7-200">Об интеграции Dynamics 365 Business Central с Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="fd4d7-200">About Integrating Dynamics 365 Business Central with Dynamics 365 for Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  


