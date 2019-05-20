---
title: Импорт нескольких изображений товаров из ZIP-файла | Документы Майкрософт
description: Можно импортировать несколько изображений товаров за один раз. Просто присвойте файлам изображений имена, соответствующие номера ваших товаров, упакуйте из в ZIP-файл, затем с помощью страницы "Импорт изображений товаров" управляйте тем, какие изображения товаров следует импортировать.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243070"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="0ab6d-104">Импорт нескольких изображений товаров</span><span class="sxs-lookup"><span data-stu-id="0ab6d-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="0ab6d-105">Можно импортировать несколько изображений товаров за один раз.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="0ab6d-106">Просто присвойте файлам изображений имена, соответствующие номера ваших товаров, упакуйте из в ZIP-файл, затем с помощью страницы **Импорт изображений товаров** управляйте тем, какие изображения товаров следует импортировать.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="0ab6d-107">Поддерживаются все распространенные форматы файлов.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="0ab6d-108">Присвоение файлам изображений названий товаров и подготовка ZIP-файла</span><span class="sxs-lookup"><span data-stu-id="0ab6d-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="0ab6d-109">В месте, в котором хранятся изображения товаров, назовите каждый файл в соответствии с номером связанного товара.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="0ab6d-110">Например:</span><span class="sxs-lookup"><span data-stu-id="0ab6d-110">For example:</span></span>

    |<span data-ttu-id="0ab6d-111">Код товара</span><span class="sxs-lookup"><span data-stu-id="0ab6d-111">Item No.</span></span>|<span data-ttu-id="0ab6d-112">Имя файла</span><span class="sxs-lookup"><span data-stu-id="0ab6d-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="0ab6d-113">1000</span><span class="sxs-lookup"><span data-stu-id="0ab6d-113">1000</span></span>|<span data-ttu-id="0ab6d-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="0ab6d-114">1000.bmp</span></span>|
    |<span data-ttu-id="0ab6d-115">1001</span><span class="sxs-lookup"><span data-stu-id="0ab6d-115">1001</span></span>|<span data-ttu-id="0ab6d-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="0ab6d-116">1001.bmp</span></span>|
    |<span data-ttu-id="0ab6d-117">1002</span><span class="sxs-lookup"><span data-stu-id="0ab6d-117">1002</span></span>|<span data-ttu-id="0ab6d-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="0ab6d-118">1002.bmp</span></span>|

2. <span data-ttu-id="0ab6d-119">Соберите все файлы в ZIP-файл.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="0ab6d-120">Например, в Проводнике Windows выберите файлы, затем выберите **Отправить**, **Сжатая папка**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="0ab6d-121">Импорт изображений товаров</span><span class="sxs-lookup"><span data-stu-id="0ab6d-121">To import item pictures</span></span>
1. <span data-ttu-id="0ab6d-122">Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка модуля "Запасы"**, затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0ab6d-123">Выберите действие **Импорт изображений товаров**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="0ab6d-124">В поле **Выбор ZIP-файла** выберите соответствующую ZIP-папку, затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="0ab6d-125">Строка для каждого товара и изображения создается на странице **Импорт изображений товаров**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ab6d-126">Для карточек товаров, на которых уже есть изображение, установлен флажок **Изображение уже существует**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="0ab6d-127">Если вы не хотите заменять никакие существующие изображения, снимите флажок **Заменять изображения**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="0ab6d-128">Если не требуется заменять отдельные существующие изображения, удалите соответствующие строки.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="0ab6d-129">Выберите действие **Импорт изображений**.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="0ab6d-130">Поле **Статус импорта** обновляется для отображения того, был ли импорт изображения пропущен или завершен.</span><span class="sxs-lookup"><span data-stu-id="0ab6d-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="0ab6d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0ab6d-131">See Also</span></span>
[<span data-ttu-id="0ab6d-132">Регистрация новых товаров</span><span class="sxs-lookup"><span data-stu-id="0ab6d-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0ab6d-133">Создание серий номеров</span><span class="sxs-lookup"><span data-stu-id="0ab6d-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="0ab6d-134">Запасы</span><span class="sxs-lookup"><span data-stu-id="0ab6d-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0ab6d-135">Покупки</span><span class="sxs-lookup"><span data-stu-id="0ab6d-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0ab6d-136">Продажи</span><span class="sxs-lookup"><span data-stu-id="0ab6d-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="0ab6d-137">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ab6d-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>