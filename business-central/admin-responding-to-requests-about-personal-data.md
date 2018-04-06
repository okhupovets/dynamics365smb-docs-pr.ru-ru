---
title: "Ответ на запросы о личных данных"
description: "Необходимо отвечать на запросы субъектов данных."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a><span data-ttu-id="afe22-103">Ответ на запросы о личных данных</span><span class="sxs-lookup"><span data-stu-id="afe22-103">Responding to Requests About Personal Data</span></span>  
<span data-ttu-id="afe22-104">Субъекты данных могут запрашивать различные типы действий в отношении своих личных данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-104">Data subjects can request several types of actions regarding their personal data.</span></span> <span data-ttu-id="afe22-105">Если вы классифицировали конфиденциальность своих данных и уверены, что они правильны, администратор может отвечать на запросы с помощью листа классификации данных в ролевом центре **Управление пользователями, группами пользователей и разрешениями** или, если вы используете клиент Windows, в ролевом центре, **Руководитель ИТ-отдела**.</span><span class="sxs-lookup"><span data-stu-id="afe22-105">If you have classified the sensitivity of your data, and are sure they are correct, an administrator can respond to requests by using the Data Classification worksheet on the **Manage Users, User Groups, and Permissions** Role Center or, if you are using the Windows client, in the **IT Manager** Role Center.</span></span> <span data-ttu-id="afe22-106">Дополнительную информацию о классификации данных и классификации конфиденциальности данных см. в разделах [Классификация данных](/dynamics-nav/classifying-data) и [Классификация чувствительности данных](admin-classifying-data-sensitivity.md).</span><span class="sxs-lookup"><span data-stu-id="afe22-106">For more information about classifying data and classifying data sensitivity, see [Classifying Data](/dynamics-nav/classifying-data) and [Classifying Data Sensitivity](admin-classifying-data-sensitivity.md).</span></span>

<span data-ttu-id="afe22-107">В следующей таблице приведены примеры типов запросов, на которые можно отвечать.</span><span class="sxs-lookup"><span data-stu-id="afe22-107">The following table provides examples of the types of requests you can respond to.</span></span>

> [!Note]
> <span data-ttu-id="afe22-108">Хотя мы обеспечиваем возможность отвечать на запросы этих типов и, таким образом, получать доступ к личным данным, ответственность за правильное размещение и классификацию личных и конфиденциальных данных лежит на вас.</span><span class="sxs-lookup"><span data-stu-id="afe22-108">While we provide capabilities for responding to these types of request, and thereby accessing, personal data, it is your responsibility to ensure that personal and sensitive data are located and classified appropriately.</span></span>

