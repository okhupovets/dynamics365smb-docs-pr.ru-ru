---
title: "Поиск данных и ввод критериев фильтра | Документы Майкрософт"
description: "Описывается порядок работы с фильтрами, например с быстрым фильтром, для уточнения результатов поиска данных."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7fd74ad235e51b1793b02e19834bdb0bd17820b
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="e9ce3-103">Поиск, фильтрация и сортировка данных</span><span class="sxs-lookup"><span data-stu-id="e9ce3-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="e9ce3-104">Есть несколько вещей, которые могут помочь искать, определять местоположение и сканировать записи в списке.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="e9ce3-105">Сюда входят сортировка, поиск и фильтрация.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="e9ce3-106">Если необходимо выполнить поиск данных, таких как название клиента, адреса или товарные группы, вводятся критерии.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="e9ce3-107">В критериях поиска можно использовать все цифры и буквы, которые вводятся в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="e9ce3-108">Кроме того, для дополнительной фильтрации результатов можно использовать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="e9ce3-109">Существует два способа поиска: с помощью экспресс-фильтра или фильтров столбцов.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="e9ce3-110">Сортировка</span><span class="sxs-lookup"><span data-stu-id="e9ce3-110">Sorting</span></span>
<span data-ttu-id="e9ce3-111">Сортировка позволяет быстро и легко получить общее представление о данных.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="e9ce3-112">При наличии большого числа клиентов, например, можно сортировать их по полю **Номер клиента**, **Учетная группа клиента**, **Код валюты**, **Код страны/региона** или **ИНН**, чтобы получить нужный обзор.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="e9ce3-113">Для сортировки списка можно либо выбрать текст заголовка столбца для переключения между порядком по возрастания или по убыванию, либо выбрать небольшую стрелку вниз в заголовке столбца, затем выбрать **По возрастанию** или **По убыванию**.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e9ce3-114">Не поддерживается сортировка изображений, полей BLOB, полей FlowFilter и полей, которые не принадлежат таблице.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="e9ce3-115">Поиск с помощью экспресс-фильтра</span><span class="sxs-lookup"><span data-stu-id="e9ce3-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="e9ce3-116">Вы можете добавить фильтры на все страницы с помощью экспресс-фильтра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="e9ce3-117">Экспресс-фильтр включается при выборе значка лупы в правом верхнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="e9ce3-118">Данный тип фильтра используется для быстрого ввода критериев.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="e9ce3-119">Экспресс-фильтр обеспечивает удобный доступ к фильтруемым данным путем ввода простого текста, а также множество вариантов указания критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="e9ce3-120">В зависимости от того, введен ли обычный текст или текст с символами, поведение экспресс-фильтра отличается.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="e9ce3-121">Если в критериях поиска ввести обычный текст, критерии поиска будут рассматриваться без учета регистра и будет выполняться поиск определенного текста.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="e9ce3-122">Если в критериях поиска ввести тест с символами, критерии поиска будут рассматриваться с учетом регистра и будет выполняться поиск точного текста.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="e9ce3-123">Критерии экспресс-фильтра</span><span class="sxs-lookup"><span data-stu-id="e9ce3-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="e9ce3-124">Критерии поиска</span><span class="sxs-lookup"><span data-stu-id="e9ce3-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="e9ce3-125">Интерпретируется как…</span><span class="sxs-lookup"><span data-stu-id="e9ce3-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="e9ce3-126">Возвращает…</span><span class="sxs-lookup"><span data-stu-id="e9ce3-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="e9ce3-127">man</span><span class="sxs-lookup"><span data-stu-id="e9ce3-127">man</span></span></TD>
    <TD><span data-ttu-id="e9ce3-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="e9ce3-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="e9ce3-129">Все записи, содержащие текст <b>man</b>, без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="e9ce3-130">se</span><span class="sxs-lookup"><span data-stu-id="e9ce3-130">se</span></span></TD>
    <TD><span data-ttu-id="e9ce3-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="e9ce3-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="e9ce3-132">Все записи, содержащие текст <b>se</b>, без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="e9ce3-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="e9ce3-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="e9ce3-134">Начинается с <b>Man</b> с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="e9ce3-135">Все записи, которые начинаются с текста <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="e9ce3-136">'man'</span><span class="sxs-lookup"><span data-stu-id="e9ce3-136">'man'</span></span></TD>
    <TD><span data-ttu-id="e9ce3-137">Точный текст с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="e9ce3-138">Все записи, которые в точности соответствуют <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="e9ce3-139">@man\*</span><span class="sxs-lookup"><span data-stu-id="e9ce3-139">@man\*</span></span> </TD>
    <TD><span data-ttu-id="e9ce3-140">Начинается на man без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="e9ce3-141">Все записи, которые начинаются на <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="e9ce3-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="e9ce3-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="e9ce3-143">Заканчивается на man без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="e9ce3-144">Все записи, которые заканчиваются на <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="e9ce3-145">Нельзя использовать подстановочные символы при фильтрации в полях перечислений, например в поле **Статус** заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="e9ce3-146">Чтобы ввести фильтр для данного типа поля, можно ввести в качестве параметра фильтра числовое значение.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="e9ce3-147">Например, в поле **Статус** в заказе на продажу, которое имеет значения **Открыть**, **Выпущено**, **Ожидает утверждения** и **Ожидает предоплаты**, используйте значения **0**, **1**, **2**, и **3** для фильтрации этих параметров.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="e9ce3-148">Поиск с помощью фильтров столбцов</span><span class="sxs-lookup"><span data-stu-id="e9ce3-148">Searching by using column Filters</span></span>
