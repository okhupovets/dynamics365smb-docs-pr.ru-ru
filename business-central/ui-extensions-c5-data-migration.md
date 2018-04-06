---
title: "Использование расширения \"Миграция данных C5\" | Microsoft Docs"
description: "Используйте это расширение для переноса клиентов, поставщиков, товаров и счетов главной книги из Microsoft Dynamics C5 2012 в Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f2b7f66de1caa63edaeb240b35501fb62645c469
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="3ba90-103">Расширение "Миграция данных C5" для Business Central</span><span class="sxs-lookup"><span data-stu-id="3ba90-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="3ba90-104">Это расширение упрощает перенос клиентов, поставщиков, товаров и ваших счетов главной книги из Microsoft Dynamics C5 2012 в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3ba90-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3ba90-105">Также можно перенести архивные операции для счетов главной книги.</span><span class="sxs-lookup"><span data-stu-id="3ba90-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="3ba90-106">Организация в [!INCLUDE[d365fin](includes/d365fin_md.md)] не должна содержать никаких данных.</span><span class="sxs-lookup"><span data-stu-id="3ba90-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="3ba90-107">Кроме того, после запуска миграции не создавайте клиентов, поставщиков, товаров или счетов, пока миграция не закончит работу.</span><span class="sxs-lookup"><span data-stu-id="3ba90-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="3ba90-108">Какие данные можно перенести?</span><span class="sxs-lookup"><span data-stu-id="3ba90-108">What Data is Migrated?</span></span>
<span data-ttu-id="3ba90-109">Следующие данные можно перенести для каждого объекта:</span><span class="sxs-lookup"><span data-stu-id="3ba90-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="3ba90-110">**Клиенты**</span><span class="sxs-lookup"><span data-stu-id="3ba90-110">**Customers**</span></span>
* <span data-ttu-id="3ba90-111">Склады</span><span class="sxs-lookup"><span data-stu-id="3ba90-111">Location</span></span>
* <span data-ttu-id="3ba90-112">Страна</span><span class="sxs-lookup"><span data-stu-id="3ba90-112">Country</span></span>
* <span data-ttu-id="3ba90-113">Измерения клиента (отдел, центр, назначение)</span><span class="sxs-lookup"><span data-stu-id="3ba90-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="3ba90-114">Метод поставки</span><span class="sxs-lookup"><span data-stu-id="3ba90-114">Shipment method</span></span>
* <span data-ttu-id="3ba90-115">Продавец</span><span class="sxs-lookup"><span data-stu-id="3ba90-115">Sales Person</span></span>
* <span data-ttu-id="3ba90-116">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="3ba90-116">Payment terms</span></span>
* <span data-ttu-id="3ba90-117">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="3ba90-117">Payment method</span></span>
* <span data-ttu-id="3ba90-118">Ценовая группа клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-118">Customer price group</span></span>
* <span data-ttu-id="3ba90-119">Скидка по счету клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-119">Customer invoice discount</span></span>

<span data-ttu-id="3ba90-120">При переносе учетной записи также переносятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="3ba90-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="3ba90-121">Настройка учета клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-121">Customer posting setup</span></span>
* <span data-ttu-id="3ba90-122">Раздел финансового журнала</span><span class="sxs-lookup"><span data-stu-id="3ba90-122">General journal batch</span></span>
* <span data-ttu-id="3ba90-123">Открытые транзакции (операции книги клиентов)</span><span class="sxs-lookup"><span data-stu-id="3ba90-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="3ba90-124">**Поставщики**</span><span class="sxs-lookup"><span data-stu-id="3ba90-124">**Vendors**</span></span>
* <span data-ttu-id="3ba90-125">Склады</span><span class="sxs-lookup"><span data-stu-id="3ba90-125">Location</span></span>
* <span data-ttu-id="3ba90-126">Страна</span><span class="sxs-lookup"><span data-stu-id="3ba90-126">Country</span></span>
* <span data-ttu-id="3ba90-127">Измерения поставщика (отдел, центр, назначение)</span><span class="sxs-lookup"><span data-stu-id="3ba90-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="3ba90-128">Скидка по счету</span><span class="sxs-lookup"><span data-stu-id="3ba90-128">Invoice discount</span></span>
* <span data-ttu-id="3ba90-129">Метод поставки</span><span class="sxs-lookup"><span data-stu-id="3ba90-129">Shipment method</span></span>
* <span data-ttu-id="3ba90-130">Закупщик</span><span class="sxs-lookup"><span data-stu-id="3ba90-130">Purchaser</span></span>
* <span data-ttu-id="3ba90-131">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="3ba90-131">Payment terms</span></span>
* <span data-ttu-id="3ba90-132">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="3ba90-132">Payment method</span></span>
* <span data-ttu-id="3ba90-133">Скидка по счету поставщика</span><span class="sxs-lookup"><span data-stu-id="3ba90-133">Vendor invoice discount</span></span>

