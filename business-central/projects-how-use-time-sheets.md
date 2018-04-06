---
title: "Использование табелей учета рабочего времени для работ | Документы Майкрософт"
description: "Описывается процедура создания табеля учета рабочего времени для работы, копирования строк планирования в него, определения видов работ, заполнения табеля учета рабочего времени и его отправки на утверждение."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: b70a73edda008994f3c7a4dc09ca9e875a020f6e
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="use-time-sheets-for-jobs"></a><span data-ttu-id="13a7b-103">Использование табелей учета рабочего времени для работ</span><span class="sxs-lookup"><span data-stu-id="13a7b-103">Use Time Sheets for Jobs</span></span>
<span data-ttu-id="13a7b-104">Используйте пакетное задание **Создать табели учета рабочего времени**, чтобы настроить табели для определенного количества периодов времени или недель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-104">You use the **Create Time Sheets** batch job to set up time sheets for a specified number of time periods or weeks.</span></span> <span data-ttu-id="13a7b-105">Вы должны иметь права на создание табелей.</span><span class="sxs-lookup"><span data-stu-id="13a7b-105">You must have permissions to be able to create time sheets.</span></span>

<span data-ttu-id="13a7b-106">Можно скопировать и использовать в табеле строки планирования работы.</span><span class="sxs-lookup"><span data-stu-id="13a7b-106">You can copy and use your job planning lines in a time sheet.</span></span> <span data-ttu-id="13a7b-107">В этом способе необходимо только ввести информацию для одного места, и информация в строке всегда будет правильной.</span><span class="sxs-lookup"><span data-stu-id="13a7b-107">In that way, you must only enter the information in one place and the line information is always correct.</span></span>

<span data-ttu-id="13a7b-108">После утверждения операций табеля для задания можно выполнять их учет в соответствующем журнале заданий или журнале ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a7b-108">After you have approved time sheet entries for a job, you can post them to the relevant job journal or resource journal.</span></span>

