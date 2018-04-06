---
title: "Настройка веб-источников в контактных организациях | Документы Майкрософт"
description: "Вы можете определить интернет- и веб-источники и назначить их контактной организации, чтобы вам было проще находить информацию о своих контактах."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4fb61c804d1f01326349d7733e52de48811c18e3
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="312e1-103">Настройка веб-источников для контактных организаций</span><span class="sxs-lookup"><span data-stu-id="312e1-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="312e1-104">Можно присваивать веб-источники с контактными организациям, чтобы определять, например, поисковые системы и веб-сайты в Интернете, которые должны использоваться для поиска информации о контактах.</span><span class="sxs-lookup"><span data-stu-id="312e1-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="312e1-105">При присвоении веб-источников указывается, какую поисковую систему и какое слово поиска приложение использует для поиска требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="312e1-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="312e1-106">Использование веб-источников для контактов — это двухэтапный процесс.</span><span class="sxs-lookup"><span data-stu-id="312e1-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="312e1-107">Сначала вы определяете код веб-источника.</span><span class="sxs-lookup"><span data-stu-id="312e1-107">First, you define the web source code.</span></span> <span data-ttu-id="312e1-108">Этот шаг нужно выполнить один раз для каждого веб-источника.</span><span class="sxs-lookup"><span data-stu-id="312e1-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="312e1-109">После настройки кода веб-источника можно начинать назначение кода контактным лицам.</span><span class="sxs-lookup"><span data-stu-id="312e1-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="312e1-110">Определение кода веб-источника</span><span class="sxs-lookup"><span data-stu-id="312e1-110">To define a web source code</span></span>
1. <span data-ttu-id="312e1-111">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Веб-источники**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="312e1-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="312e1-112">Выберите действия **Создать**.</span><span class="sxs-lookup"><span data-stu-id="312e1-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="312e1-113">Заполните поля **Код**, **Описание** и **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="312e1-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="312e1-114">В поле **URL-адрес** введите %1 для вставки заполнителя для слова поиска в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="312e1-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="312e1-115">При запуске веб-источника из контакта %1 заменяется на слово поиска (например, на название организации), которое было введено в окне **Веб-источники контакта**.</span><span class="sxs-lookup"><span data-stu-id="312e1-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="312e1-116">Повторите эти шаги, чтобы настроить необходимое количество веб-источников.</span><span class="sxs-lookup"><span data-stu-id="312e1-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="312e1-117">Назначение веб-источников контактной организации</span><span class="sxs-lookup"><span data-stu-id="312e1-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="312e1-118">При назначении веб-источников вы указываете, какую поисковую систему и какое слово поиска приложение будет использовать для поиска требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="312e1-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="312e1-119">Откройте контакт.</span><span class="sxs-lookup"><span data-stu-id="312e1-119">Open the contact.</span></span>
2. <span data-ttu-id="312e1-120">Выберите действие **Организация**, а затем — действие **Веб-источники**.</span><span class="sxs-lookup"><span data-stu-id="312e1-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="312e1-121">Откроется окно **Веб-источники контакта**.</span><span class="sxs-lookup"><span data-stu-id="312e1-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="312e1-122">В поле **Код веб-источника** выберите веб-источник, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="312e1-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="312e1-123">В поле **Поиск слова** введите искомое слово, используемое для поиска информации.</span><span class="sxs-lookup"><span data-stu-id="312e1-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="312e1-124">Повторите эти шаги для назначения желаемого количества веб-источников.</span><span class="sxs-lookup"><span data-stu-id="312e1-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="312e1-125">Также можно назначать веб-источники в окне **Список контактов**, следуя той же процедуре.</span><span class="sxs-lookup"><span data-stu-id="312e1-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="312e1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="312e1-126">See Also</span></span>
[<span data-ttu-id="312e1-127">Создание контактных организаций</span><span class="sxs-lookup"><span data-stu-id="312e1-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="312e1-128">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="312e1-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
