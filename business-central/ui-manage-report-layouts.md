---
title: "Пользовательские и встроенные макеты отчетов и документов | Документы Майкрософт"
description: "Макеты отчетов служат для персонализации документов, например для настройки шрифтов, логотипов и параметров страниц PDF-файлов, которые вы отправляете клиентам."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3a8f17e86241a49ec65233b42ac0fb647462a8ab
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="managing-report-and-document-layouts"></a><span data-ttu-id="33291-103">Управление макетами отчетов и документов</span><span class="sxs-lookup"><span data-stu-id="33291-103">Managing Report and Document Layouts</span></span>
<span data-ttu-id="33291-104">Макет отчета контролирует содержимое и формат отчета, включая то, какие поля данных набора данных отчета отображаются в нем и как они упорядочены, а также стиль текста, изображения и т. д.</span><span class="sxs-lookup"><span data-stu-id="33291-104">A report layout controls content and format of the report, including which data fields of a report dataset appear on the report and how they are arranged, text style, images, and more.</span></span> <span data-ttu-id="33291-105">В [!INCLUDE[d365fin](includes/d365fin_md.md)] можно изменить используемый в отчете макет, создать новый макет или изменить текущие макеты.</span><span class="sxs-lookup"><span data-stu-id="33291-105">From [!INCLUDE[d365fin](includes/d365fin_md.md)], you can change which layout is used on a report, create new layout, or modify the existing layouts.</span></span>

> [!NOTE]  
>   <span data-ttu-id="33291-106">В [!INCLUDE[d365fin](includes/d365fin_md.md)] термин "отчет" также означает внешние документы, такие как счета продажи и подтверждения заказов, которые вы отправляете клиентам в виде PDF-файлов.</span><span class="sxs-lookup"><span data-stu-id="33291-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the term "report" also covers externally-facing documents, such as sales invoices and order confirmations that you send to customers as PDF files.</span></span>

<span data-ttu-id="33291-107">В частности, макет отчета настраивает следующее.</span><span class="sxs-lookup"><span data-stu-id="33291-107">In particular, a report layout sets up the following:</span></span>