<span data-ttu-id="13a7b-109">Прежде чем использовать табели, необходимо настроить общую информацию и указать администратора и одного или нескольких утверждающих табелей.</span><span class="sxs-lookup"><span data-stu-id="13a7b-109">Before you can use time sheets, you must set up general information and specify an administrator and one or more approvers of time sheets.</span></span> <span data-ttu-id="13a7b-110">Дополнительные сведения см. в разделе [Настройка табелей учета рабочего времени](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="13a7b-110">For more information, see [Set Up Time Sheets](projects-how-setup-time-sheets.md).</span></span>

## <a name="to-create-a-time-sheet"></a><span data-ttu-id="13a7b-111">Создание табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="13a7b-111">To create a time sheet</span></span>
<span data-ttu-id="13a7b-112">Можно использовать пакетное задание **Создать табели учета рабочего времени**, чтобы настроить табели для определенного количества периодов времени или недель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-112">You can use the **Create Time Sheets** batch job to set up time sheets for a specified number of time periods or weeks.</span></span> <span data-ttu-id="13a7b-113">Затем владелец табеля может открыть его и записать время, которое было затрачено на задание.</span><span class="sxs-lookup"><span data-stu-id="13a7b-113">Then, the time sheet owner can open it and record time that has been spent on a task.</span></span>

1. <span data-ttu-id="13a7b-114">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="13a7b-115">В окне **Список табелей** выберите действие **Создать табели учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-115">In the **Time Sheet List** window, choose the **Create Time Sheets** action.</span></span>
3. <span data-ttu-id="13a7b-116">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="13a7b-117">Поля **Использовать табель** и **Код пользователя владельца табеля** должны быть заполнены в карте для ресурса табеля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-117">The **Use Time Sheet** and **Time Sheet Owner User ID** fields must be filled in on the card for the resource of the time sheet.</span></span>

1. <span data-ttu-id="13a7b-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-118">Choose the **OK** button.</span></span>  

<span data-ttu-id="13a7b-119">Можно просматривать табели, созданные вами, в окне **Список табелей**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-119">You can view the time sheets that you have created in the **Time Sheet list** window.</span></span>

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a><span data-ttu-id="13a7b-120">Копирование строк планирования работ в табель учета времени</span><span class="sxs-lookup"><span data-stu-id="13a7b-120">To copy job planning lines to a time sheet</span></span>
<span data-ttu-id="13a7b-121">Далее описывается процедура создания быстрого добавления строк планирования работы в табель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-121">The following procedure describes how to quickly add job planning lines to a time sheet.</span></span>

1. <span data-ttu-id="13a7b-122">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-123">В окне **Список табелей** выберите табель для соответствующего периода времени, затем выберите действие **Изменить табель**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-123">In the **Time Sheet List** window, select a time sheet for the relevant time period, and then choose the **Edit Time Sheet** action.</span></span>  
3. <span data-ttu-id="13a7b-124">Выберите действие **Создать строки из планирования работ**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-124">Choose the **Create lines from job planning** action.</span></span> <span data-ttu-id="13a7b-125">Все строки планирования заданий в периоде времени табеля копируются в табель для лица или машины в поле **Номер ресурса** табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="13a7b-125">Any job planning lines in the time sheet time period are copied to the time sheet for the person or machine in the **Resource No.** field on the time sheet.</span></span>

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a><span data-ttu-id="13a7b-126">Определение видов работ и добавление вида работ в табель</span><span class="sxs-lookup"><span data-stu-id="13a7b-126">To define work types and add one to a time sheet</span></span>
<span data-ttu-id="13a7b-127">Можно определить тип работы для всех для строк табелей для заданий.</span><span class="sxs-lookup"><span data-stu-id="13a7b-127">You can define the work type for all time sheet lines for jobs.</span></span> <span data-ttu-id="13a7b-128">Таким образом можно добавить информацию, которая необходима, чтобы выставить счет клиенту за различные типы работ.</span><span class="sxs-lookup"><span data-stu-id="13a7b-128">In this way, you can add information that you need to bill the customer for different types of work.</span></span>

1. <span data-ttu-id="13a7b-129">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheets**, and then choose the related link.</span></span>   
2. <span data-ttu-id="13a7b-130">Откройте соответствующий табель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-130">Open the relevant time sheet.</span></span>
3. <span data-ttu-id="13a7b-131">Выберите поле **Описание**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-131">Choose the **Description** field.</span></span>  
4. <span data-ttu-id="13a7b-132">В окне **Сведения о работах строк табелей** окне выберите поле **Код вида работы** и выберите вид работы из списка, например **КМ**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-132">In the **Time Sheet Line Job Detail** window, choose the **Work Type Code** field, and select a work type from the list, such as **Miles**.</span></span>  
5. <span data-ttu-id="13a7b-133">В случае отсутствия видов работ, выберите действие **Создать**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-133">If no work types exist, chose the **New** action.</span></span>
6. <span data-ttu-id="13a7b-134">В окне **Виды работ** заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-134">In the **Work Types** window, fill in the fields as necessary.</span></span>
7. <span data-ttu-id="13a7b-135">Повторите шаг 4 для назначения нового вида работ табелю.</span><span class="sxs-lookup"><span data-stu-id="13a7b-135">Repeat step 4 to assign the new work type to the time sheet.</span></span>

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a><span data-ttu-id="13a7b-136">Повторное использование строк табелей в других табелях</span><span class="sxs-lookup"><span data-stu-id="13a7b-136">To reuse time sheet lines in other time sheets</span></span>
<span data-ttu-id="13a7b-137">Если ваши сведения о табеле учета рабочего времени остаются прежним от периода времени к периоду времени, можно сохранить время, копируя строки из предыдущего периода времени.</span><span class="sxs-lookup"><span data-stu-id="13a7b-137">If your time sheet information remains the same from time period to time period, you can save time by copying the lines from the previous time period.</span></span> <span data-ttu-id="13a7b-138">Затем необходимо просто ввести свое время работы для нового периода.</span><span class="sxs-lookup"><span data-stu-id="13a7b-138">Then, you just enter your time usage for the new period.</span></span>

1. <span data-ttu-id="13a7b-139">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-140">Откройте табель дата периода, более позднего, чем период для существующего табеля со строками.</span><span class="sxs-lookup"><span data-stu-id="13a7b-140">Open the time sheet for a period later than the period for an existing time sheet with lines.</span></span>  
3. <span data-ttu-id="13a7b-141">Выберите действие **Копировать строки из предыдущих табелей**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-141">Choose the **Copy Lines from Previous Time Sheet** action.</span></span>

<span data-ttu-id="13a7b-142">Строки копируются, включая подробную информацию, такую как тип и описание.</span><span class="sxs-lookup"><span data-stu-id="13a7b-142">The lines are copied, including details such as type and description.</span></span> <span data-ttu-id="13a7b-143">Например, если данная строка связана с работой, то поле **Код работы** копируется.</span><span class="sxs-lookup"><span data-stu-id="13a7b-143">For example, if the line is related to a job, the **Job No.** is copied.</span></span> <span data-ttu-id="13a7b-144">Все скопированные строки имеют статус **Открыто**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-144">All copied lines have the status **Open**.</span></span> <span data-ttu-id="13a7b-145">Теперь строки можно изменять, как требуется.</span><span class="sxs-lookup"><span data-stu-id="13a7b-145">You can now modify the lines as needed.</span></span>

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a><span data-ttu-id="13a7b-146">Заполнение строк табелей и отправка на утверждение</span><span class="sxs-lookup"><span data-stu-id="13a7b-146">To fill in a time sheet lines and submit for approval</span></span>
<span data-ttu-id="13a7b-147">Регистрация табеля отслеживается в часах (стандартной базовой единице измерения для ресурсов).</span><span class="sxs-lookup"><span data-stu-id="13a7b-147">Time sheet registration is tracked in hours, the standard base unit of measure for resources.</span></span> <span data-ttu-id="13a7b-148">По умолчанию в табеле отображаются общие рабочие дни с понедельника по пятницу.</span><span class="sxs-lookup"><span data-stu-id="13a7b-148">By default, a time sheet shows the common work days of Monday through Friday.</span></span>

1. <span data-ttu-id="13a7b-149">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-150">Выберите табель для соответствующего периода времени, затем выберите действие **Изменить табель**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-150">Select a time sheet for the relevant time period, and then choose the **Edit Time Sheet** action.</span></span>  
3. <span data-ttu-id="13a7b-151">Заполните поля в строке по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="13a7b-151">Fill in the fields on a line as necessary.</span></span> <span data-ttu-id="13a7b-152">Введите количество часов, использованных ресурсом, для каждого дня недели.</span><span class="sxs-lookup"><span data-stu-id="13a7b-152">Enter the number of hours used by the resource on each day of the week.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="13a7b-153">Можно просмотреть общее количество часов, которые вы ввели на информационной панели **Сводка по фактическим и бюджетным суммам**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-153">You can review the sum of time sheet hours that you have entered in the **Actual/Budgeted Summary** FactBox.</span></span>  
4. <span data-ttu-id="13a7b-154">Повторите шаг 3 для других видов работ, которые выполняет ресурс.</span><span class="sxs-lookup"><span data-stu-id="13a7b-154">Repeat step 3 for other work types that the resource performs.</span></span>
5. <span data-ttu-id="13a7b-155">Выберите действие **Передать**, затем выберите действие **Все открытые строки** для передачи всех строк или действие **Только выбранные строки** для передачи только строк, которые выбраны в окне **Табель учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-155">Choose the **Submit** action, and then choose the **All open lines** action to submit all lines or the **Selected lines only** action to submit only the lines that are selected in the **Time Sheet** window.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="13a7b-156">Вы можете отправлять только строки табеля, для которых введено время.</span><span class="sxs-lookup"><span data-stu-id="13a7b-156">You can only submit time sheet lines for which you have entered time.</span></span>  
6. <span data-ttu-id="13a7b-157">Чтобы изменить информацию в строке, для которой установлено значение **Представляется**, выделите строку и выберите действие **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-157">To modify information on a line that has been set to **Submitted**, select the line, and then choose the **Reopen** action.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="13a7b-158">Менеджер может отклонить строку табеля, которая представлена на утверждение.</span><span class="sxs-lookup"><span data-stu-id="13a7b-158">A manager may reject a time sheet line that is submitted for approval.</span></span> <span data-ttu-id="13a7b-159">Если строка имеет статус **Отклонено**, вы можете внести изменения в строку, а затем выбрать **Отправить** еще раз.</span><span class="sxs-lookup"><span data-stu-id="13a7b-159">If a line has a status of **Rejected**, you can make changes to the line, and then choose **Submit** again.</span></span>  
7. <span data-ttu-id="13a7b-160">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-160">Choose the **OK** button.</span></span>

## <a name="to-approve-or-reject-a-time-sheet"></a><span data-ttu-id="13a7b-161">Утверждение или отклонение табеля</span><span class="sxs-lookup"><span data-stu-id="13a7b-161">To approve or reject a time sheet</span></span>
<span data-ttu-id="13a7b-162">Табель должны быть отправлен для утверждения, прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="13a7b-162">A time sheet must be submitted for approval before it can be used.</span></span> <span data-ttu-id="13a7b-163">Можно принимать или отклонять отдельные строки в табеле либо отправлять обратно для выполнения дополнительного действия.</span><span class="sxs-lookup"><span data-stu-id="13a7b-163">You can approve and reject individual lines on a time sheet or send them back to the submitter for additional action.</span></span> <span data-ttu-id="13a7b-164">Табель может быть утвержден двумя способами:</span><span class="sxs-lookup"><span data-stu-id="13a7b-164">A time sheet can be approved in two ways:</span></span>

* <span data-ttu-id="13a7b-165">Администратор табелей может утвердить любой табель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-165">A time sheet administrator can approve any time sheet.</span></span>
* <span data-ttu-id="13a7b-166">Лицо, указанное в поле **Код пользователя, утверждающего табель** в карточке ресурса, может утвердить табели этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="13a7b-166">The person who is specified in the **Time Sheet Approver User ID** field on a resource card can approve that resource's time sheets.</span></span> <span data-ttu-id="13a7b-167">Дополнительные сведения см. в разделе [Настройка табелей учета рабочего времени](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="13a7b-167">For more information, see [Set Up Time Sheets](projects-how-setup-time-sheets.md).</span></span>

1. <span data-ttu-id="13a7b-168">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Управление табелями учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-168">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Manager Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="13a7b-169">Выберите табель в списке.</span><span class="sxs-lookup"><span data-stu-id="13a7b-169">Select a time sheet from the list.</span></span>  
3. <span data-ttu-id="13a7b-170">В окне **Табель учета рабочего времени** выберите действие **Утвердить**, затем выберите действие **Все отправленные строки** для утверждения всех строк или действие **Только выбранные строки** для утверждения только строк, которые выбраны в окне **Табель учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-170">In the **Time Sheet** window, choose the **Approve** action, and then choose the **All submitted lines** action to approve all lines or the **Selected lines only** action to approve only the lines that are selected in the **Time Sheet** window.</span></span>
4. <span data-ttu-id="13a7b-171">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-171">Choose the **OK** button.</span></span>  
5. <span data-ttu-id="13a7b-172">Можно также выбрать действие **Отклонить** и выполнить шаги с 4 по 5.</span><span class="sxs-lookup"><span data-stu-id="13a7b-172">Alternatively, choose the **Reject** action and follow steps 4 through 5.</span></span>  

> [!TIP]  
>   <span data-ttu-id="13a7b-173">Используйте информационные панели **Статус табеля** и **Сводка по фактическим и бюджетным суммам** для общего просмотра сведений о табеле учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="13a7b-173">Use the **Time Sheet Status** and **Actual/Budgeted Summary** FactBoxes to get an overview of time sheet information.</span></span>

<span data-ttu-id="13a7b-174">После утверждения или отклонение табеля его нельзя изменить, пока он не будет повторно открыт.</span><span class="sxs-lookup"><span data-stu-id="13a7b-174">After you have approved or rejected a time sheet, it cannot be modified unless it is first reopened.</span></span> <span data-ttu-id="13a7b-175">В следующей процедуре объясняется, как повторно открыть утвержденный или отклоненный табель.</span><span class="sxs-lookup"><span data-stu-id="13a7b-175">The following procedure explains how to reopen an approved or rejected time sheet.</span></span>

## <a name="to-reopen-a-time-sheet"></a><span data-ttu-id="13a7b-176">Повторное открытие табеля</span><span class="sxs-lookup"><span data-stu-id="13a7b-176">To reopen a time sheet</span></span>
1. <span data-ttu-id="13a7b-177">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), **введите Управление табелями учета рабочего времени** или **Табели учета рабочего времени**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-177">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Manager Time Sheets** or **Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="13a7b-178">Откройте табель из списка.</span><span class="sxs-lookup"><span data-stu-id="13a7b-178">Open a time sheet from the list.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="13a7b-179">Повторно можно открыть только строки с состоянием **Одобрено**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-179">You can only reopen lines that have the status **Approved**.</span></span> <span data-ttu-id="13a7b-180">Невозможно повторно открыть строки со статусом **Отклонено**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-180">You cannot reopen lines that have the status **Rejected**.</span></span> <span data-ttu-id="13a7b-181">Невозможно повторно открыть табель, если он был учтен.</span><span class="sxs-lookup"><span data-stu-id="13a7b-181">You cannot reopen a time sheet if it has been posted.</span></span>  
3. <span data-ttu-id="13a7b-182">В окне **Табель учета рабочего времени** выберите действие **Открыть**, затем выберите действие **Все отправленные строки** для повторного открытия всех строк или действие **Только выбранные строки** для повторного открытия только строк, которые выбраны в окне **Табель учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-182">In the **Time Sheet** window, choose the **Reopen** action, and then choose the **All submitted lines** action to reopen all lines or the **Selected lines only** action to reopen only the lines that are selected in the **Time Sheet** window.</span></span>
4. <span data-ttu-id="13a7b-183">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-183">Choose the **OK** button.</span></span> <span data-ttu-id="13a7b-184">Статус строки или строк табелей изменяется на **Представляется**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-184">The status of the time sheets line or lines is changes to **Submitted**.</span></span>  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a><span data-ttu-id="13a7b-185">Учет строк табеля в журнале ресурсов</span><span class="sxs-lookup"><span data-stu-id="13a7b-185">To post time sheet lines in a resource journal</span></span>
<span data-ttu-id="13a7b-186">После утверждения операций табеля для ресурса можно выполнять их учет в соответствующем журнале ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a7b-186">After you have approved time sheet entries for a resource, you can post them to the relevant resource journal.</span></span>

