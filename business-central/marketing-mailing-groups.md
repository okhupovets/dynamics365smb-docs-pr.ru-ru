---
title: "Настройка групп рассылки для контактов | Документы Майкрософт"
description: "Вы можете использовать группы рассылки для идентификации групп контактов, которые должны получать одни и те же сведения, например в рамках маркетинговой кампании."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 92173c1df5f105ad9156c34ab7050ef1546127bc
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="682df-103">Настройка групп рассылки для контактов</span><span class="sxs-lookup"><span data-stu-id="682df-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="682df-104">Группы рассылки можно использовать для определения групп контактов, которые должны получать одинаковую информацию.</span><span class="sxs-lookup"><span data-stu-id="682df-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="682df-105">Например, можно настроить группу рассылки для контактов, которым нужно послать уведомление о переезде офиса, или другую группу для отправки подарков к праздникам.</span><span class="sxs-lookup"><span data-stu-id="682df-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="682df-106">Использование групп рассылки для контактов — это двухэтапный процесс.</span><span class="sxs-lookup"><span data-stu-id="682df-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="682df-107">Сначала вы определяете код группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="682df-107">First, you define the mailing group code.</span></span> <span data-ttu-id="682df-108">Этот шаг нужно выполнить один раз для каждой группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="682df-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="682df-109">После настройки кода группы рассылки можно начинать назначение кода контактным организациям.</span><span class="sxs-lookup"><span data-stu-id="682df-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="682df-110">Определение кодов групп рассылки</span><span class="sxs-lookup"><span data-stu-id="682df-110">To define mailing group codes</span></span>
<span data-ttu-id="682df-111">Код группы рассылки определяет тип или категорию группы, например ПЕРЕЕЗД для переезда офиса или ПОДАРОК для праздничных подарков.</span><span class="sxs-lookup"><span data-stu-id="682df-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="682df-112">Допускается наличие нескольких кодов отраслевых групп.</span><span class="sxs-lookup"><span data-stu-id="682df-112">You can have several industry group codes.</span></span> <span data-ttu-id="682df-113">Для определения отраслевых групп используется окно **Группы рассылки**.</span><span class="sxs-lookup"><span data-stu-id="682df-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="682df-114">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Группы рассылки**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="682df-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="682df-115">Выберите действие **Создать**, введите код и описание.</span><span class="sxs-lookup"><span data-stu-id="682df-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="682df-116">Длина кода не должна превышать 11 знаков (допускается сочетание букв и цифр).</span><span class="sxs-lookup"><span data-stu-id="682df-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="682df-117">Назначение групп рассылки контакту</span><span class="sxs-lookup"><span data-stu-id="682df-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="682df-118">Откройте контакт.</span><span class="sxs-lookup"><span data-stu-id="682df-118">Open the contact.</span></span>
2. <span data-ttu-id="682df-119">Выберите действие **Группы рассылки**.</span><span class="sxs-lookup"><span data-stu-id="682df-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="682df-120">Откроется окно **Группы рассылки контакта**.</span><span class="sxs-lookup"><span data-stu-id="682df-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="682df-121">В поле **Код группы рассылки** выберите группу рассылки, которую нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="682df-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="682df-122">Повторите эти шаги для назначения желаемого количества групп рассылки.</span><span class="sxs-lookup"><span data-stu-id="682df-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="682df-123">Также можно назначать группы рассылки из списка контактов, следуя той же процедуре.</span><span class="sxs-lookup"><span data-stu-id="682df-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="682df-124">Число групп рассылки, назначенных контакту, отображается в поле **Число групп рассылки** в разделе **Сегментация** в окне **Контакт**.</span><span class="sxs-lookup"><span data-stu-id="682df-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="682df-125">После назначения контактам групп рассылки можно использовать эту информацию для выбора контактов для сегмента.</span><span class="sxs-lookup"><span data-stu-id="682df-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="682df-126">Дополнительные сведения см. в разделе [Добавление контактов к сегментам](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="682df-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="682df-127">См. также</span><span class="sxs-lookup"><span data-stu-id="682df-127">See Also</span></span>
[<span data-ttu-id="682df-128">Создание контактных организаций</span><span class="sxs-lookup"><span data-stu-id="682df-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="682df-129">Создание контактных лиц</span><span class="sxs-lookup"><span data-stu-id="682df-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="682df-130">Работа с Financials</span><span class="sxs-lookup"><span data-stu-id="682df-130">Working with Financials</span></span>](ui-work-product.md)