* <span data-ttu-id="33291-108">Поля меток и данных для включения из набора данных отчета [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="33291-108">The label and data fields to include from the dataset of the [!INCLUDE[d365fin](includes/d365fin_md.md)] report.</span></span>
* <span data-ttu-id="33291-109">Текстовый формат, например тип, размер и цвет шрифта.</span><span class="sxs-lookup"><span data-stu-id="33291-109">The text format, such as font type, size, and color.</span></span>
* <span data-ttu-id="33291-110">Логотип компании и его расположение.</span><span class="sxs-lookup"><span data-stu-id="33291-110">The company logo and its position.</span></span>
* <span data-ttu-id="33291-111">Общие параметры страницы, такие как поля и фоновые изображения.</span><span class="sxs-lookup"><span data-stu-id="33291-111">General page settings, such as margins and background images.</span></span>

<span data-ttu-id="33291-112">[!INCLUDE[d365fin](includes/d365fin_md.md)] можно настроить с несколькими макетами, между которыми можно при необходимости переключаться.</span><span class="sxs-lookup"><span data-stu-id="33291-112">A [!INCLUDE[d365fin](includes/d365fin_md.md)] can be set up with multiple report layouts, which you can switch among as required.</span></span> <span data-ttu-id="33291-113">Можно использовать один из встроенных макетов отчета или создать пользовательские макеты отчета и назначить их отчетам.</span><span class="sxs-lookup"><span data-stu-id="33291-113">You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed.</span></span> <span data-ttu-id="33291-114">Дополнительные сведения см. в разделе [Создание пользовательского макета отчета или документа](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="33291-114">For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).</span></span>

<span data-ttu-id="33291-115">Существует два типа макетов отчета, которые можно использовать в отчетах — Word и RDLC.</span><span class="sxs-lookup"><span data-stu-id="33291-115">There are two types of report layouts that you can use on reports; Word and RDLC.</span></span>

## <a name="word-report-layout-overview"></a><span data-ttu-id="33291-116">Обзор макета отчетов Word</span><span class="sxs-lookup"><span data-stu-id="33291-116">Word report layout overview</span></span>
<span data-ttu-id="33291-117">Макет отчета Word основан на документе Word (тип файла DOCX).</span><span class="sxs-lookup"><span data-stu-id="33291-117">A Word report layout is a based on Word document (.docx file type).</span></span> <span data-ttu-id="33291-118">Макеты отчетов Word позволяют разрабатывать макеты отчетов с помощью Microsoft Word 2013 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="33291-118">Word report layouts enable you to design report layouts by using Microsoft Word 2013 or later.</span></span> <span data-ttu-id="33291-119">Макет отчета Word определяет содержимое отчета, расположение элементов отчета и их внешний вид.</span><span class="sxs-lookup"><span data-stu-id="33291-119">A Word report layout determines the report's content - controlling how that content elements are arranged and how they look.</span></span> <span data-ttu-id="33291-120">Документ макета отчетов Word, как правило, использует таблицы для организации содержимого, клетки которых могут содержать поля данных, текст или изображения.</span><span class="sxs-lookup"><span data-stu-id="33291-120">A Word report layout document will typically use tables to arrange content, where the cells can contain data fields, text, or pictures.</span></span>

 <span data-ttu-id="33291-121">![Пример документа макета отчета Word для NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")</span><span class="sxs-lookup"><span data-stu-id="33291-121">![Example of a word report layout document for NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")</span></span>  

## <a name="rdlc-layout-overview"></a><span data-ttu-id="33291-122">Обзор макета RDLC</span><span class="sxs-lookup"><span data-stu-id="33291-122">RDLC layout overview</span></span>
<span data-ttu-id="33291-123">Макеты RDLC основаны на клиентских макетах определения отчета (типы файла RDLC или RDL).</span><span class="sxs-lookup"><span data-stu-id="33291-123">RDLC layouts are based on client report definition layouts (.rdlc or .rdl file types).</span></span> <span data-ttu-id="33291-124">Эти макеты создаются и изменяются с использованием конструктора отчетов SQL Server Report Builder.</span><span class="sxs-lookup"><span data-stu-id="33291-124">These layouts are created and modified by using SQL Server Report Builder.</span></span> <span data-ttu-id="33291-125">Дизайнерская концепция макетов RDLC схожа с макетами Word, где макет определяет общий формат отчета и включаемые в него поля из набора данных.</span><span class="sxs-lookup"><span data-stu-id="33291-125">The design concept for RDLC layouts is similar to Word layouts, where the layout defines the general format of the report and determines the fields from the dataset to include.</span></span> <span data-ttu-id="33291-126">Разработка макетов RDLC более сложная, чем макетов Word.</span><span class="sxs-lookup"><span data-stu-id="33291-126">Designing RDLC layouts is more advanced than Word layouts.</span></span> <span data-ttu-id="33291-127">Дополнительные сведения см. в разделе [Разработка макетов отчетов RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).</span><span class="sxs-lookup"><span data-stu-id="33291-127">For more information, see [Designing RDLC Report Layouts](/dynamics-nav/Designing-RDLC-Report-Layouts).</span></span>

## <a name="built-in-and-custom-report-layouts"></a><span data-ttu-id="33291-128">Встроенные и пользовательские макеты отчетов</span><span class="sxs-lookup"><span data-stu-id="33291-128">Built-in and custom report layouts</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="33291-129"> включает несколько встроенных макетов.</span><span class="sxs-lookup"><span data-stu-id="33291-129"> includes several built-in layouts.</span></span> <span data-ttu-id="33291-130">Встроенные макеты — это предопределенные макеты, предназначенные для определенных отчетов.</span><span class="sxs-lookup"><span data-stu-id="33291-130">Built-in layouts are predefined layouts that are designed for specific reports.</span></span> <span data-ttu-id="33291-131">Отчеты [!INCLUDE[d365fin](includes/d365fin_md.md)] будут иметь встроенный макет RDLC, макет отчета Word, а в некоторых случаях оба макета.</span><span class="sxs-lookup"><span data-stu-id="33291-131">[!INCLUDE[d365fin](includes/d365fin_md.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both.</span></span> <span data-ttu-id="33291-132">Невозможно изменить встроенные макеты отчетов в [!INCLUDE[d365fin](includes/d365fin_md.md)], но можно использовать их в качестве начальной точки для создания собственных пользовательских макетов отчетов.</span><span class="sxs-lookup"><span data-stu-id="33291-132">You cannot modify a built-in report layout from [!INCLUDE[d365fin](includes/d365fin_md.md)] but you use them as a starting point for building your own custom report layouts.</span></span>

<span data-ttu-id="33291-133">Пользовательские макеты — это макеты отчетов, созданные пользователем для изменения внешнего вида отчета.</span><span class="sxs-lookup"><span data-stu-id="33291-133">Custom layouts are report layouts that you design to change the appearance of a report.</span></span> <span data-ttu-id="33291-134">Обычно пользовательский макет создается на основании встроенного макета, но его можно создать с нуля или из копии существующего пользовательского макета.</span><span class="sxs-lookup"><span data-stu-id="33291-134">You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout.</span></span> <span data-ttu-id="33291-135">Пользовательские макеты позволяют настроить несколько макетов для одного и того же отчета. При необходимости можно переключаться между ними.</span><span class="sxs-lookup"><span data-stu-id="33291-135">Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed.</span></span> <span data-ttu-id="33291-136">Например, можно иметь разные макеты для каждой организации [!INCLUDE[d365fin](includes/d365fin_md.md)] или разные макеты для одной и той же организации, но разных случаев или событий, например специальной кампании или сезона отпусков.</span><span class="sxs-lookup"><span data-stu-id="33291-136">For example, you can have different layouts for each [!INCLUDE[d365fin](includes/d365fin_md.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.</span></span>

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a><span data-ttu-id="33291-137">Выбор между макетом отчета RDLC и Word</span><span class="sxs-lookup"><span data-stu-id="33291-137">Deciding whether to use a Word or RDLC report layout</span></span>
<span data-ttu-id="33291-138">В основе макета отчета может лежать документ Word или файл RDLC.</span><span class="sxs-lookup"><span data-stu-id="33291-138">A report layout can be based on either a Word document or RDLC file.</span></span> <span data-ttu-id="33291-139">Принятие решения об использовании макета отчета Word или RDLC зависит от того, как должен выглядеть готовый отчет, и ваших знаний о построителе отчетов SQL Server или Word.</span><span class="sxs-lookup"><span data-stu-id="33291-139">Deciding on whether to use a Word report layout or RDLC report layout type will depend on how you want the generated report to look and your knowledge of Word and SQL Server Report Builder.</span></span>

<span data-ttu-id="33291-140">Общие концепции дизайна макетов Word и RDLC очень схожи.</span><span class="sxs-lookup"><span data-stu-id="33291-140">The general design concepts for Word and RDLC layouts are very similar.</span></span> <span data-ttu-id="33291-141">Однако каждый тип имеет определенные особенности дизайна, влияющие на отображение созданного отчета в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="33291-141">However each type has certain design features that affect how the generated report is appears in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="33291-142">Это означат, что один и тот же отчет может выглядеть по-разному при использовании макетов отчетов Word и RDLC.</span><span class="sxs-lookup"><span data-stu-id="33291-142">This means that the same report might look different when using the Word report layout compared to the RDLC report layout.</span></span>

<span data-ttu-id="33291-143">Процедура настройки макетов отчетов Word и RDLC в отчетах одинакова.</span><span class="sxs-lookup"><span data-stu-id="33291-143">The process for setting up Word report layouts and RDLC report layouts on reports is the same.</span></span> <span data-ttu-id="33291-144">Основное различие — в способе изменения макетов.</span><span class="sxs-lookup"><span data-stu-id="33291-144">The main difference is in the way you modify the layouts.</span></span> <span data-ttu-id="33291-145">Макеты отчетов Word, как правило, проще создавать и изменять, чем макеты отчетов RDLC, поскольку можно использовать Word.</span><span class="sxs-lookup"><span data-stu-id="33291-145">Word report layouts are typically easier to create and modify than RDLC report layouts because you can use Word.</span></span> <span data-ttu-id="33291-146">Макеты отчетов RDLC изменяются с помощью построителя отчетов SQL Server, предназначенного для более продвинутых пользователей.</span><span class="sxs-lookup"><span data-stu-id="33291-146">RDLC report layouts are modified by using SQL Server Report builder which targets more advanced users.</span></span>

<span data-ttu-id="33291-147">Дополнительные сведения о том, как изменять используемый макет, см. в разделе [Изменение макета, в настоящее время используемого в отчете](ui-how-change-layout-currently-used-report.md).</span><span class="sxs-lookup"><span data-stu-id="33291-147">For information on how to change which layout to use, see [Change Which Layout is Currently Used on a Report](ui-how-change-layout-currently-used-report.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="33291-148">См. также</span><span class="sxs-lookup"><span data-stu-id="33291-148">See Also</span></span>
[<span data-ttu-id="33291-149">Обновление макетов отчетов или документов</span><span class="sxs-lookup"><span data-stu-id="33291-149">Updating Report or Document Layouts</span></span>](ui-update-report-layouts.md)  
<span data-ttu-id="33291-150">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33291-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="33291-151">Создание и изменение пользовательского макета отчета или документа</span><span class="sxs-lookup"><span data-stu-id="33291-151">Create and Modify a Custom Report or Document Layout</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="33291-152">Импорт и экспорт пользовательского макета отчета или документа</span><span class="sxs-lookup"><span data-stu-id="33291-152">Import and Export a Custom Report or Document Layout</span></span>](ui-how-import-and-export-report-layout.md)  
[<span data-ttu-id="33291-153">Отправка документов по электронной почте</span><span class="sxs-lookup"><span data-stu-id="33291-153">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="33291-154">Работа с отчетами</span><span class="sxs-lookup"><span data-stu-id="33291-154">Working with Reports</span></span>](ui-work-report.md)  