1. <span data-ttu-id="13a7b-187">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал ресурсов**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-187">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-188">Выберите действие **Предлагать строки из табелей**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-188">Choose the **Suggest Lines from Time Sheets** action.</span></span>  
3. <span data-ttu-id="13a7b-189">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-189">Fill in the fields as necessary.</span></span>  
4. <span data-ttu-id="13a7b-190">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-190">Choose the **OK** button.</span></span> <span data-ttu-id="13a7b-191">Операции для использования создаются в журнале ресурсов, в котором можно изменить информацию как нужно.</span><span class="sxs-lookup"><span data-stu-id="13a7b-191">Entries for usage are created in the resource journal, where you can modify the information as needed.</span></span>  
5. <span data-ttu-id="13a7b-192">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-192">Choose the **Post** action.</span></span>  
6. <span data-ttu-id="13a7b-193">Чтобы проверить учет, выберите действие **Книга операций**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-193">To verify the posting, choose the **Ledger Entries** action.</span></span> <span data-ttu-id="13a7b-194">Открывается окно **Книга операций по ресурсам** с результатом учета журнала ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a7b-194">The **Resource Ledger Entries** window opens showing the result of posting the resource journal.</span></span>

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a><span data-ttu-id="13a7b-195">Учет строк табеля в журнале работ</span><span class="sxs-lookup"><span data-stu-id="13a7b-195">To post time sheet lines in a job journal</span></span>
<span data-ttu-id="13a7b-196">После утверждения операций табеля для работы можно выполнять их учет в соответствующем журнале работ.</span><span class="sxs-lookup"><span data-stu-id="13a7b-196">After you have approved time sheet entries for a job, you can post them to the relevant job journal.</span></span>

