---
title: "Выбор принтера для отчетов | Документы Майкрософт"
description: "Выбор принтеров для отчетов."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e0b13ff745cddf6173b7a6dacda05e915eff41ff
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="specify-printer-selection-for-reports"></a>Выбор принтера для отчета
Эта страница пустая, поскольку еще невозможно настроить определенные принтеры для конкретных отчетов. Мы работаем над разрешением этой проблемы.

Между тем, если вам требуется напечатать отчет, вам следует сначала загрузить отчет как PDF-документ, нажав кнопку **Отправить**. Затем выберите тип файла для загрузки отчета, в данном случае — **Документ PDF**. Теперь можно либо открыть PDF-документ сразу же и напечатать его, либо сохранить документ и напечатать его позже.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>См. также
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Практическое руководство. Запуск пакетных заданий](ui-how-run-batch-jobs.md)  
[Практическое руководство. Отправка документов по электронной почте](ui-how-send-documents-email.md)  