<span data-ttu-id="e9ce3-149">Можно добавить фильтр на один или несколько столбцов в списке.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="e9ce3-150">Фильтрация по столбцах обеспечивает большую гибкость и возможности, чем экспресс-фильтр.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="e9ce3-151">Добавление фильтра в столбец</span><span class="sxs-lookup"><span data-stu-id="e9ce3-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="e9ce3-152">Прежде чем добавлять фильтр, выберите значок ![Показать как список](media/ui_show_as_list_icon.png "Стрелка влево, показать как список"), чтобы переключиться в представление списка.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="e9ce3-153">Выберите стрелку вниз в заголовке столбца, затем выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="e9ce3-154">Выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="e9ce3-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="e9ce3-155">Выберите *...* рядом с полем для выбора значения из списка.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="e9ce3-156">Введите критерии фильтра в поле.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="e9ce3-157">Подробнее см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-157">See the next section for details.</span></span>
4. <span data-ttu-id="e9ce3-158">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="e9ce3-159">Критерии фильтра и символы</span><span class="sxs-lookup"><span data-stu-id="e9ce3-159">Filter criteria and symbols</span></span>
<span data-ttu-id="e9ce3-160">В процессе установки критериев фильтра можно использовать все цифры и буквы, которые обычно вводятся в поле.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="e9ce3-161">Кроме того, для дополнительной фильтрации результатов можно использовать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="e9ce3-162">В следующих таблицах приведены символы, которые могут быть использованы в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="e9ce3-163">Могут быть ситуации, когда значения поля содержит эти символы, и требуется фильтрация по ним.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="e9ce3-164">Чтобы это сделать, необходимо включить выражение фильтра, которое содержит данный символ в кавычках (").</span><span class="sxs-lookup"><span data-stu-id="e9ce3-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="e9ce3-165">Например, если необходимо фильтровать записи, которые начинаются с текста *S&R*, выражение фильтра имеет вид **'S&R\*'**.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R\*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="e9ce3-166">(..) Диапазон</span><span class="sxs-lookup"><span data-stu-id="e9ce3-166">(..) Interval</span></span>  
  
|<span data-ttu-id="e9ce3-167">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-167">Sample Expression</span></span>|<span data-ttu-id="e9ce3-168">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-169">1 100..2 100</span><span class="sxs-lookup"><span data-stu-id="e9ce3-169">1100..2100</span></span>|<span data-ttu-id="e9ce3-170">Номера от 1 100 до 2 100</span><span class="sxs-lookup"><span data-stu-id="e9ce3-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="e9ce3-171">..2 500</span><span class="sxs-lookup"><span data-stu-id="e9ce3-171">..2500</span></span>|<span data-ttu-id="e9ce3-172">До 2500, включительно</span><span class="sxs-lookup"><span data-stu-id="e9ce3-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="e9ce3-173">..31.12.00</span><span class="sxs-lookup"><span data-stu-id="e9ce3-173">..12 31 00</span></span>|<span data-ttu-id="e9ce3-174">Даты по 31.12.00 включительно</span><span class="sxs-lookup"><span data-stu-id="e9ce3-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="e9ce3-175">P8..</span><span class="sxs-lookup"><span data-stu-id="e9ce3-175">P8..</span></span>|<span data-ttu-id="e9ce3-176">Информация для 8-го учетного периода и позже.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="e9ce3-177">..23</span><span class="sxs-lookup"><span data-stu-id="e9ce3-177">..23</span></span>|<span data-ttu-id="e9ce3-178">С даты начала по 23 число текущего месяца текущего года до 23:59:59</span><span class="sxs-lookup"><span data-stu-id="e9ce3-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="e9ce3-179">23..</span><span class="sxs-lookup"><span data-stu-id="e9ce3-179">23..</span></span>|<span data-ttu-id="e9ce3-180">с 23 текущего месяца текущего года 00:00:00 до конца</span><span class="sxs-lookup"><span data-stu-id="e9ce3-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="e9ce3-181">22..23</span><span class="sxs-lookup"><span data-stu-id="e9ce3-181">22..23</span></span>|<span data-ttu-id="e9ce3-182">с 22 текущего месяца текущего года 0:00:00 по 23 текущего месяца текущего года 23:59:59</span><span class="sxs-lookup"><span data-stu-id="e9ce3-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="e9ce3-183">(&#124;) Либо/или</span><span class="sxs-lookup"><span data-stu-id="e9ce3-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="e9ce3-184">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-184">Sample Expression</span></span>|<span data-ttu-id="e9ce3-185">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="e9ce3-186">1200&#124;1300</span></span>|<span data-ttu-id="e9ce3-187">Номера со значением 1 200 или 1 300</span><span class="sxs-lookup"><span data-stu-id="e9ce3-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="e9ce3-188">(<>) Не равно</span><span class="sxs-lookup"><span data-stu-id="e9ce3-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="e9ce3-189">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-189">Sample Expression</span></span>|<span data-ttu-id="e9ce3-190">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-191"><>0</span><span class="sxs-lookup"><span data-stu-id="e9ce3-191"><>0</span></span>|<span data-ttu-id="e9ce3-192">Все числа, кроме 0</span><span class="sxs-lookup"><span data-stu-id="e9ce3-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="e9ce3-193">Возможность использования Microsoft SQL Server позволяет комбинировать данный символ со знаками подстановки.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="e9ce3-194">Например, <>A\* означает несоответствие любым текстам, начинающимся с А.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-194">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="e9ce3-195">(>) Больше чем</span><span class="sxs-lookup"><span data-stu-id="e9ce3-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="e9ce3-196">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-196">Sample Expression</span></span>|<span data-ttu-id="e9ce3-197">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-198">>1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-198">>1200</span></span>|<span data-ttu-id="e9ce3-199">Числа больше, чем 1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="e9ce3-200">(>=) Больше чем или равно</span><span class="sxs-lookup"><span data-stu-id="e9ce3-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="e9ce3-201">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-201">Sample Expression</span></span>|<span data-ttu-id="e9ce3-202">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-203">>=1200</span></span>|<span data-ttu-id="e9ce3-204">Номера больше или равны 1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="e9ce3-205">(<) Меньше чем</span><span class="sxs-lookup"><span data-stu-id="e9ce3-205">(<) Less than</span></span>  
  
|<span data-ttu-id="e9ce3-206">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-206">Sample Expression</span></span>|<span data-ttu-id="e9ce3-207">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-208"><1200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-208"><1200</span></span>|<span data-ttu-id="e9ce3-209">Номера меньше, чем 1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="e9ce3-210">(<=) Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="e9ce3-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="e9ce3-211">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-211">Sample Expression</span></span>|<span data-ttu-id="e9ce3-212">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-213"><=1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-213"><=1200</span></span>|<span data-ttu-id="e9ce3-214">Номера меньше или равны 1 200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="e9ce3-215">(&) И</span><span class="sxs-lookup"><span data-stu-id="e9ce3-215">(&) And</span></span>  
  
|<span data-ttu-id="e9ce3-216">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-216">Sample Expression</span></span>|<span data-ttu-id="e9ce3-217">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-218">>200&<1200</span></span>|<span data-ttu-id="e9ce3-219">Числа больше 200 и меньше 1200</span><span class="sxs-lookup"><span data-stu-id="e9ce3-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="e9ce3-220">('') Точное совпадение символа</span><span class="sxs-lookup"><span data-stu-id="e9ce3-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="e9ce3-221">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-221">Sample Expression</span></span>|<span data-ttu-id="e9ce3-222">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-223">'man'</span><span class="sxs-lookup"><span data-stu-id="e9ce3-223">'man'</span></span>|<span data-ttu-id="e9ce3-224">Текст, точно соответствующий man с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="e9ce3-225">(@) Без учета регистра</span><span class="sxs-lookup"><span data-stu-id="e9ce3-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="e9ce3-226">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-226">Sample Expression</span></span>|<span data-ttu-id="e9ce3-227">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-228">@man\*</span><span class="sxs-lookup"><span data-stu-id="e9ce3-228">@man\*</span></span>|<span data-ttu-id="e9ce3-229">Текст, начинающийся с man без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="e9ce3-230">(\*) Неопределенное количество неизвестных символов</span><span class="sxs-lookup"><span data-stu-id="e9ce3-230">(\*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="e9ce3-231">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-231">Sample Expression</span></span>|<span data-ttu-id="e9ce3-232">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-233">*Ко*</span><span class="sxs-lookup"><span data-stu-id="e9ce3-233">*Co*</span></span>|<span data-ttu-id="e9ce3-234">Текст, который содержит "Ко" с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="e9ce3-235">\*Ко</span><span class="sxs-lookup"><span data-stu-id="e9ce3-235">\*Co</span></span>|<span data-ttu-id="e9ce3-236">Текст, который заканчивается на "Ко" с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="e9ce3-237">Ко\*</span><span class="sxs-lookup"><span data-stu-id="e9ce3-237">Co\*</span></span>|<span data-ttu-id="e9ce3-238">Текст, который начинается с "Ко" с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="e9ce3-239">(?) Один неизвестный символ</span><span class="sxs-lookup"><span data-stu-id="e9ce3-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="e9ce3-240">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-240">Sample Expression</span></span>|<span data-ttu-id="e9ce3-241">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-242">Ст?л</span><span class="sxs-lookup"><span data-stu-id="e9ce3-242">Hans?n</span></span>|<span data-ttu-id="e9ce3-243">Такой текст, как «Стул» или «Стол»</span><span class="sxs-lookup"><span data-stu-id="e9ce3-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="e9ce3-244">Объединенные выражения форматов</span><span class="sxs-lookup"><span data-stu-id="e9ce3-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="e9ce3-245">Образец выражения</span><span class="sxs-lookup"><span data-stu-id="e9ce3-245">Sample Expression</span></span>|<span data-ttu-id="e9ce3-246">Отображаемые записи</span><span class="sxs-lookup"><span data-stu-id="e9ce3-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="e9ce3-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="e9ce3-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="e9ce3-248">Включает все записи с номером 5999 или номерами от 8100 до 8490.</span><span class="sxs-lookup"><span data-stu-id="e9ce3-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="e9ce3-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="e9ce3-249">..1299&#124;1400..</span></span>|<span data-ttu-id="e9ce3-250">Все записи с номером меньше или равно 1299 или номером от 1400 или больше (все номера, кроме от 1300 до 1399).</span><span class="sxs-lookup"><span data-stu-id="e9ce3-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="e9ce3-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="e9ce3-251">>50&<100</span></span>|<span data-ttu-id="e9ce3-252">Все записи с номерами больше 50 и меньше 100 (номера от 51 до 99).</span><span class="sxs-lookup"><span data-stu-id="e9ce3-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="e9ce3-253">См. также</span><span class="sxs-lookup"><span data-stu-id="e9ce3-253">See Also</span></span>
<span data-ttu-id="e9ce3-254">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9ce3-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
