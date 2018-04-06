---
title: "Создание новой организации | Документы Майкрософт"
description: "Для использования служб RapidStart Services создаются таблицы и страницы, но они не содержат никаких данных."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="3ce68-103">Создание новой организации</span><span class="sxs-lookup"><span data-stu-id="3ce68-103">Create a New Company</span></span>
<span data-ttu-id="3ce68-104">Для использования служб RapidStart Services для [!INCLUDE[d365fin](includes/d365fin_md.md)] необходимо сначала создать новую организацию, для которой необходимо выполнить реализацию клиента.</span><span class="sxs-lookup"><span data-stu-id="3ce68-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="3ce68-105">При создании новой организации создаются стандартные таблицы и страницы [!INCLUDE[d365fin](includes/d365fin_md.md)], но без сведений.</span><span class="sxs-lookup"><span data-stu-id="3ce68-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="3ce68-106">Кроме того, можно применить специфические данные настройки организации после ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="3ce68-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="3ce68-107">Информация предоставляется в пакете конфигурации (файл с расширением RAPIDSTAR), который хранит данные в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="3ce68-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="3ce68-108">Примеры пакетов конфигурации, включая файлы для определенных стран и регионов, поставляются вместе с демонстрационной организацией CRONUS.</span><span class="sxs-lookup"><span data-stu-id="3ce68-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="3ce68-109">Используйте следующую процедуру для использования примера пакета конфигураций в новой компании.</span><span class="sxs-lookup"><span data-stu-id="3ce68-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="3ce68-110">Использование образца пакета конфигурации BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="3ce68-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="3ce68-111">Откройте демонстрационную организацию «CRONUS Россия ЗАО».</span><span class="sxs-lookup"><span data-stu-id="3ce68-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="3ce68-112">Дополнительные сведения см. в разделе [Изменение базовых настроек](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="3ce68-113">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Пакеты конфигурации**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="3ce68-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="3ce68-114">Выберите пакет BASICCONFIG из списка и выберите действие **Экспортировать пакет**.</span><span class="sxs-lookup"><span data-stu-id="3ce68-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="3ce68-115">Используйте следующую процедуру для создания новой организации и в процессе используйте пакет BASICCONFIG.</span><span class="sxs-lookup"><span data-stu-id="3ce68-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="3ce68-116">Создание организации</span><span class="sxs-lookup"><span data-stu-id="3ce68-116">To create a new company</span></span>  
1. <span data-ttu-id="3ce68-117">Создать новую компанию.</span><span class="sxs-lookup"><span data-stu-id="3ce68-117">Create a new company.</span></span> <span data-ttu-id="3ce68-118">Дополнительную информацию см. в разделе [Создание новой организации в [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="3ce68-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="3ce68-119">Из ролевого центра «Внедряющий мастер служб RapidStart Services» теперь можно импортировать пакет конфигурации, который вы экспортировали из организации «CRONUS Россия ЗАО».</span><span class="sxs-lookup"><span data-stu-id="3ce68-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="3ce68-120">После создания новой организации некоторые таблицы заполняются автоматически, даже если не применен ни один шаблон организации.</span><span class="sxs-lookup"><span data-stu-id="3ce68-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="3ce68-121">Например, можно просмотреть стандартные коды для транзакций учета и пакетных транзакций в окне **Код источника**.</span><span class="sxs-lookup"><span data-stu-id="3ce68-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="3ce68-122">Если нужно предоставить локальную версию [!INCLUDE[d365fin](includes/d365fin_md.md)], следует просмотреть эту таблицу и изучить вопросы, связанные с языками.</span><span class="sxs-lookup"><span data-stu-id="3ce68-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="3ce68-123">О таблицах данных</span><span class="sxs-lookup"><span data-stu-id="3ce68-123">About Data Tables</span></span>
<span data-ttu-id="3ce68-124">Таблицы данных [!INCLUDE[d365fin](includes/d365fin_md.md)] доступны в двух основных видах: основная таблица и таблица настройки.</span><span class="sxs-lookup"><span data-stu-id="3ce68-124">[!INCLUDE[d365fin](includes/d365fin_md.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="3ce68-125">При настойке конфигурации компании можно использовать эти типы, чтобы ориентироваться на стратегию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ce68-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="3ce68-126">Таблицы основных данных</span><span class="sxs-lookup"><span data-stu-id="3ce68-126">Master Data Tables</span></span>  
<span data-ttu-id="3ce68-127">В следующей таблице приведены некоторые из таблиц основных данных.</span><span class="sxs-lookup"><span data-stu-id="3ce68-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="3ce68-128">При инициализации новой организации эти таблицы будут пустыми.</span><span class="sxs-lookup"><span data-stu-id="3ce68-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="3ce68-129">Номер таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-129">Table No.</span></span>|<span data-ttu-id="3ce68-130">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3ce68-131">15</span><span class="sxs-lookup"><span data-stu-id="3ce68-131">15</span></span>|<span data-ttu-id="3ce68-132">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="3ce68-132">G/L Account</span></span>|  
|<span data-ttu-id="3ce68-133">18</span><span class="sxs-lookup"><span data-stu-id="3ce68-133">18</span></span>|<span data-ttu-id="3ce68-134">Клиент</span><span class="sxs-lookup"><span data-stu-id="3ce68-134">Customer</span></span>|  
|<span data-ttu-id="3ce68-135">23</span><span class="sxs-lookup"><span data-stu-id="3ce68-135">23</span></span>|<span data-ttu-id="3ce68-136">Поставщик</span><span class="sxs-lookup"><span data-stu-id="3ce68-136">Vendor</span></span>|  
|<span data-ttu-id="3ce68-137">27</span><span class="sxs-lookup"><span data-stu-id="3ce68-137">27</span></span>|<span data-ttu-id="3ce68-138">Пункт меню</span><span class="sxs-lookup"><span data-stu-id="3ce68-138">Item</span></span>|  
|<span data-ttu-id="3ce68-139">5050</span><span class="sxs-lookup"><span data-stu-id="3ce68-139">5050</span></span>|<span data-ttu-id="3ce68-140">Контакт</span><span class="sxs-lookup"><span data-stu-id="3ce68-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="3ce68-141">Настройка таблиц данных</span><span class="sxs-lookup"><span data-stu-id="3ce68-141">Setup Data Tables</span></span>  
<span data-ttu-id="3ce68-142">В следующей таблице перечислены некоторые из таблиц данных настройки, в которых фиксируются сведения о настройке в анкете конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ce68-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="3ce68-143">Эти таблицы содержат базовые данные, когда организация создается.</span><span class="sxs-lookup"><span data-stu-id="3ce68-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="3ce68-144">Номер таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-144">Table No.</span></span>|<span data-ttu-id="3ce68-145">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3ce68-146">98</span><span class="sxs-lookup"><span data-stu-id="3ce68-146">98</span></span>|<span data-ttu-id="3ce68-147">Настройка ГК</span><span class="sxs-lookup"><span data-stu-id="3ce68-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="3ce68-148">311</span><span class="sxs-lookup"><span data-stu-id="3ce68-148">311</span></span>|<span data-ttu-id="3ce68-149">Настройка модуля "Продажи и дебитор. задолж."</span><span class="sxs-lookup"><span data-stu-id="3ce68-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="3ce68-150">312</span><span class="sxs-lookup"><span data-stu-id="3ce68-150">312</span></span>|<span data-ttu-id="3ce68-151">Настройка модуля "Покупки и кредиторская задолженность"</span><span class="sxs-lookup"><span data-stu-id="3ce68-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="3ce68-152">313</span><span class="sxs-lookup"><span data-stu-id="3ce68-152">313</span></span>|<span data-ttu-id="3ce68-153">Настройка модуля "Запасы"</span><span class="sxs-lookup"><span data-stu-id="3ce68-153">Inventory Setup</span></span>|  

<span data-ttu-id="3ce68-154">В дополнение к таблицам данных настроек [!INCLUDE[d365fin](includes/d365fin_md.md)] также имеет таблицы данных типа настройки, в которых указаны основные сведения об организации и ее бизнес-процессах.</span><span class="sxs-lookup"><span data-stu-id="3ce68-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="3ce68-155">В следующей таблице перечислены некоторые из них.</span><span class="sxs-lookup"><span data-stu-id="3ce68-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="3ce68-156">Номер таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-156">Table No.</span></span>|<span data-ttu-id="3ce68-157">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="3ce68-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="3ce68-158">3</span><span class="sxs-lookup"><span data-stu-id="3ce68-158">3</span></span>|<span data-ttu-id="3ce68-159">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="3ce68-159">Payment Terms</span></span>|  
|<span data-ttu-id="3ce68-160">4</span><span class="sxs-lookup"><span data-stu-id="3ce68-160">4</span></span>|<span data-ttu-id="3ce68-161">Валюта</span><span class="sxs-lookup"><span data-stu-id="3ce68-161">Currency</span></span>|  
|<span data-ttu-id="3ce68-162">6</span><span class="sxs-lookup"><span data-stu-id="3ce68-162">6</span></span>|<span data-ttu-id="3ce68-163">Ценовые группы клиентов</span><span class="sxs-lookup"><span data-stu-id="3ce68-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="3ce68-164">5700</span><span class="sxs-lookup"><span data-stu-id="3ce68-164">5700</span></span>|<span data-ttu-id="3ce68-165">Единица хранения</span><span class="sxs-lookup"><span data-stu-id="3ce68-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="3ce68-166">См. также</span><span class="sxs-lookup"><span data-stu-id="3ce68-166">See Also</span></span>  
[<span data-ttu-id="3ce68-167">Применение конфигураций к новым организациям</span><span class="sxs-lookup"><span data-stu-id="3ce68-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="3ce68-168">Настройка компании с помощью служб RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="3ce68-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="3ce68-169">Администрация</span><span class="sxs-lookup"><span data-stu-id="3ce68-169">Administration</span></span>](admin-setup-and-administration.md)
