---
title: "Настройка для сервисных товаров и компонентов сервисных товаров | Документы Майкрософт"
description: "Узнайте, что необходимо настроить, чтобы можно было использовать сервисные товары, включая такие значения по умолчанию, как время отклика, процент скидки по контракту и ценовая группа сервиса."
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
ms.openlocfilehash: 050456758a2bf4f3489ed382103d5fed99e8fada
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="f2e8e-103">Настройка сервисных товаров и компонентов сервисных товаров</span><span class="sxs-lookup"><span data-stu-id="f2e8e-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="f2e8e-104">Для работы с сервисными товарами необходимо настроить следующее</span><span class="sxs-lookup"><span data-stu-id="f2e8e-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="f2e8e-105">Группы сервисных товаров.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-105">Service item groups.</span></span>
* <span data-ttu-id="f2e8e-106">Необязательно</span><span class="sxs-lookup"><span data-stu-id="f2e8e-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="f2e8e-107">Чтобы настроить группы сервисных товаров</span><span class="sxs-lookup"><span data-stu-id="f2e8e-107">To set up service item groups</span></span>
<span data-ttu-id="f2e8e-108">Можно настроить группы товаров, которые связаны друг с другом в плане ремонта и обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="f2e8e-109">Можно определить значения по умолчанию для сервисных товаров в группах сервисных товаров, такие как время отклика, процент скидки по контракту и ценовая группа сервиса.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="f2e8e-110">Для товаров внутри группы сервисных товаров можно указать, следует ли регистрировать их автоматически как сервисные товары при их продаже.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="f2e8e-111">Товарам назначаются группы сервисных товаров в карточке **Товар**, а сервисным товарам – в карточке **Сервисный товар**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="f2e8e-112">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Группы сервисных товаров**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f2e8e-113">Создать новую группу сервисных товаров.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="f2e8e-114">Заполните поля **Код** и **Описание**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="f2e8e-115">В поле **Скидка по контракту по умолчанию (%)** введите требуемые стандартные проценты скидки контракта для сервисных товаров группы.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="f2e8e-116">В поле **Код ценовой группы обслуж. по умолч.** введите требуемую стандартную ценовую группу сервиса для сервисных товаров группы.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="f2e8e-117">В поле **Время отклика по умолчанию (часы)** введите требуемое стандартное время отклика в часах для сервисных товаров группы.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="f2e8e-118">Если нужно, чтобы при продаже товары группы регистрировались в программе как сервисные, выберите поле **Создать сервисный товар**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="f2e8e-119">Настройка компонентов сервисного товара</span><span class="sxs-lookup"><span data-stu-id="f2e8e-119">To set up service item components</span></span>
<span data-ttu-id="f2e8e-120">Сервисный товар может состоять из нескольких компонентов, которые могут быть заменены запчастями при обслуживании товара.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="f2e8e-121">Эти компоненты настраиваются на странице **Сервисный товар - список компонентов**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="f2e8e-122">Кроме того, если нужно настроить компоненты сервисных товаров, являющихся спецификациями, можно скопировать товары спецификаций и создать их как компоненты сервисного товара.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="f2e8e-123">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Сервисные товары**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="f2e8e-124">Откройте сервисный товар, для которого нужно настроить компоненты.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="f2e8e-125">Выберите действие **Компоненты**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-125">Choose the **Components** action.</span></span> <span data-ttu-id="f2e8e-126">Откроется окно **Сервисный товар - список компонентов**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="f2e8e-127">Добавьте новый компонент.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-127">Add a new component.</span></span>  
5. <span data-ttu-id="f2e8e-128">В поле **Тип** выберите **Сервисный товар**, если сам компонент зарегистрирован как сервисный товар.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="f2e8e-129">В противном случае выберите **Товар**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="f2e8e-130">В поле **Номер**</span><span class="sxs-lookup"><span data-stu-id="f2e8e-130">In the **No.**</span></span> <span data-ttu-id="f2e8e-131">выберите товар или сервисный товар, являющийся компонентом сервисного товара.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="f2e8e-132">Настройка компонентов сервисного товара из спецификации</span><span class="sxs-lookup"><span data-stu-id="f2e8e-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="f2e8e-133">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Сервисные товары**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f2e8e-134">Откройте сервисный товар, компоненты которого нужно настроить из спецификации.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="f2e8e-135">Выберите действие **Компоненты**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-135">Choose the **Components** action.</span></span> <span data-ttu-id="f2e8e-136">Откроется окно **Сервисный товар - список компонентов**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="f2e8e-137">Выберите действие **Копировать из спецификации**,</span><span class="sxs-lookup"><span data-stu-id="f2e8e-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="f2e8e-138">Если товар, с которым связан сервисный товар, является спецификацией, то компоненты для всех товаров в спецификации создаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="f2e8e-139">Настройка сервисной полки</span><span class="sxs-lookup"><span data-stu-id="f2e8e-139">To set up a service shelf</span></span>
<span data-ttu-id="f2e8e-140">Можно настроить сервисные полки, которые определяют место хранения сервисных товаров.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="f2e8e-141">Сервисные полки назначаются сервисным товарам на страницах **Сервисный заказ** и **Журнал сервисных товаров**.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="f2e8e-142">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Полки сервисных товаров**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="f2e8e-143">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="f2e8e-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2e8e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="f2e8e-144">See Also</span></span>
<span data-ttu-id="f2e8e-145">[Настройка кодов для стандартных сервисов](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="f2e8e-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="f2e8e-146">Настройка устранения проблем</span><span class="sxs-lookup"><span data-stu-id="f2e8e-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
