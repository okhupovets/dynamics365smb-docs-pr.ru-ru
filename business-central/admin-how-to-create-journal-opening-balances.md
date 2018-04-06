---
title: "Создание входящего сальдо журнала | Microsoft Docs"
description: "Business Central включает несколько пакетных заданий, которые помогают перенести предыдущие сальдо счетов в заново настроенную организацию. Можно легко перенести эти данные с помощью учета в журналах."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="4eae2-104">Создание входящего сальдо журнала</span><span class="sxs-lookup"><span data-stu-id="4eae2-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="4eae2-105"> включает несколько пакетных заданий, которые помогают перенести предыдущие сальдо счетов в заново настроенную организацию.</span><span class="sxs-lookup"><span data-stu-id="4eae2-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="4eae2-106">Можно легко перенести эти данные с помощью журнала клиентов, журнала поставщиков, журнала товаров или журнала ГК.</span><span class="sxs-lookup"><span data-stu-id="4eae2-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="4eae2-107">Первым этапом является создание пакета конфигурации, включающего таблицы настройки таких журналов.</span><span class="sxs-lookup"><span data-stu-id="4eae2-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="4eae2-108">Следующая процедура предполагает, что этот шаг выполнен.</span><span class="sxs-lookup"><span data-stu-id="4eae2-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="4eae2-109">Дополнительные сведения см. в разделе [Настройка конфигурации организации](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4eae2-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="4eae2-110">Эта процедура описывает последовательные действия, в число которых включается применение пакета, предоставленного партнером.</span><span class="sxs-lookup"><span data-stu-id="4eae2-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="4eae2-111">Перед началом убедитесь, что вы находитесь на странице ролевого центра «Внедряющий мастер служб RapidStart Services», так как она дает правильный контекст для вашей работы по конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4eae2-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="4eae2-112">Дополнительные сведения см. в разделе [Изменение базовых настроек](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4eae2-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="4eae2-113">Применение журнальных записей к новой организации</span><span class="sxs-lookup"><span data-stu-id="4eae2-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="4eae2-114">Настройте новую организацию и примените к ней пакет конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4eae2-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="4eae2-115">Дополнительные сведения см. в разделе [Настройка организации с помощью мастера RapidStart Services](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="4eae2-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="4eae2-116">Новая организация не содержит информацию о входящем сальдо журнала.</span><span class="sxs-lookup"><span data-stu-id="4eae2-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="4eae2-117">Откройте журнал конфигураций и импортируйте существующие данные о товарах, клиентах, поставщиках и Главной книге.</span><span class="sxs-lookup"><span data-stu-id="4eae2-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="4eae2-118">Дополнительные сведения см. в разделе [Миграция данных клиента](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="4eae2-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="4eae2-119">Выберите, например действие **Создать строки журнала ГК**.</span><span class="sxs-lookup"><span data-stu-id="4eae2-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="4eae2-120">Заполните экспресс-вкладку **Параметры** должным образом и по мере необходимости настройте фильтры.</span><span class="sxs-lookup"><span data-stu-id="4eae2-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="4eae2-121">Например, в поле **Шаблон журнала** введите описательное имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="4eae2-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="4eae2-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4eae2-122">Choose the **OK** button.</span></span> <span data-ttu-id="4eae2-123">Записи теперь находятся в журнале, но суммы не указаны.</span><span class="sxs-lookup"><span data-stu-id="4eae2-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="4eae2-124">Экспортируйте таблицу журнала в Excel и вручную введите информацию об учете и балансирующем счете из унаследованных данных.</span><span class="sxs-lookup"><span data-stu-id="4eae2-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="4eae2-125">Импортируйте и примените информацию о таблице в новой организации.</span><span class="sxs-lookup"><span data-stu-id="4eae2-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="4eae2-126">Строки журнала готовы к учету.</span><span class="sxs-lookup"><span data-stu-id="4eae2-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="4eae2-127">В журнале конфигураций выберите таблицу строки журнала, затем выберите действие **Данные базы данных**.</span><span class="sxs-lookup"><span data-stu-id="4eae2-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="4eae2-128">Проверьте информацию, затем выберите действие **Учет**.</span><span class="sxs-lookup"><span data-stu-id="4eae2-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="4eae2-129">Повторите эти шаги для импорта и учета всех других начальных балансов.</span><span class="sxs-lookup"><span data-stu-id="4eae2-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4eae2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4eae2-130">See Also</span></span>  
[<span data-ttu-id="4eae2-131">Применение конфигураций к новым организациям</span><span class="sxs-lookup"><span data-stu-id="4eae2-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="4eae2-132">Настройка компании с помощью служб RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="4eae2-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="4eae2-133">Администрация</span><span class="sxs-lookup"><span data-stu-id="4eae2-133">Administration</span></span>](admin-setup-and-administration.md)
