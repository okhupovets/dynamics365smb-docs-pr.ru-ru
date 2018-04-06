---
title: "Практическое руководство. Добавление полей в макет отчета Word | Документы Майкрософт"
description: "Описывается процедура добавления полей набора данных отчета в существующий макет отчета Word для отчета."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 30d515822fd3e1ca3bf5b83e2bbc4e0841bea9cc
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="add-fields-to-a-word-report-layout"></a><span data-ttu-id="48971-103">Добавление полей в макет отчета Word</span><span class="sxs-lookup"><span data-stu-id="48971-103">Add Fields to a Word Report Layout</span></span>
<span data-ttu-id="48971-104">Набор данных отчета может состоять из полей, отображающих метки, данные и изображения.</span><span class="sxs-lookup"><span data-stu-id="48971-104">A report dataset can consist of fields that display labels, data, and images.</span></span> <span data-ttu-id="48971-105">В этом разделе описывается процедура добавления полей набора данных отчета в существующий макет отчета Word для отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-105">This topic describes the procedure for adding fields of a report dataset to an existing Word report layout for a report.</span></span> <span data-ttu-id="48971-106">Поля добавляются с использованием пользовательской части XML в Word для отчета и путем добавления элементов управления содержимым, сопоставляемых полям в наборе данных отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-106">You add fields by using the Word custom XML part for the report and adding content controls that map to the fields of the report dataset.</span></span> <span data-ttu-id="48971-107">Добавление полей требует определенных знаний набора данных отчета, чтобы можно было идентифицировать поля, которые требуется добавить в макет.</span><span class="sxs-lookup"><span data-stu-id="48971-107">Adding fields requires that you have some knowledge of the report's dataset so that you can identify the fields that you want to add to the layout.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="48971-108">Невозможно изменить встроенные макеты отчетов<!--Onprem. Built-in layouts can only be modified by using the development environment-->.</span><span class="sxs-lookup"><span data-stu-id="48971-108">You cannot modify built-in report layouts<!--Onprem. Built-in layouts can only be modified by using the development environment-->.</span></span>  

##  <a name="OpenXMLPart"></a> <span data-ttu-id="48971-109">Открытие пользовательской части XML для отчета в Word</span><span class="sxs-lookup"><span data-stu-id="48971-109">To open the Custom XML part for the Report in Word</span></span>  
  
