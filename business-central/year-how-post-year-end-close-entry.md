---
title: "Проверка и учет операции закрытия года | Документы Майкрософт"
description: "Описывается порядок открытия журнала, указанного в пакетном задании \"Закрытие отчета о прибылях и убытках\", и проверки и учета операции закрытия года."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4263f6b3260dd5b8e8fad4f515dcdb61e12eb012
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="117a2-103">Учет операции закрытия года</span><span class="sxs-lookup"><span data-stu-id="117a2-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="117a2-104">После использования пакетного задания **Закрытие отчета о прибылях и убытках** для создания закрывающей операции (операций) на конец года необходимо открыть журнал, указанный для пакетного задания, и затем просмотреть и учесть записи.</span><span class="sxs-lookup"><span data-stu-id="117a2-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="117a2-105">Учет операции закрытия года</span><span class="sxs-lookup"><span data-stu-id="117a2-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="117a2-106">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Финансовый журнал**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="117a2-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="117a2-107">В окне **Финансовый журнал** в поле **Код раздела** выберите раздел, который содержит закрывающие операции.</span><span class="sxs-lookup"><span data-stu-id="117a2-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="117a2-108">Проверьте записи.</span><span class="sxs-lookup"><span data-stu-id="117a2-108">Review the entries.</span></span>
4. <span data-ttu-id="117a2-109">Чтобы учесть журнал, выберите действие **Учесть**.</span><span class="sxs-lookup"><span data-stu-id="117a2-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="117a2-110">При обнаружении ошибки отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="117a2-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="117a2-111">Если учет выполнен успешно, система удалит учтенные записи из журнала.</span><span class="sxs-lookup"><span data-stu-id="117a2-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="117a2-112">После завершения учета запись учитывается во всех счетах прибылей и убытков, при этом ее сальдо становится нулевым, и результат года переносится в балансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="117a2-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="117a2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="117a2-113">See Also</span></span>
[<span data-ttu-id="117a2-114">Закрытие учетных периодов</span><span class="sxs-lookup"><span data-stu-id="117a2-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="117a2-115">Закрытие книг</span><span class="sxs-lookup"><span data-stu-id="117a2-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="117a2-116">Закрытие отчета о прибылях и убытках</span><span class="sxs-lookup"><span data-stu-id="117a2-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="117a2-117">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="117a2-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