|<span data-ttu-id="afe22-109">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="afe22-109">Request Type</span></span>|<span data-ttu-id="afe22-110">Описание и предлагаемый отклик</span><span class="sxs-lookup"><span data-stu-id="afe22-110">Description and Suggested Response</span></span>|
|-----|-----|
|<span data-ttu-id="afe22-111">Запросы переносимости</span><span class="sxs-lookup"><span data-stu-id="afe22-111">Portability requests</span></span>|<span data-ttu-id="afe22-112">Субъект данных может выполнить запрос переносимости данных, означающий, частично, что вы должны экспортировать личные данные субъекта данных из вашей системы и предоставить их в структурированном обычно используемом формате.</span><span class="sxs-lookup"><span data-stu-id="afe22-112">A data subject can make a data portability request, meaning, in part, that you must export the data subject's personal data from your systems and provide it in in a structured, commonly used format.</span></span> <span data-ttu-id="afe22-113">Для ответа на такие запросы используйте программу Data Privacy Utility для экспорта личных данных в файл Excel.</span><span class="sxs-lookup"><span data-stu-id="afe22-113">To respond to these requests, use the Data Privacy Utility to export personal data to an Excel file.</span></span> <span data-ttu-id="afe22-114">С помощью Excel можно изменить личные данные и сохранить их в широко используемом формате, пригодном для компьютеров, например CSV или XML.</span><span class="sxs-lookup"><span data-stu-id="afe22-114">Using Excel, you can edit the personal data and save it in a commonly used, machine-readable format, such as .csv or .xml.</span></span> <span data-ttu-id="afe22-115">Администраторы могут также экспортировать данные с использованием пакетов конфигурации Rapid Start, а затем настроить главные таблицы данных и связанные с ними таблицы, содержащие личные данные.</span><span class="sxs-lookup"><span data-stu-id="afe22-115">Administrators can also export data using Rapid Start configuration packages, and then configure master data tables and their related tables that contain personal data.</span></span> |
|<span data-ttu-id="afe22-116">Запросы удаления</span><span class="sxs-lookup"><span data-stu-id="afe22-116">Requests for deletion</span></span>|<span data-ttu-id="afe22-117">Субъект данных может запросить удаление своих личных данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-117">A data subject can request that you delete their personal data.</span></span> <span data-ttu-id="afe22-118">Существует несколько способов удалить личные данные с помощью настраиваемых возможностей, но вы отвечаете за принятие решения и реализацию.</span><span class="sxs-lookup"><span data-stu-id="afe22-118">There are several ways to delete personal data using the customization capabilities, but the decision and implementation is your responsibility.</span></span> <span data-ttu-id="afe22-119">В некоторых случаях можно выбрать прямое редактирование своих данных, например, удаление контакта и затем выполнение пакетного задания удаления отмененных взаимодействий для удаления взаимодействий для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="afe22-119">In some cases, you may choose to directly edit your data, for example deleting a contact and then running the Delete Canceled Interaction batch job to delete interactions for the contact.</span></span> <br><br> <span data-ttu-id="afe22-120">**Примечание.** Если указана дата в поле **Разрешить удаление документа до** на странице **Настройка модуля "Продажи"** или **Настройка модуля "Покупки"**, может потребоваться изменить дату, чтобы можно было удалить учтенные документы продаж и покупок, которые были напечатаны и которые имеют даты учета в эту дату или до нее.</span><span class="sxs-lookup"><span data-stu-id="afe22-120">**Note:** If you have specified a date in the **Allow Document Deletion Before** field on the **Sales & Receivables Setup** or **Purchases & Payables Setup** pages, you might need to change the date so that you can delete posted sales and purchase documents that you have printed and that have posting dates on or before that date.</span></span>|
|<span data-ttu-id="afe22-121">Запросы на исправление</span><span class="sxs-lookup"><span data-stu-id="afe22-121">Requests for correction</span></span>|<span data-ttu-id="afe22-122">Субъект данных может запросить исправление ошибок в своих личных данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-122">A data subject can request that you correct inaccurate personal data.</span></span> <span data-ttu-id="afe22-123">Существует несколько способов сделать это.</span><span class="sxs-lookup"><span data-stu-id="afe22-123">There are several ways to do so.</span></span> <span data-ttu-id="afe22-124">В некоторых случаях можно экспортировать списки в Excel для быстрого исправления нескольких записей, а затем импортировать обновленные данные.</span><span class="sxs-lookup"><span data-stu-id="afe22-124">In some cases, you can export lists to Excel to quickly bulk-edit multiple records, and then import the updated data.</span></span> <span data-ttu-id="afe22-125">Дополнительные сведения см. в разделе [Экспорт бизнес-данных в Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data).</span><span class="sxs-lookup"><span data-stu-id="afe22-125">For more information, see [Exporting your Business Data to Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data).</span></span> <span data-ttu-id="afe22-126">Можно также вручную отредактировать поля, которые содержат личные данные, например изменить информацию о клиенте в карточке клиента.</span><span class="sxs-lookup"><span data-stu-id="afe22-126">You can also manually edit fields that contain personal data, such as editing information about a customer in the Customer card.</span></span> <span data-ttu-id="afe22-127">Однако записи транзакций, такие как общие операции, операции клиента и операции книги налогов, являются важными для целостности системы планирования ресурсов предприятия.</span><span class="sxs-lookup"><span data-stu-id="afe22-127">However, transaction records such as general, customer, and tax ledger entries are essential to the integrity of the enterprise resource planning system.</span></span> <span data-ttu-id="afe22-128">Если личные данные хранятся в записях бизнес-транзакций, подумайте об использовании возможностей настройки для изменения таких личных данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-128">If you store personal data in business transaction records, consider using the customization capabilities to modify such personal data.</span></span>|