<span data-ttu-id="3ba90-134">При переносе учетной записи также переносятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="3ba90-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="3ba90-135">Настройка учета поставщика</span><span class="sxs-lookup"><span data-stu-id="3ba90-135">Vendor posting setup</span></span>
* <span data-ttu-id="3ba90-136">Раздел финансового журнала</span><span class="sxs-lookup"><span data-stu-id="3ba90-136">General journal batch</span></span>
* <span data-ttu-id="3ba90-137">Открытые транзакции (операции книги поставщиков)</span><span class="sxs-lookup"><span data-stu-id="3ba90-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="3ba90-138">**Товаров**</span><span class="sxs-lookup"><span data-stu-id="3ba90-138">**Items**</span></span>
* <span data-ttu-id="3ba90-139">Склады</span><span class="sxs-lookup"><span data-stu-id="3ba90-139">Location</span></span>
* <span data-ttu-id="3ba90-140">Страна</span><span class="sxs-lookup"><span data-stu-id="3ba90-140">Country</span></span>
* <span data-ttu-id="3ba90-141">Измерения товара (отдел, центр, назначение)</span><span class="sxs-lookup"><span data-stu-id="3ba90-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="3ba90-142">Скидки строки продаж</span><span class="sxs-lookup"><span data-stu-id="3ba90-142">Sales line discounts</span></span>
* <span data-ttu-id="3ba90-143">Группы скидок клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-143">Customer discount groups</span></span>
* <span data-ttu-id="3ba90-144">Группы скидок по товару</span><span class="sxs-lookup"><span data-stu-id="3ba90-144">Item discount groups</span></span>
* <span data-ttu-id="3ba90-145">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="3ba90-145">Sales price</span></span>
* <span data-ttu-id="3ba90-146">Код тарифа</span><span class="sxs-lookup"><span data-stu-id="3ba90-146">Tariff number</span></span>
* <span data-ttu-id="3ba90-147">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="3ba90-147">Units of measure</span></span>
* <span data-ttu-id="3ba90-148">Код трассировки товара</span><span class="sxs-lookup"><span data-stu-id="3ba90-148">Item tracking code</span></span>
* <span data-ttu-id="3ba90-149">Ценовая группа клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-149">Customer price group</span></span>