1. <span data-ttu-id="13a7b-197">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Журнал работ**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-197">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-198">Выберите действие **Предлагать строки из табелей**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-198">Choose the **Suggest Lines from Time Sheets** action.</span></span>  
3. <span data-ttu-id="13a7b-199">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-199">Fill in the fields as necessary.</span></span>  
4. <span data-ttu-id="13a7b-200">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-200">Choose the **OK** button.</span></span> <span data-ttu-id="13a7b-201">Операции для использования создаются в журнале работ, в котором можно изменить информацию как нужно.</span><span class="sxs-lookup"><span data-stu-id="13a7b-201">Entries for usage are created in the job journal, where you can modify the information as needed.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="13a7b-202">Информация о типе работы и о том, оплачивается ли эта работа, копируется из строки табеля.</span><span class="sxs-lookup"><span data-stu-id="13a7b-202">Information about work type and whether the work is chargeable is copied from the time sheet line.</span></span> <span data-ttu-id="13a7b-203">Если необходимо, можно сократить количество и выполнить частичный учет.</span><span class="sxs-lookup"><span data-stu-id="13a7b-203">If needed, you can reduce the quantity of hours and do a partial posting.</span></span> <span data-ttu-id="13a7b-204">Если уменьшить количество, то в следующий раз при выборе действия **Предлагать строки из табелей** создаваемая строка будет содержать остаток часов.</span><span class="sxs-lookup"><span data-stu-id="13a7b-204">If you reduce the quantity, then the next time that you choose the **Suggest Lines From Time Sheets** action, the line that is created will contain the remaining quantity of hours.</span></span>  
5. <span data-ttu-id="13a7b-205">Выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-205">Choose the **Post** action.</span></span>  
6. <span data-ttu-id="13a7b-206">Чтобы проверить учет, выберите действие **Книга операций**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-206">To verify the posting, choose the **Ledger Entries** action.</span></span> <span data-ttu-id="13a7b-207">Открывается окно **Книга операций по работам** с результатом учета журнала ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a7b-207">The **Job Ledger Entries** window opens showing the result of posting the resource journal.</span></span>

