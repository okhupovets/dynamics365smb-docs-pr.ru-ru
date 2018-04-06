---
title: "Практическое руководство. Ограничение и разрешение использования записи | Microsoft Docs"
description: "Если нужно ограничить использование записи в определенных видах деятельности, например, до утверждения записи, можно встроить в рабочий процесс два отклика, управляющих использованием записи."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e95d6106fd4908bf13004da11656b9b6d1446ad3
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="1b9b9-103">Ограничение и разрешение использования записи</span><span class="sxs-lookup"><span data-stu-id="1b9b9-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="1b9b9-104">Если нужно ограничить использование записи в определенных видах деятельности, например, до утверждения записи, можно встроить в рабочий процесс два отклика, управляющих использованием записи.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="1b9b9-105">Один отклик процесса будет ограничивать использование записи, определенное событием и условиями рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="1b9b9-106">Другой отклик рабочего процесса будет разрешать использование записи, определенное событием и условиями рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="1b9b9-107">Для этой цели в универсальной версии [!INCLUDE[d365fin](includes/d365fin_md.md)] доступно два отклика: **Ограничить использование записи**</span><span class="sxs-lookup"><span data-stu-id="1b9b9-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="1b9b9-108">и **Разрешить использование записи**.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1b9b9-109">Универсальная версия [!INCLUDE[d365fin](includes/d365fin_md.md)] предлагает поддержку для ограничения учета записи, экспорта в качестве платежа, а также печати в чеке.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="1b9b9-110">Для поддержки других ограничений партнер Майкрософт должен настроить код приложения.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1b9b9-111">Возможности рабочих процессов для ограничения и разрешения использования записей не связаны с функциональностью блокировки учета записей товара, клиента и поставщика.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="1b9b9-112">Далее описывается процедура ограничения учета заказов на покупку до их утверждения.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="1b9b9-113">Новый рабочий процесс будет основан на существующем шаблоне рабочего процесса "Рабочий процесс утверждения счета покупки".</span><span class="sxs-lookup"><span data-stu-id="1b9b9-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="1b9b9-114">Создание шага рабочего процесса, ограничивающего учет неутвержденных заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="1b9b9-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="1b9b9-115">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Рабочие процессы**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1b9b9-116">В окне **Рабочие процессы** создайте новый рабочий процесс с именем "Рабочий процесс утверждения заказов на покупку".</span><span class="sxs-lookup"><span data-stu-id="1b9b9-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="1b9b9-117">Дополнительные сведения см. в разделе [Создание рабочих процессов](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="1b9b9-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="1b9b9-118">Выберите действие **Копировать из шаблона рабочего процесса**.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="1b9b9-119">Выберите поле **Исходный код рабочего процесса**, а затем в окне **Шаблоны рабочих процессов** выберите шаблон "Рабочий процесс утверждения счета покупки".</span><span class="sxs-lookup"><span data-stu-id="1b9b9-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="1b9b9-120">Обратите внимание, что первые 2 шага рабочего процесса связаны с ограничением и последующим разрешением использования счетов покупки.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="1b9b9-121">Теперь измените условие события в первом шаге нового рабочего процесса, чтобы указать, что он применяется к заказам на покупку.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="1b9b9-122">На экспресс-вкладке **Шаги рабочего процесса** выберите поле **Условия события**, а затем для фильтра **Тип документа** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="1b9b9-123">Измените, удалите или добавьте другие шаги рабочего процесса в соответствии с бизнес-процессом, который начинается с ограничения учета неутвержденных заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="1b9b9-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b9b9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1b9b9-124">See Also</span></span>  
<span data-ttu-id="1b9b9-125">[Создание рабочих процессов](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1b9b9-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="1b9b9-126">Рабочий процесс</span><span class="sxs-lookup"><span data-stu-id="1b9b9-126">Workflow</span></span>](across-workflow.md)   
