---
title: "Отслеживание действий пользователей в журнале изменений | Документы Майкрософт"
description: "Вы можете активизировать журнал пользователя, чтобы у вас была история всех изменений, внесенных в данные в отслеживаемых таблицах."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fe5bac9b47ccaca4cb3c1bdac7cda6b8d5ebbfd4
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="02567-103">Изменение ведения журналов в Business Central</span><span class="sxs-lookup"><span data-stu-id="02567-103">Logging Changes in Business Central</span></span>
<span data-ttu-id="02567-104">Можно включить журнал изменений в [!INCLUDE[d365fin](includes/d365fin_md.md)], чтобы иметь историю действий.</span><span class="sxs-lookup"><span data-stu-id="02567-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="02567-105">Журнал основывается на изменениях, внесенных в данные таблиц, по которым выполняется отслеживание. В журнале изменений операции хронологически упорядочены, а также показывает изменения, примененные к полям в определенных таблицах.</span><span class="sxs-lookup"><span data-stu-id="02567-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="02567-106">Журнал изменений записывает все изменения в таблице.</span><span class="sxs-lookup"><span data-stu-id="02567-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="02567-107">Работа с журналом изменений</span><span class="sxs-lookup"><span data-stu-id="02567-107">Working with the Change Log</span></span>
<span data-ttu-id="02567-108">Обычной проблемой со многих финансовых системах является выявление источника происхождения ошибок и изменений в данных.</span><span class="sxs-lookup"><span data-stu-id="02567-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="02567-109">Это может быть все что угодно — от неправильно введенного номера телефона клиента, до неправильного учета в Главной книге.</span><span class="sxs-lookup"><span data-stu-id="02567-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="02567-110">Журнал изменений позволяет отслеживать все изменения, внесенные пользователем непосредственно в данные базы данных.</span><span class="sxs-lookup"><span data-stu-id="02567-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="02567-111">Необходимо указать каждую таблицу и поле, которые система должна записывать в журнал, после чего следует активировать журнал изменений.</span><span class="sxs-lookup"><span data-stu-id="02567-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="02567-112">Можно активировать и деактивировать журнал изменений в окне **Настройка журнала изменений**.</span><span class="sxs-lookup"><span data-stu-id="02567-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="02567-113">Когда вы активируете или деактивируйте журнал изменений, это действие регистрируется, чтобы всегда можно было просмотреть, какой пользователь деактивировал или повторно активировал журнал изменений.</span><span class="sxs-lookup"><span data-stu-id="02567-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="02567-114">Эта функция не может быть отключена.</span><span class="sxs-lookup"><span data-stu-id="02567-114">This cannot be turned off.</span></span>  

<span data-ttu-id="02567-115">В окне **Настройка журнала изменений**, если выбрать действие **Таблицы**, можно указать, для каких таблиц требуется отслеживать изменения и какие изменения требуется отслеживаться. [!INCLUDE[d365fin](includes/d365fin_md.md)] также отслеживает несколько системных таблиц.</span><span class="sxs-lookup"><span data-stu-id="02567-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="02567-116">После настройки журнала изменений, его активации и внесения изменений в данные можно просмотреть и отфильтровать изменения в окне **Операции журнала изменений**.</span><span class="sxs-lookup"><span data-stu-id="02567-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="02567-117">Если требуется удалить операции, это можно сделать в окне **Удалить операции журнала изменений**, в котором можно установить фильтры на основе времени и даты.</span><span class="sxs-lookup"><span data-stu-id="02567-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="02567-118">См. также</span><span class="sxs-lookup"><span data-stu-id="02567-118">See Also</span></span>
[<span data-ttu-id="02567-119">Изменение базовых настроек</span><span class="sxs-lookup"><span data-stu-id="02567-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="02567-120">Сортировка</span><span class="sxs-lookup"><span data-stu-id="02567-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="02567-121">Использование поиска страницы или отчета</span><span class="sxs-lookup"><span data-stu-id="02567-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="02567-122">[Управление пользователями и разрешениями](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="02567-122">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="02567-123">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02567-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
