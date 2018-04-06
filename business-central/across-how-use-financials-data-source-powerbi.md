---
title: "Настройка отчетов для Business Central в Power BI | Документы Майкрософт"
description: "Можно сделать данные Financials доступными в качестве источника данных в Power BI и создать мощные отчеты о состоянии вашего бизнеса."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42939e97d121bd3a2abff91671d9f9571faffbfd
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="2b58b-103">Использование [!INCLUDE[d365fin](includes/d365fin_md.md)] как источника данных Power BI для создания отчетов</span><span class="sxs-lookup"><span data-stu-id="2b58b-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as Power BI Data Source for Building Reports</span></span>
<span data-ttu-id="2b58b-104">Можно сделать данные [!INCLUDE[d365fin](includes/d365fin_md.md)] доступными в качестве источника данных в Power BI и создать мощные отчеты о состоянии вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="2b58b-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

> [!NOTE]  
> <span data-ttu-id="2b58b-105">Вы должны иметь допустимую учетную запись в [!INCLUDE[d365fin](includes/d365fin_md.md)] и в Power BI.</span><span class="sxs-lookup"><span data-stu-id="2b58b-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="2b58b-106">Кроме того, необходимо загрузить [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="2b58b-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="2b58b-107">Добавление [!INCLUDE[d365fin](includes/d365fin_md.md)] как источника данных в Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b58b-107">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Power BI Desktop</span></span>
1. <span data-ttu-id="2b58b-108">В Power BI Desktop в левой области навигации выберите **Получить данные**.</span><span class="sxs-lookup"><span data-stu-id="2b58b-108">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="2b58b-109">В окне **Получить данные** выберите **Веб-службы**, выберите **Dynamics 365 Business Central**, затем нажмите кнопку **Подключиться**.</span><span class="sxs-lookup"><span data-stu-id="2b58b-109">In the **Get Data** window, choose **Online Services**, choose **Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="2b58b-110">Power BI отобразит мастер с руководством по [процессу подключения](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md).</span><span class="sxs-lookup"><span data-stu-id="2b58b-110">Power BI displays a wizard that will guide you through the [connection process](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md).</span></span> <span data-ttu-id="2b58b-111">Первый шаг — вход в службу.</span><span class="sxs-lookup"><span data-stu-id="2b58b-111">The first step will be to sign into the service.</span></span> <span data-ttu-id="2b58b-112">Выберите **Войти** и выберите учетную запись для входа.</span><span class="sxs-lookup"><span data-stu-id="2b58b-112">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="2b58b-113">Это должна быть та же учетная запись, которая использовалась для входа в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b58b-113">This should be the same account you sign into [!INCLUDE[d365fin](includes/d365fin_md.md)] with.</span></span>
4. <span data-ttu-id="2b58b-114">Нажмите кнопку **Подключиться**, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="2b58b-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="2b58b-115">Мастер Power BI отобразит список организаций и источников данных [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b58b-115">The Power BI wizard shows a list of [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="2b58b-116">Эти источники данных представляют все веб-службы, которые вы опубликовали из каждой организации в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b58b-116">These data source represent all the web services that you have published from each company in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
5. <span data-ttu-id="2b58b-117">Либо создайте новый URL-адрес веб-службы в [!INCLUDE[d365fin](includes/d365fin_md.md)], используя действие **Создать набор данных** на странице **Веб-службы** с помощью руководства по сопровождаемой настройке **Настройка отчетов** либо используя действие **Изменить в Excel** в любом списке.</span><span class="sxs-lookup"><span data-stu-id="2b58b-117">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="2b58b-118">Укажите данные, которые требуется добавить в модель данных, а затем нажмите кнопку **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="2b58b-118">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="2b58b-119">Повторите предыдущие шаги для добавления дополнительных данных [!INCLUDE[d365fin](includes/d365fin_md.md)] в модель данных Power BI.</span><span class="sxs-lookup"><span data-stu-id="2b58b-119">Repeat the previous steps to add additional [!INCLUDE[d365fin](includes/d365fin_md.md)] data to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="2b58b-120">После успешного подключения к [!INCLUDE[d365fin](includes/d365fin_md.md)] выполнять повторный вход не требуется.</span><span class="sxs-lookup"><span data-stu-id="2b58b-120">Once you have successfully connected to [!INCLUDE[d365fin](includes/d365fin_md.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="2b58b-121">После загрузки данные отобразятся в правой области навигации на странице.</span><span class="sxs-lookup"><span data-stu-id="2b58b-121">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="2b58b-122">На этом шаге вы успешно подключились с данным Business Central и готовы начать создание отчета Power BI.</span><span class="sxs-lookup"><span data-stu-id="2b58b-122">At this point, you have successfully connected to your Business Central data and are ready to begin building your Power BI report.</span></span> <span data-ttu-id="2b58b-123">Дополнительные сведения см. в разделе [Документация Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).</span><span class="sxs-lookup"><span data-stu-id="2b58b-123">For more information, see the [Power BI documentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b58b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2b58b-124">See Also</span></span>
[<span data-ttu-id="2b58b-125">Бизнес-аналитика</span><span class="sxs-lookup"><span data-stu-id="2b58b-125">Business Intelligence</span></span>](bi.md)  
<span data-ttu-id="2b58b-126">[Добро пожаловать в [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="2b58b-126">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="2b58b-127">Импорт бизнес-данных из других финансовых систем</span><span class="sxs-lookup"><span data-stu-id="2b58b-127">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="2b58b-128">[Настройка [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md) </span><span class="sxs-lookup"><span data-stu-id="2b58b-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md) </span></span>  
[<span data-ttu-id="2b58b-129">Финансы</span><span class="sxs-lookup"><span data-stu-id="2b58b-129">Finance</span></span>](finance.md)  
<span data-ttu-id="2b58b-130">[Подключение Power BI к [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)</span><span class="sxs-lookup"><span data-stu-id="2b58b-130">[Connecting Power BI to [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)</span></span>  