<span data-ttu-id="3ba90-150">При переносе учетной записи также переносятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="3ba90-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="3ba90-151">Настройка учета запасов</span><span class="sxs-lookup"><span data-stu-id="3ba90-151">Inventory posting setup</span></span>
* <span data-ttu-id="3ba90-152">Общая настройка учета</span><span class="sxs-lookup"><span data-stu-id="3ba90-152">General posting setup</span></span>
* <span data-ttu-id="3ba90-153">Раздел журнала товаров</span><span class="sxs-lookup"><span data-stu-id="3ba90-153">Item journal batch</span></span>
* <span data-ttu-id="3ba90-154">Открытые транзакции (операции книги товаров)</span><span class="sxs-lookup"><span data-stu-id="3ba90-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="3ba90-155">При наличии открытых транзакций, использующих иностранные валюты, также переносятся валютные курсы для этих валют.</span><span class="sxs-lookup"><span data-stu-id="3ba90-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="3ba90-156">Другие валютные курсы не переносятся.</span><span class="sxs-lookup"><span data-stu-id="3ba90-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="3ba90-157">Для миграции данных</span><span class="sxs-lookup"><span data-stu-id="3ba90-157">To migrate data</span></span>
<span data-ttu-id="3ba90-158">Для экспорта данных из C5 и импорта их в [!INCLUDE[d365fin](includes/d365fin_md.md)] нужно выполнить всего несколько шагов:</span><span class="sxs-lookup"><span data-stu-id="3ba90-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="3ba90-159">В C5, используйте функцию **Экспорт базы данных**, чтобы экспортировать данные.</span><span class="sxs-lookup"><span data-stu-id="3ba90-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="3ba90-160">Затем отправьте папку экспорта в сжатую (ZIP) папку.</span><span class="sxs-lookup"><span data-stu-id="3ba90-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="3ba90-161">В [!INCLUDE[d365fin](includes/d365fin_md.md)] выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Миграция данных**, затем выберите **Миграция данных**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="3ba90-162">Выполните шаги облегчить в мастере настройки.</span><span class="sxs-lookup"><span data-stu-id="3ba90-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="3ba90-163">Обязательно выберите в качестве источника данных **Импорт из Microsoft Dynamcis C5 2012**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="3ba90-164">Организации часто добавляют поля для настройки C5 для определенной сферы деятельности.</span><span class="sxs-lookup"><span data-stu-id="3ba90-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="3ba90-165"> не производит миграцию данных из настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="3ba90-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="3ba90-166">Кроме того, миграция потерпит неудачу, если имеется более 10 настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="3ba90-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="3ba90-167">Просмотр состояния миграции</span><span class="sxs-lookup"><span data-stu-id="3ba90-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="3ba90-168">Используйте страницу **Обзор миграции данных** для контроля успешности миграции.</span><span class="sxs-lookup"><span data-stu-id="3ba90-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="3ba90-169">На этой странице отображается такая информация, как количество объектов, которые будут включены в миграцию, состояние миграции, количество элементов, для который была произведена миграция, и была ли эта миграция успешной.</span><span class="sxs-lookup"><span data-stu-id="3ba90-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="3ba90-170">Также отображается число ошибок, позволяет вам определить, что пошло неправильно, и, когда это возможно, позволяет легко перейти к объекту для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="3ba90-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="3ba90-171">Дополнительные сведения см. в следующем разделе этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3ba90-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="3ba90-172">Пока результаты миграции еще ожидаются, следует обновить страницу для отображения результатов.</span><span class="sxs-lookup"><span data-stu-id="3ba90-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="3ba90-173">Исправление ошибок</span><span class="sxs-lookup"><span data-stu-id="3ba90-173">Correcting Errors</span></span>
<span data-ttu-id="3ba90-174">Если что-то пошло не так и возникли ошибки, в поле **Состояние** отображается **Завершено с ошибками**, а в поле **Число ошибок** отображается количество ошибок.</span><span class="sxs-lookup"><span data-stu-id="3ba90-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="3ba90-175">Для просмотра списка ошибок можно открыть страницу **Ошибки миграции данных**, выбрав:</span><span class="sxs-lookup"><span data-stu-id="3ba90-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="3ba90-176">Номер в поле **Число ошибок** для объекта.</span><span class="sxs-lookup"><span data-stu-id="3ba90-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="3ba90-177">Объект, затем действие **Показать ошибки**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="3ba90-178">На странице **Ошибки миграции данных** чтобы исправить ошибку, можно выбрать сообщение об ошибке, затем выбрать **Изменить запись** для открытия страницы, которая показывает перенесенные данные для объекта.</span><span class="sxs-lookup"><span data-stu-id="3ba90-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="3ba90-179">После исправления одной или нескольких ошибок можно выбрать **Миграция**, чтобы выполнить перенос только исправленных объектов, без необходимости полного повторного выполнения миграции.</span><span class="sxs-lookup"><span data-stu-id="3ba90-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="3ba90-180">Если исправлено несколько ошибок, можно использовать функцию **Выбрать больше**, чтобы выбрать несколько строк для миграции.</span><span class="sxs-lookup"><span data-stu-id="3ba90-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="3ba90-181">Если же ошибки не важны и их можно не исправлять, можно выбрать их, затем выбрать **Пропустить выбранные элементы**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="3ba90-182">Если имеются товары, которые включены в спецификацию, может возникнуть необходимость выполнить миграцию несколько раз, если исходный товар не был создан до вариантов, которые ссылаются на него.</span><span class="sxs-lookup"><span data-stu-id="3ba90-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="3ba90-183">Если сначала создается вариант товара, то ссылка на исходный товару может привести к появлению сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3ba90-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="3ba90-184">Проверка данных после миграции</span><span class="sxs-lookup"><span data-stu-id="3ba90-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="3ba90-185">Если требуется проверять правильность миграции данных, можно просмотреть следующие страницы в C5 и [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3ba90-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="3ba90-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="3ba90-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="3ba90-187">Объекты клиента</span><span class="sxs-lookup"><span data-stu-id="3ba90-187">Customer Entries</span></span>| <span data-ttu-id="3ba90-188">Финансовые журналы</span><span class="sxs-lookup"><span data-stu-id="3ba90-188">General Journals</span></span>|
|<span data-ttu-id="3ba90-189">Объекты поставщика</span><span class="sxs-lookup"><span data-stu-id="3ba90-189">Vendor Entries</span></span>| <span data-ttu-id="3ba90-190">Финансовые журналы</span><span class="sxs-lookup"><span data-stu-id="3ba90-190">General Journals</span></span>|
|<span data-ttu-id="3ba90-191">Операции товара</span><span class="sxs-lookup"><span data-stu-id="3ba90-191">Item Entries</span></span>| <span data-ttu-id="3ba90-192">Журналы товаров</span><span class="sxs-lookup"><span data-stu-id="3ba90-192">Item Journals</span></span>|

<span data-ttu-id="3ba90-193">В [!INCLUDE[d365fin](includes/d365fin_md.md)] пакет для перенесенных данных называется **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="3ba90-194">Остановка миграции данных</span><span class="sxs-lookup"><span data-stu-id="3ba90-194">Stopping Data Migration</span></span>
<span data-ttu-id="3ba90-195">Можно остановить миграцию данных, выбрав **Остановить все операции миграции**.</span><span class="sxs-lookup"><span data-stu-id="3ba90-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="3ba90-196">Если это сделать, все ожидающие операции миграции также будут остановлены.</span><span class="sxs-lookup"><span data-stu-id="3ba90-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ba90-197">См. также</span><span class="sxs-lookup"><span data-stu-id="3ba90-197">See Also</span></span>
<span data-ttu-id="3ba90-198">[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)] с помощью расширений](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3ba90-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="3ba90-199">[Добро пожаловать в [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="3ba90-199">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  