## <a name="to-archive-time-sheets"></a><span data-ttu-id="13a7b-208">Архивирование табелей</span><span class="sxs-lookup"><span data-stu-id="13a7b-208">To archive time sheets</span></span>
<span data-ttu-id="13a7b-209">После учета табелей их можно поместить в архив для обращения в будущем.</span><span class="sxs-lookup"><span data-stu-id="13a7b-209">After you have posted time sheets, you can archive them for future reference.</span></span> <span data-ttu-id="13a7b-210">Все строки табелей необходимо учесть, прежде чем табель можно будет поместить в архив.</span><span class="sxs-lookup"><span data-stu-id="13a7b-210">All time sheets lines must be posted before a time sheet can be archived.</span></span>

> [!NOTE]  
>   <span data-ttu-id="13a7b-211">Примечание. Когда архивируется табель учета рабочего времени, он удаляется из списков в окнах **Табели учета рабочего времени** и **Управление табелями учета рабочего времени**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-211">When you archive a time sheet, it is removed from the lists in both the **Time Sheets** window and the **Manager Time Sheets** window.</span></span>

1. <span data-ttu-id="13a7b-212">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Переместить табели учета рабочего времени менеджеров в архив**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-212">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Move Time Sheets to Archive**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13a7b-213">Заполните поля, как требуется, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13a7b-213">Fill in the fields as necessary, and then choose the **OK** button.</span></span>  
3. <span data-ttu-id="13a7b-214">Для просмотра архивированных табелей выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Архивы табелей** или **Архивы табелей руководителя**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="13a7b-214">To review archived time sheets, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Time Sheet Archives** or **Manager Time Sheet Archives**, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="13a7b-215">См. также</span><span class="sxs-lookup"><span data-stu-id="13a7b-215">See Also</span></span>
[<span data-ttu-id="13a7b-216">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="13a7b-216">Project Management</span></span>](projects-manage-projects.md)  
<span data-ttu-id="13a7b-217">[Настройка управления проектами](projects-setup-projects.md)  </span><span class="sxs-lookup"><span data-stu-id="13a7b-217">[Setting Up Project Management](projects-setup-projects.md)  </span></span>  
[<span data-ttu-id="13a7b-218">Финансы</span><span class="sxs-lookup"><span data-stu-id="13a7b-218">Finance</span></span>](finance.md)  
<span data-ttu-id="13a7b-219">[Покупки](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="13a7b-219">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="13a7b-220">[Продажи](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="13a7b-220">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="13a7b-221">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13a7b-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