## <a name="restrict-data-processing-for-a-data-subject"></a><span data-ttu-id="afe22-129">Ограничение обработки данных для субъекта данных</span><span class="sxs-lookup"><span data-stu-id="afe22-129">Restrict Data Processing for a Data Subject</span></span>
<span data-ttu-id="afe22-130">Субъект данных может запросить временную приостановку обработки своих личных данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-130">A data subject can request that you temporarily stop processing their personal data.</span></span> <span data-ttu-id="afe22-131">Для удовлетворения таких запросов можно пометить запись такого субъекта как заблокированную из-за конфиденциальности, чтобы остановить обработку их данных.</span><span class="sxs-lookup"><span data-stu-id="afe22-131">To honor such requests, you can mark their record as blocked due to privacy to stop processing their data.</span></span> <span data-ttu-id="afe22-132">Когда запись отмечена как заблокированная, вы не можете создавать новые транзакции, которые используют эту запись.</span><span class="sxs-lookup"><span data-stu-id="afe22-132">When a record is marked as blocked, you cannot create new transactions that use that record.</span></span> <span data-ttu-id="afe22-133">Например, нельзя создать новый счет для клиента, если клиент или менеджер по продажам заблокирован.</span><span class="sxs-lookup"><span data-stu-id="afe22-133">For example, you cannot create a new invoice for a customer when either the customer or the salesperson is blocked.</span></span> <span data-ttu-id="afe22-134">Чтобы пометить субъекта данных как заблокированного, откройте карточку субъекта данных, например карточку клиента, поставщика или контакта, и установите флажок **Заблокировано из-за конфиденциальности**.</span><span class="sxs-lookup"><span data-stu-id="afe22-134">To mark a data subject as blocked, open the card for the data subject, for example the Customer, Vendor, or Contact cards, and choose the **Privacy Blocked** check box.</span></span> <span data-ttu-id="afe22-135">Может потребоваться выбрать **Показать больше** для отображения этого поля.</span><span class="sxs-lookup"><span data-stu-id="afe22-135">You may need to choose **Show More** to display the field.</span></span>

## <a name="handling-data-about-minors"></a><span data-ttu-id="afe22-136">Обработка данных о несовершеннолетних</span><span class="sxs-lookup"><span data-stu-id="afe22-136">Handling Data About Minors</span></span>
<span data-ttu-id="afe22-137">Если возраст контактного лица меньше официального возраста совершеннолетия в соответствии с законодательством вашего региона, это можно указать, установив флажок **Несовершеннолетний** на карточке **Контакт**.</span><span class="sxs-lookup"><span data-stu-id="afe22-137">If a contact person's age is below the age of legal consent according to the laws in your region, you can indicate that by choosing the **Minor** check box on the **Contact** card.</span></span> <span data-ttu-id="afe22-138">При этом автоматически устанавливается флажок **Заблокировано из-за конфиденциальности**.</span><span class="sxs-lookup"><span data-stu-id="afe22-138">When you do, the **Privacy Blocked** check box is automatically selected.</span></span> <span data-ttu-id="afe22-139">При получении согласия от родителей или официального опекуна несовершеннолетнего вы можете установить флажок **Родительское согласие получено**, чтобы разблокировать контакт.</span><span class="sxs-lookup"><span data-stu-id="afe22-139">When you receive consent from the minor's parent or legal guardian, you can choose the **Parental Consent Received** check box to unblock the contact.</span></span> <span data-ttu-id="afe22-140">Хотя можно обрабатывать личные данные несовершеннолетних, нельзя использовать функцию профилирования в Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="afe22-140">Though you can process personal data for minors, you cannot use the profiling functionality in Microsoft Dynamics 365 for Sales.</span></span>

> [!Note]
> <span data-ttu-id="afe22-141">Журнал изменений может регистрировать такие сведения, как когда и кем был установлен флажок **Родительское согласие получено**.</span><span class="sxs-lookup"><span data-stu-id="afe22-141">The Change Log can record details such as when, and by whom, the **Parental Consent Received** check box was chosen.</span></span> <span data-ttu-id="afe22-142">Администратор может настроить это, используя руководство **Настройка журнала изменений**, и также выбрав флажок **Фиксировать в журнале изменение флажка полученного родительского согласия** в карточке **Контакт**.</span><span class="sxs-lookup"><span data-stu-id="afe22-142">An administrator can set that up by using the **Change Log Setup** guide, and also choosing the **Log Modification for Parental Consent Received** check box on the **Contact** card.</span></span> <span data-ttu-id="afe22-143">Дополнительные сведения см. в разделе [Регистрация изменений](/dynamics-nav-app/across-log-changes).</span><span class="sxs-lookup"><span data-stu-id="afe22-143">For more information, see [Logging Changes](/dynamics-nav-app/across-log-changes).</span></span>  

## <a name="see-also"></a><span data-ttu-id="afe22-144">См. также</span><span class="sxs-lookup"><span data-stu-id="afe22-144">See Also</span></span>
[<span data-ttu-id="afe22-145">Классификация данных</span><span class="sxs-lookup"><span data-stu-id="afe22-145">Classifying Data</span></span>](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[<span data-ttu-id="afe22-146">Классификация конфиденциальности данных</span><span class="sxs-lookup"><span data-stu-id="afe22-146">Classifying Data Sensitivity</span></span>](admin-classifying-data-sensitivity.md)  
[<span data-ttu-id="afe22-147">Экспорт бизнес-данных в Excel</span><span class="sxs-lookup"><span data-stu-id="afe22-147">Exporting your Business Data to Excel</span></span>](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  
