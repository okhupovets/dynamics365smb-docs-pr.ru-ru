---
title: "Определение макета чека | Документы Майкрософт"
description: "Вы можете разрабатывать и печатать чеки в различных форматах, чтобы они соответствовали определенным стандартам."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d48b7954402b96c1bb5d3a2a63c70f48c6a4f9d7
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="8715f-103">Определение макетов платежных документов</span><span class="sxs-lookup"><span data-stu-id="8715f-103">Define Check Layouts</span></span>
<span data-ttu-id="8715f-104">Вы можете разработать платежные документы в соответствии со стандартами, установленными местными органами власти.</span><span class="sxs-lookup"><span data-stu-id="8715f-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="8715f-105">Изображения платежных документов можно печатать на английском, французском или испанском языке.</span><span class="sxs-lookup"><span data-stu-id="8715f-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="8715f-106">Платежные документы разрабатываются для печати в форматах изображений платежных документов США и Канады в формате "платежный документ-бланк-платежный документ" или "бланк-бланк-платежный документ".</span><span class="sxs-lookup"><span data-stu-id="8715f-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="8715f-107">Определение макетов платежных документов</span><span class="sxs-lookup"><span data-stu-id="8715f-107">To define check layouts</span></span>
1. <span data-ttu-id="8715f-108">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Выбор отчета - банковский счет**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8715f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="8715f-109">В окне **Выбор отчета - банковский счет** в поле **Использование** выберите **Платежный документ**.</span><span class="sxs-lookup"><span data-stu-id="8715f-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="8715f-110">Выберите один из следующих кодов отчетов.</span><span class="sxs-lookup"><span data-stu-id="8715f-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="8715f-111">Код отчета</span><span class="sxs-lookup"><span data-stu-id="8715f-111">Report ID</span></span> | <span data-ttu-id="8715f-112">Название отчета</span><span class="sxs-lookup"><span data-stu-id="8715f-112">Report Name</span></span> | <span data-ttu-id="8715f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8715f-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8715f-114">1401</span><span class="sxs-lookup"><span data-stu-id="8715f-114">1401</span></span> |<span data-ttu-id="8715f-115">Платежный документ</span><span class="sxs-lookup"><span data-stu-id="8715f-115">Check</span></span> |<span data-ttu-id="8715f-116">Это отчет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8715f-116">This is the default report.</span></span> |
| <span data-ttu-id="8715f-117">10401</span><span class="sxs-lookup"><span data-stu-id="8715f-117">10401</span></span> |<span data-ttu-id="8715f-118">Платежный документ (Бланк/Бланк/Платежный документ)</span><span class="sxs-lookup"><span data-stu-id="8715f-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="8715f-119">Этот отчет предназначен для печати платежных документов в формате "бланк/бланк/платежный документ".</span><span class="sxs-lookup"><span data-stu-id="8715f-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="8715f-120">10411</span><span class="sxs-lookup"><span data-stu-id="8715f-120">10411</span></span> |<span data-ttu-id="8715f-121">Платежный документ (Бланк/Платежный документ/Бланк)</span><span class="sxs-lookup"><span data-stu-id="8715f-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="8715f-122">Этот отчет предназначен для печати платежных документов в формате "платежный документ/бланк/платежный документ".</span><span class="sxs-lookup"><span data-stu-id="8715f-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="8715f-123">После настройки макетов платежных документов их можно распечатывать из окна **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="8715f-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="8715f-124">Дополнительные сведения см. в разделе [Работа с платежными документами](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="8715f-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8715f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8715f-125">See Also</span></span>
[<span data-ttu-id="8715f-126">Управление кредиторской задолженностью</span><span class="sxs-lookup"><span data-stu-id="8715f-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="8715f-127">[Управление банковскими счетами](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="8715f-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="8715f-128">Выполнение процессов завершения периода</span><span class="sxs-lookup"><span data-stu-id="8715f-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="8715f-129">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8715f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8715f-130">Общие бизнес-функции</span><span class="sxs-lookup"><span data-stu-id="8715f-130">General Business Functionality</span></span>](ui-across-business-areas.md)