1.  <span data-ttu-id="48971-110">Если это еще не сделано, откройте макет отчета Word в Word.</span><span class="sxs-lookup"><span data-stu-id="48971-110">If not already open, then open the Word report layout document in Word.</span></span>  
  
     <span data-ttu-id="48971-111">Дополнительные сведения см. в разделе [Создание и изменение пользовательского макета отчета](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="48971-111">For more information, see [Create and Modify a Custom Report Layout](ui-how-create-custom-report-layout.md).</span></span>  
  
2.  <span data-ttu-id="48971-112">Отобразите вкладку **Разработчик** на ленте Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="48971-112">Show the **Developer** tab in the ribbon of Microsoft Word.</span></span>  
  
     <span data-ttu-id="48971-113">По умолчанию вкладка **Разработчик** не отображается на ленте.</span><span class="sxs-lookup"><span data-stu-id="48971-113">By default, the **Developer** tab is not shown in the ribbon.</span></span> <span data-ttu-id="48971-114">Дополнительные сведения см. в разделе [Отображение вкладки разработчика на ленте](http://go.microsoft.com/fwlink/?LinkID=389631).</span><span class="sxs-lookup"><span data-stu-id="48971-114">For more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631).</span></span>  
  
3.  <span data-ttu-id="48971-115">На вкладке **Разработчик** выберите **Область сопоставления XML**.</span><span class="sxs-lookup"><span data-stu-id="48971-115">On the **Developer** tab, choose **XML Mapping Pane**.</span></span>  
  
4.  <span data-ttu-id="48971-116">В области **Сопоставление XML** в раскрывающемся списке **Пользовательская XML-часть** выберите пользовательскую XML-часть для отчета ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->, который обычно последний в списке.</span><span class="sxs-lookup"><span data-stu-id="48971-116">In the **XML Mapping** pane, in the **Custom XML Part** dropdown list, choose the custom XML part for ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> report, which is typically last in the list.</span></span> <span data-ttu-id="48971-117">Имя пользовательской XML-части имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="48971-117">The name of the custom XML part has the following format:</span></span>  
  
     <span data-ttu-id="48971-118">urn:microsoft-dynamics-nav/reports/*имя_отчета*/*ИД*</span><span class="sxs-lookup"><span data-stu-id="48971-118">urn:microsoft-dynamics-nav/reports/*report_name*/*ID*</span></span>  
  
     <span data-ttu-id="48971-119">*имя_отчета* — это имя, назначенное отчету<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="48971-119">*report_name* is the name that is assigned to the report<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.</span></span>  
  
     <span data-ttu-id="48971-120">*ИД* — это идентификационный номер отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-120">*ID* is the identification number of the report.</span></span>  
  
     <span data-ttu-id="48971-121">После выбора пользовательской XML-части в области сопоставления XML отображаются метки и элементы управления полем, доступные для отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-121">After you select the custom XML part, the XML Mapping pane displays the labels and field controls that are available for the report.</span></span>  
  
### <a name="to-add-a-label-or-data-field"></a><span data-ttu-id="48971-122">Добавление поля метки или данных</span><span class="sxs-lookup"><span data-stu-id="48971-122">To add a label or data field</span></span>  
  
1.  <span data-ttu-id="48971-123">Поместите курсор в документ, где требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="48971-123">Place your cursor in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="48971-124">В области **Сопоставления XML** щелкните правой кнопкой мыши элемент управления, который требуется добавить, щелкните **Вставить элемент управления содержимым** и щелкните **Обычный текст**.</span><span class="sxs-lookup"><span data-stu-id="48971-124">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    > [!NOTE]  
    >  <span data-ttu-id="48971-125">Невозможно добавить поле, вручную введя название поля набора данных в элементе управления содержимым.</span><span class="sxs-lookup"><span data-stu-id="48971-125">You cannot add a field by manually typing the dataset field name in the content control.</span></span> <span data-ttu-id="48971-126">Необходимо использовать область **Сопоставление XML** для сопоставления полей.</span><span class="sxs-lookup"><span data-stu-id="48971-126">You must use the **XML Mapping** pane to map the fields.</span></span>  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a><span data-ttu-id="48971-127">Добавление повторяющихся строк полей данных для создания списка</span><span class="sxs-lookup"><span data-stu-id="48971-127">To add repeating rows of data fields to create a list</span></span>  
  
1.  <span data-ttu-id="48971-128">В таблице добавьте строку таблицы со столбцом для каждого поля, которое должно повторяться.</span><span class="sxs-lookup"><span data-stu-id="48971-128">In a table, add a table row that includes a column for each field that you want repeated.</span></span>  
  
     <span data-ttu-id="48971-129">Эта строка будет функционировать как местозаполнитель для повторяющихся полей.</span><span class="sxs-lookup"><span data-stu-id="48971-129">This row will act as a placeholder for the repeating fields.</span></span>  
  
2.  <span data-ttu-id="48971-130">Выберите всю строку.</span><span class="sxs-lookup"><span data-stu-id="48971-130">Select the entire row.</span></span>  
  
3.  <span data-ttu-id="48971-131">В области **Сопоставления XML** щелкните правой кнопкой мыши элемент управления, соответствующий элементу данных отчета, который содержит повторяемые поля, щелкните **Вставить элемент управления содержимым** и выберите **Повторяющийся**.</span><span class="sxs-lookup"><span data-stu-id="48971-131">In the **XML Mapping** pane, right-click the control that corresponds to the report data item that contains the fields that you want repeated, choose **Insert Content Control**, and then choose **Repeating**.</span></span>  
  
4.  <span data-ttu-id="48971-132">Добавьте повторяющиеся поля на строку следующим образом.</span><span class="sxs-lookup"><span data-stu-id="48971-132">Add the repeating fields to the row as follows:</span></span>  
  
    1.  <span data-ttu-id="48971-133">Поместите указатель в столбец.</span><span class="sxs-lookup"><span data-stu-id="48971-133">Place your pointer in a column.</span></span>  
  
    2.  <span data-ttu-id="48971-134">В области **Сопоставления XML** щелкните правой кнопкой мыши элемент управления, который требуется добавить, щелкните **Вставить элемент управления содержимым** и щелкните **Обычный текст**.</span><span class="sxs-lookup"><span data-stu-id="48971-134">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    3.  <span data-ttu-id="48971-135">Для каждого поля повторите шаги а и б.</span><span class="sxs-lookup"><span data-stu-id="48971-135">For each field, repeat steps a and b.</span></span>  
  
## <a name="adding-image-fields"></a><span data-ttu-id="48971-136">Добавление полей изображений</span><span class="sxs-lookup"><span data-stu-id="48971-136">Adding Image Fields</span></span>  
 <span data-ttu-id="48971-137">Набор данных отчета может включать поле, содержащее изображение, например логотип компании или изображение товара.</span><span class="sxs-lookup"><span data-stu-id="48971-137">A report dataset can include a field that contains an image, such as a company logo or a picture of an item.</span></span> <span data-ttu-id="48971-138">Чтобы добавить изображение из набора данных отчета, вставьте элемент управления содержимым **Изображение**.</span><span class="sxs-lookup"><span data-stu-id="48971-138">To add an image from the report dataset, you insert a **Picture** content control.</span></span>  
  
 <span data-ttu-id="48971-139">Изображения выравниваются в верхнем левом углу элемента управления содержимым и автоматически меняют свой размер пропорционально границе элемента управления содержимым.</span><span class="sxs-lookup"><span data-stu-id="48971-139">Images align in the top-left corner of the content control and resize automatically in proportion to fit the boundary of the content control.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="48971-140">Можно добавить изображения только в формате, поддерживаемом Word, например BMP, JPEG и PNG.</span><span class="sxs-lookup"><span data-stu-id="48971-140">You can only add images that have a format that is supported by Word, such as .bmp, .jpeg, and .png file types.</span></span> <span data-ttu-id="48971-141">При добавлении изображения в формате, не поддерживаемом Word, получается ошибка при выполнении отчета из клиента ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="48971-141">If you add an image that has a format that is not supported by Word, you will get an error when you run the report from the ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> client.</span></span>  
  
#### <a name="to-add-an-image"></a><span data-ttu-id="48971-142">Добавление изображения</span><span class="sxs-lookup"><span data-stu-id="48971-142">To add an image</span></span>  
  
1.  <span data-ttu-id="48971-143">Поместите указатель в документ, где требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="48971-143">Place your pointer in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="48971-144">В области **Сопоставления XML** щелкните правой кнопкой мыши элемент управления, который требуется добавить, щелкните **Вставить элемент управления содержимым** и щелкните **Изображение**.</span><span class="sxs-lookup"><span data-stu-id="48971-144">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Picture**.</span></span>  
  
3.  <span data-ttu-id="48971-145">Чтобы увеличить или уменьшить размер изображения, перетащите маркер размера по направлению к центру элемента управления содержимым или от него.</span><span class="sxs-lookup"><span data-stu-id="48971-145">To increase or decrease the image size, drag a sizing handle away from or towards the center of the content control.</span></span>  

## <a name="custom-xml-part-overview"></a><span data-ttu-id="48971-146">Обзор пользовательской XML-части</span><span class="sxs-lookup"><span data-stu-id="48971-146">Custom XML Part Overview</span></span>
<span data-ttu-id="48971-147">Макеты отчетов Word создаются на базе *пользовательских XML-частей*.</span><span class="sxs-lookup"><span data-stu-id="48971-147">Word report layouts are built on *custom XML parts*.</span></span> <span data-ttu-id="48971-148">Пользовательская XML-часть для отчета состоит из элементов, соответствующих элементам данных, столбцам и меткам, составляющим набор данных отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-148">A custom XML part for a report consists of elements that correspond to the data items, columns, and labels that comprise the report's dataset.</span></span> <span data-ttu-id="48971-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Пользовательская XML-часть используется для сопоставления данных в отчете при выполнении отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->The custom XML part is used to map the data into a report when the report is run.</span></span>

  
### <a name="xml-structure-of-custom-xml-part"></a><span data-ttu-id="48971-150">Структура XML и пользовательская часть XML</span><span class="sxs-lookup"><span data-stu-id="48971-150">XML Structure of Custom XML Part</span></span>  
<span data-ttu-id="48971-151">В следующей таблице приведен упрощенный обзор XML пользовательской XML-части.</span><span class="sxs-lookup"><span data-stu-id="48971-151">The following table provides a simplified overview of the XML of a custom XML part.</span></span>  
  
|<span data-ttu-id="48971-152">XML-элементы</span><span class="sxs-lookup"><span data-stu-id="48971-152">XML Elements</span></span>|<span data-ttu-id="48971-153">Описанием</span><span class="sxs-lookup"><span data-stu-id="48971-153">Description</span></span>|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|<span data-ttu-id="48971-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="48971-154">Header</span></span>|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|<span data-ttu-id="48971-155">Спецификация пространства имен XML.</span><span class="sxs-lookup"><span data-stu-id="48971-155">XML namespace specification.</span></span> <span data-ttu-id="48971-156">`<reportname>` — это имя, назначенное отчету.</span><span class="sxs-lookup"><span data-stu-id="48971-156">`<reportname>` is the name that is assigned to the report.</span></span> <span data-ttu-id="48971-157">`<id>` — это ИД, назначенный отчету.</span><span class="sxs-lookup"><span data-stu-id="48971-157">`<id>` is the ID that is assigned to the report.</span></span>|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|<span data-ttu-id="48971-158">Содержит все метки отчета.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span><span class="sxs-lookup"><span data-stu-id="48971-158">Contains all the labels for the report.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span></span><br /><span data-ttu-id="48971-159">-   Элементы меток, связанные со столбцами, имеют формат `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="48971-159">-   Label elements that are related to columns have the format `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span></span><br /><span data-ttu-id="48971-160">-  Элементы меток имеют формат `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="48971-160">-  Label elements have the format `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span></span><br /><span data-ttu-id="48971-161">-   Метки перечислены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="48971-161">-   Labels are listed in alphabetical order.</span></span>|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|<span data-ttu-id="48971-162">Элементы данных и столбцы верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="48971-162">Top-level data item and columns.</span></span> <span data-ttu-id="48971-163">Столбцы перечислены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="48971-163">Columns are listed in alphabetical order.</span></span><!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|<span data-ttu-id="48971-164">Элементы данных и столбцы, вложенные в элемент данных верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="48971-164">Data items and columns that are nested in the top-level data item.</span></span> <span data-ttu-id="48971-165">Столбцы перечислены в алфавитном порядке под соответствующим элементом данных.</span><span class="sxs-lookup"><span data-stu-id="48971-165">Columns are listed in alphabetical order under the respective data item.</span></span>|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|<span data-ttu-id="48971-166">Заключительный элемент.</span><span class="sxs-lookup"><span data-stu-id="48971-166">Closing element.</span></span>|  
  
### <a name="custom-xml-part-in-word"></a><span data-ttu-id="48971-167">Пользовательская часть XML в Word</span><span class="sxs-lookup"><span data-stu-id="48971-167">Custom XML Part in Word</span></span>  
 <span data-ttu-id="48971-168">В Word следует открыть пользовательскую XML-часть в области **Сопоставление XML**, а затем воспользоваться этой областью для сопоставления этих элементов элементам управления содержимым в документе Word.</span><span class="sxs-lookup"><span data-stu-id="48971-168">In Word, you open the custom XML part in the **XML Mapping** pane, and then use the pane to map elements to content controls in the Word document.</span></span> <span data-ttu-id="48971-169">Область **Сопоставление XML** можно открыть на вкладке **Разработчик** (для получения дополнительных сведений см. в разделе [Отображение вкладки разработчика на ленте](http://go.microsoft.com/fwlink/?LinkID=389631)).</span><span class="sxs-lookup"><span data-stu-id="48971-169">The **XML Mapping** pane is accessible from the **Developer** tab (for more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631)).</span></span>  
  
 <span data-ttu-id="48971-170">Элементы в области **Сопоставление XML** отображается в структуре, схожей с XML-источником.</span><span class="sxs-lookup"><span data-stu-id="48971-170">The elements in the **XML Mapping** pane appear in a structure that is similar to the XML source.</span></span> <span data-ttu-id="48971-171">Поля меток группируются под общим элементом **Метки**, а элементы данных и столбцы упорядочены в иерархическую структуру, соответствующую источнику XML, где столбцы отображаются в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="48971-171">Label fields are grouped under a common **Labels** element and data item and columns are arranged in a hierarchal structure that corresponds to the XML source, with columns listed in alphabetical order.</span></span> <span data-ttu-id="48971-172">Элементы идентифицируются по имени, как определено свойством "Имя" в конструкторе наборов данных отчетов в ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="48971-172">Elements are identified by their name as defined by the Name property in Report Dataset Designer in ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span></span>  
  
 <span data-ttu-id="48971-173">На приведенном ниже рисунке изображена простая пользовательская XML-часть из предыдущего раздела в области **Сопоставление XML** документа Word.</span><span class="sxs-lookup"><span data-stu-id="48971-173">The following figure illustrates the simple custom XML part from the previous section in the **XML Mapping** pane of a Word document.</span></span>  
  
 <span data-ttu-id="48971-174">![Часть области сопоставления XML в Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")</span><span class="sxs-lookup"><span data-stu-id="48971-174">![Clip of the XML Mapping pane in word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")</span></span>  
  
-   <span data-ttu-id="48971-175">Для добавления метки или поля в макет вставьте элемент управления содержимым, соответствующий элементу в области **Сопоставление XML**.</span><span class="sxs-lookup"><span data-stu-id="48971-175">To add a label or field to the layout, you insert a content control that maps to the element in the **XML Mapping** pane.</span></span>  
  
-   <span data-ttu-id="48971-176">Для создания повторяющихся строк столбцов вставьте элемент управления содержимым **Повторяющийся** для родительского элемента данных и добавьте элемент управления содержимым для столбцов.</span><span class="sxs-lookup"><span data-stu-id="48971-176">To create repeating rows of columns, insert a **Repeating** content control for the parent data item element, and then add content control for the columns.</span></span>  
  
-   <span data-ttu-id="48971-177">Для меток фактический текст, отображаемый в созданном отчете, — это значение свойства **Заголовок** для поля в таблице элементов данных (если метка связана со столбцом в наборе данных отчета) или для метки в конструкторе меток отчетов (если метка не связана со столбцом в наборе данных).</span><span class="sxs-lookup"><span data-stu-id="48971-177">For labels, the actual text that appears in the generated report is the value of the **Caption** property for the field in the data item table (if the label is related to the column in the report dataset) or a label in the Report Label Designer (if the label is not related to a column in the dataset).</span></span>  
  
-   <span data-ttu-id="48971-178">Язык метки, отображаемый при выполнении отчета, зависит от настройки языка объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="48971-178">The language of the label that is displayed when you run the report depends on the language setting of the report object.</span></span> <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a><span data-ttu-id="48971-179">См. также</span><span class="sxs-lookup"><span data-stu-id="48971-179">See Also</span></span>  
 [<span data-ttu-id="48971-180">Создание и изменение пользовательского макета отчета</span><span class="sxs-lookup"><span data-stu-id="48971-180">Create and Modify a Custom Report Layout</span></span>](ui-how-create-custom-report-layout.md)   