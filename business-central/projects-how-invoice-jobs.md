---
title: "Создание счета продажи работы с целью выставления счета по работе | Документы Майкрософт"
description: "Описывается, как выставлять счета клиентам за расходы по работе по мере выполнения проекта."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b526879c1b49a90ff0ddcb415ba19f9d0567f7fd
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="invoice-jobs"></a><span data-ttu-id="116cf-103">Выставление счетов за работы</span><span class="sxs-lookup"><span data-stu-id="116cf-103">Invoice Jobs</span></span>
<span data-ttu-id="116cf-104">Во время проекта могут накапливаться затраты на выполнение работы из-за потребления ресурсов, материалов и связанных с работой покупок.</span><span class="sxs-lookup"><span data-stu-id="116cf-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="116cf-105">В ходе выполнения работы, эти транзакции учитываются в журнале работ.</span><span class="sxs-lookup"><span data-stu-id="116cf-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="116cf-106">Важно, чтобы перед выставлением счета клиенту в журнал работ были занесены все затраты.</span><span class="sxs-lookup"><span data-stu-id="116cf-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="116cf-107">Программа позволяет выставить счет за всю работу в окне **Рабочее задание - строки** или только по выбранным строками "К оплате" в окне **Строки планирования**.</span><span class="sxs-lookup"><span data-stu-id="116cf-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="116cf-108">Счета можно выставлять после завершения работы или через определенные промежутки времени в ходе выполнения работы согласно плану выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="116cf-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="116cf-109">Если выбрать значение **К оплате** в поле **Тип строки работы** в документах покупки для связанных с работой покупок, то создаются строки планирования работ, которые готовы для выставления счета клиенту.</span><span class="sxs-lookup"><span data-stu-id="116cf-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="116cf-110">Дополнительные сведения см. в разделе [Управление запасами для проекта](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="116cf-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="116cf-111">Создание и учет счета продажи для работы</span><span class="sxs-lookup"><span data-stu-id="116cf-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="116cf-112">Счет по работе или по одному или нескольким рабочим заданиям можно создавать, когда работа, по которой требуется выставить счет, завершена или при наступлении даты выставления счета согласно плану выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="116cf-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="116cf-113">Из окна **Работы** можно выставить клиенту счет, выбрав работу, затем выбрав действие **Создать счет продаж работ**.</span><span class="sxs-lookup"><span data-stu-id="116cf-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="116cf-114">Приведенная ниже процедура показывает, как использовать пакетное задание для выставления счетов за несколько работ.</span><span class="sxs-lookup"><span data-stu-id="116cf-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="116cf-115">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работа - создание счета продажи**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="116cf-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="116cf-116">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="116cf-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="116cf-117">Установите фильтры, если требуется ограничить работы, которые будет обрабатывать пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="116cf-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="116cf-118">Нажмите кнопку **ОК**, чтобы создать счета.</span><span class="sxs-lookup"><span data-stu-id="116cf-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="116cf-119">Создание нескольких счетов продажи по работам из строк планирования работы</span><span class="sxs-lookup"><span data-stu-id="116cf-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="116cf-120">Можно создать счет из строк планирования работы и указать количество товара, ресурс или счет ГК, по которому следует выставить счет.</span><span class="sxs-lookup"><span data-stu-id="116cf-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="116cf-121">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работы**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="116cf-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="116cf-122">Откройте соответствующую работу.</span><span class="sxs-lookup"><span data-stu-id="116cf-122">Open a relevant job.</span></span>
3. <span data-ttu-id="116cf-123">Выберите рабочее задание, для которого поле **Тип рабочего задания** содержит значение **Учет**, затем выберите действие **Строки планирования работ**.</span><span class="sxs-lookup"><span data-stu-id="116cf-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="116cf-124">В строке планирования работы в поле **Переносимое в счет количество** введите количество товара, ресурса, типа счета Главной книги, по которому следует выставить счет.</span><span class="sxs-lookup"><span data-stu-id="116cf-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="116cf-125">Выберите действие **Создать счет продажи**.</span><span class="sxs-lookup"><span data-stu-id="116cf-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="116cf-126">В окне **Работа - создание счета продажи** введите дату учета и укажите, требуется ли создать новый счет или добавить этот счет в уже существующему.</span><span class="sxs-lookup"><span data-stu-id="116cf-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="116cf-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="116cf-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="116cf-128">В строке планирования работы, в поле **Перенесенное в счет количество**, можно увидеть, количество.</span><span class="sxs-lookup"><span data-stu-id="116cf-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="116cf-129">В окне **Строки планирования работ** выберите действие **Счета продажи/кредит-ноты**.</span><span class="sxs-lookup"><span data-stu-id="116cf-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="116cf-130">Открывается окно **Счет продажи**, содержащее количество, которое было перемещено в счет.</span><span class="sxs-lookup"><span data-stu-id="116cf-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="116cf-131">Внесите все дополнительные изменения, затем выберите действие **Учет**.</span><span class="sxs-lookup"><span data-stu-id="116cf-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="116cf-132">Приведенная выше процедура аналогична процедуре для создания, рассмотрения и учета кредит-ноты продажи, связанной с работой.</span><span class="sxs-lookup"><span data-stu-id="116cf-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="116cf-133">Расчет и учет операций выполнения работ</span><span class="sxs-lookup"><span data-stu-id="116cf-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="116cf-134">После завершения всех действий по работе, включая учет потребления и выставление счетов, необходимо обновить работу, чтобы она получила **статус** **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="116cf-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="116cf-135">Затем необходимо обратить все НЗП, которые были учтены в главной книге.</span><span class="sxs-lookup"><span data-stu-id="116cf-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="116cf-136">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Работы**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="116cf-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="116cf-137">Выберите открытую работу, затем выберите действие **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="116cf-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="116cf-138">В поле **Статус** выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="116cf-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="116cf-139">Следуйте шагам помощи для вычисления и учета НЗП.</span><span class="sxs-lookup"><span data-stu-id="116cf-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="116cf-140">Можно также выполнить шаги 5 и 6, чтобы сделать это вручную.</span><span class="sxs-lookup"><span data-stu-id="116cf-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="116cf-141">Выберите действие **Рассчитать НЗП**.</span><span class="sxs-lookup"><span data-stu-id="116cf-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="116cf-142">В окне **Расчет НЗП по работам** заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="116cf-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="116cf-143">У операций НЗП по работам, созданных пакетным заданием, появится флажок в поле **Работа выполнена**, указывающий, что они являются операциями выполнения.</span><span class="sxs-lookup"><span data-stu-id="116cf-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="116cf-144">Выберите действие **Работа - учет НЗП в ГК**.</span><span class="sxs-lookup"><span data-stu-id="116cf-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="116cf-145">В окне **Работа - учет НЗП в ГК** заполните требуемые поля.</span><span class="sxs-lookup"><span data-stu-id="116cf-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="116cf-146">У операций НЗП по работам в главной книге, созданных пакетным заданием, появится флажок в поле **Работа выполнена**, указывающий, что они являются операциями выполнения.</span><span class="sxs-lookup"><span data-stu-id="116cf-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="116cf-147">См. также</span><span class="sxs-lookup"><span data-stu-id="116cf-147">See Also</span></span>
[<span data-ttu-id="116cf-148">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="116cf-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="116cf-149">Финансы</span><span class="sxs-lookup"><span data-stu-id="116cf-149">Finance</span></span>](finance.md)  
<span data-ttu-id="116cf-150">[Покупки](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="116cf-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="116cf-151">[Продажи](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="116cf-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="116cf-152">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="116cf-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
