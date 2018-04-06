---
title: "Управление документами, удаление или сжатие документов | Документы Майкрософт"
description: "Можно хранить исторические данные или удалить их."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 292231a907970de2821daeba87003eca7bf54cdc
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a><span data-ttu-id="3f034-103">Управление документами</span><span class="sxs-lookup"><span data-stu-id="3f034-103">Manage Documents</span></span>
<span data-ttu-id="3f034-104">Исполнителю главной роли, например администратору приложения, приходится постоянно иметь дело с накапливающимися архивными документами (удалять или сжимать их).</span><span class="sxs-lookup"><span data-stu-id="3f034-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="3f034-105">Удаление документов</span><span class="sxs-lookup"><span data-stu-id="3f034-105">Delete Documents</span></span>
<span data-ttu-id="3f034-106">В определенных ситуациях может возникнуть потребность в удалении заказов на покупку с уже выставленными счетами, которые ещё не были удалены.</span><span class="sxs-lookup"><span data-stu-id="3f034-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> <span data-ttu-id="3f034-107">В [!INCLUDE[d365fin](includes/d365fin_md.md)] выполняется проверка наличия для удаленных заказов на покупку полностью выставленных счетов.</span><span class="sxs-lookup"><span data-stu-id="3f034-107">[!INCLUDE[d365fin](includes/d365fin_md.md)] checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="3f034-108">Невозможно удалить заказы, на которые не полностью выставлены счета и которые не полностью получены.</span><span class="sxs-lookup"><span data-stu-id="3f034-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="3f034-109">Возвраты обычно удаляются после выставления по ним счета.</span><span class="sxs-lookup"><span data-stu-id="3f034-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="3f034-110">Когда счет учтен, он переносится в окно **Учтенная кредит-нота покупки**.</span><span class="sxs-lookup"><span data-stu-id="3f034-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="3f034-111">Если установлен флажок **Возврат поставки по кредит-ноте** в окне **Настройка модуля покупок**, счет переносится в окно **Учтенный возврат поставки**.</span><span class="sxs-lookup"><span data-stu-id="3f034-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="3f034-112">Можно удалить документы с помощью пакетного задания **Удаление занесенных на счет возвратов покупки**.</span><span class="sxs-lookup"><span data-stu-id="3f034-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="3f034-113">Перед удалением пакетное задание проверяет, полностью ли отгружены заказы на возврат покупки и выставлены ли по ним счета.</span><span class="sxs-lookup"><span data-stu-id="3f034-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="3f034-114">Общие заказы на покупку не удаляются после обработки и выставления счёта по всем связанным заказам на покупку.</span><span class="sxs-lookup"><span data-stu-id="3f034-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="3f034-115">Можно удалить подобные заказы с помощью пакетного задания **Удалить общие заказы на покупку, по которым выставлены счета**.</span><span class="sxs-lookup"><span data-stu-id="3f034-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="3f034-116">Сервисные заказы, учтенные в счетах, обычно удаляются автоматически после выставления по ним счетов в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="3f034-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="3f034-117">Во время учета счета в окне **Учтенные сервисные счета** создается соответствующая запись.</span><span class="sxs-lookup"><span data-stu-id="3f034-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="3f034-118">Учтенный документ можно просматривать в окне **Учтенный сервисный счет**.</span><span class="sxs-lookup"><span data-stu-id="3f034-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="3f034-119">Однако сервисные заказы не удаляются автоматически, если общее количество по заказу было учтено не из самого заказа, а из окна **Сервисный счет**.</span><span class="sxs-lookup"><span data-stu-id="3f034-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="3f034-120">В этом случае может понадобиться удалить вручную заказы, по которым выставлены счета и которые не были удалены программой.</span><span class="sxs-lookup"><span data-stu-id="3f034-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="3f034-121">Это можно выполнить путем запуска пакетного задания **Удалить серв. заказы, по кот. выст. сч.**.</span><span class="sxs-lookup"><span data-stu-id="3f034-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f034-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3f034-122">See Also</span></span>  
[<span data-ttu-id="3f034-123">Настройка и администрирование в Business Central</span><span class="sxs-lookup"><span data-stu-id="3f034-123">Setup and Administration in Business Central</span></span>](admin-setup-and-administration.md)  
