---
title: "Транзакции между компаниями в одной организации | Документы Майкрософт"
description: "С помощью функции межфирменного учета можно упростить бизнес-процессы и транзакции между компаниями в пределах одной организации."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c68e4bd69c854ecd99cfb833c941066d9a805da
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="managing-intercompany-transactions"></a><span data-ttu-id="0663f-103">Управление межфирменными транзакциями</span><span class="sxs-lookup"><span data-stu-id="0663f-103">Managing Intercompany Transactions</span></span>
<span data-ttu-id="0663f-104">Ваша организация может состоять из нескольких компаний, но не иметь соответствующего количества бухгалтерских и административных отделов.</span><span class="sxs-lookup"><span data-stu-id="0663f-104">Your organization may consist of several companies, but might not have the equivalent number of accounting and administrative teams.</span></span> <span data-ttu-id="0663f-105">Функция межфирменного учета позволяет вести дела с филиалами и внутренними партнерскими организациями таким же образом, как с внешними поставщиками и клиентами.</span><span class="sxs-lookup"><span data-stu-id="0663f-105">The Intercompany functionality lets you do business with your subsidiary and internal partner organizations in the same way as you engage with your external vendors and customers.</span></span> <span data-ttu-id="0663f-106">Ввод данных о транзакциях с аффилированной организацией в соответствующих документах осуществляется только один раз.</span><span class="sxs-lookup"><span data-stu-id="0663f-106">You enter intercompany transaction information only once in the appropriate documents.</span></span> <span data-ttu-id="0663f-107">Вы можете использовать уже знакомые функции, например, управление расчетами с клиентами и поставщиками.</span><span class="sxs-lookup"><span data-stu-id="0663f-107">You can use the functionality you are already familiar with, such as receivables and payables management.</span></span> <span data-ttu-id="0663f-108">Средства сопоставления для плана счетов и измерения помогают обеспечить отображение данных в нужных местах.</span><span class="sxs-lookup"><span data-stu-id="0663f-108">Mapping facilities for the chart of accounts and dimensions help ensure that information appears in the right places.</span></span>  

<span data-ttu-id="0663f-109">Существует четыре основных преимущества использования функции межфирменного учета:</span><span class="sxs-lookup"><span data-stu-id="0663f-109">There are four main benefits to the Intercompany functionality:</span></span>  

- <span data-ttu-id="0663f-110">Увеличение производительности в результате экономии времени и упрощения транзакций</span><span class="sxs-lookup"><span data-stu-id="0663f-110">Increased productivity as a result of time saved and simplified transactions</span></span>  
- <span data-ttu-id="0663f-111">Минимизация вероятности ошибок при однократном вводе информации и автоматических обновлений на системном уровне</span><span class="sxs-lookup"><span data-stu-id="0663f-111">Minimized error potential with one-time entry of information and system-wide, automated updates</span></span>  
- <span data-ttu-id="0663f-112">Полный журнал аудита, полное видение бизнес-процессов и истории транзакций</span><span class="sxs-lookup"><span data-stu-id="0663f-112">Complete audit trail and full visibility into business activities and transaction histories</span></span>  
- <span data-ttu-id="0663f-113">Эффективные, экономичные транзакции с филиалами и дочерними организациями</span><span class="sxs-lookup"><span data-stu-id="0663f-113">Efficient, cost-effective transactions with affiliate and subsidiary companies</span></span>  

<span data-ttu-id="0663f-114">Вы полностью контролируете все документы по транзакциям.</span><span class="sxs-lookup"><span data-stu-id="0663f-114">You are in full control of all transaction documents.</span></span> <span data-ttu-id="0663f-115">Например, вы можете отклонить отправленный вам документ и сторнировать неверно учтенные операции.</span><span class="sxs-lookup"><span data-stu-id="0663f-115">For example, you can reject a document sent to you and, in this way, reverse postings that were incorrect.</span></span> <span data-ttu-id="0663f-116">Или, в случае покупки у партнера или дочерней компании, можно обновлять заказ на покупку до тех пор, пока продавец не отгрузит товары.</span><span class="sxs-lookup"><span data-stu-id="0663f-116">Or, when making a purchase from a partner or subsidiary company, you can update the purchase order as long as the selling company has not shipped any goods.</span></span>  

<span data-ttu-id="0663f-117">При вводе транзакции нет необходимости указывать счета для отдельных наборов журналов, достаточно дать идентификатор организации-партнера.</span><span class="sxs-lookup"><span data-stu-id="0663f-117">When you enter a transaction, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="0663f-118">Функция межфирменного учета создает строки финансового журнала, которые обеспечивают балансировку журналов обеих организаций, участвующих в транзакции.</span><span class="sxs-lookup"><span data-stu-id="0663f-118">The Intercompany functionality creates general journal lines that result in the balancing of the books of both companies involved in a transaction.</span></span> <span data-ttu-id="0663f-119">В счетах дебиторов и кредиторов пользователь назначает межфирменный код партнера любому клиенту или поставщику.</span><span class="sxs-lookup"><span data-stu-id="0663f-119">In receivables and payables, you assign an intercompany partner code to any customer or vendor.</span></span> <span data-ttu-id="0663f-120">Начиная с этого момента все генерируемые заказы и счета, относящиеся к транзакциям с этими организациями, генерируют документы в партнерской организации с правильным сальдо счетов.</span><span class="sxs-lookup"><span data-stu-id="0663f-120">From that moment on, all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>  

 <span data-ttu-id="0663f-121">Создав в системе бизнес-партнеров в качестве клиентов и поставщиков, и назначив им коды партнеров по межфирменным операциям, можно обмениваться межфирменными документами покупок и продаж, включая товары и номера товарных издержек.</span><span class="sxs-lookup"><span data-stu-id="0663f-121">After you set up business partners as customers and vendors in the system, and assign them intercompany partner codes, it is possible to exchange intercompany purchase and sales documents, including items and item charges.</span></span> <span data-ttu-id="0663f-122">Функция межфирменного учета обеспечивает межфирменные транзакции между несколькими базами данных, например в разных странах или регионах, а также в разных валютах, разных планах счетов, разных измерениях и при различной нумерации товаров.</span><span class="sxs-lookup"><span data-stu-id="0663f-122">The Intercompany functionality allows intercompany transactions between multiple databases, for example, in different countries/regions, as well as multiple currencies, different charts of accounts, different dimensions, and different item numbering.</span></span>  

<span data-ttu-id="0663f-123">В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.</span><span class="sxs-lookup"><span data-stu-id="0663f-123">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

 |<span data-ttu-id="0663f-124">По</span><span class="sxs-lookup"><span data-stu-id="0663f-124">To</span></span> |<span data-ttu-id="0663f-125">Ссылка</span><span class="sxs-lookup"><span data-stu-id="0663f-125">See</span></span>|
 |---|---|
 |<span data-ttu-id="0663f-126">Создание межфирменных поставщиков и клиентов как так называемых межфирменных партнеров (партнеры МФ) и настройка межфирменного плана счетов.</span><span class="sxs-lookup"><span data-stu-id="0663f-126">Create your intercompany vendors and customers as so-called intercompany partners, and set up an intercompany chart of accounts.</span></span>|[<span data-ttu-id="0663f-127">Настройка межфирменных взаимодействий</span><span class="sxs-lookup"><span data-stu-id="0663f-127">Set Up Intercompany</span></span>](intercompany-how-setup.md)|
 |<span data-ttu-id="0663f-128">Использование межфирменных документов или журналов для учета транзакций, выполненных с межфирменными партнерами.</span><span class="sxs-lookup"><span data-stu-id="0663f-128">Use intercompany documents or journals to post transactions with your intercompany partners.</span></span>|[<span data-ttu-id="0663f-129">Работа с межфирменными документами и журналами</span><span class="sxs-lookup"><span data-stu-id="0663f-129">Work with Intercompany Documents and Journals</span></span>](intercompany-how-work-documents-journals.md)|
 |<span data-ttu-id="0663f-130">Упорядочение и обработка входящих и исходящих транзакций, которыми вы обмениваетесь с межфирменными партнерами.</span><span class="sxs-lookup"><span data-stu-id="0663f-130">Organize and process incoming and outgoing transactions that you exchange with your intercompany partners.</span></span>|[<span data-ttu-id="0663f-131">Управление межфирменными входящими и исходящими ящиками</span><span class="sxs-lookup"><span data-stu-id="0663f-131">Manage the Intercompany Inbox and Outbox</span></span>](intercompany-how-manage-intercompany-inbox.md)|

## <a name="see-also"></a><span data-ttu-id="0663f-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0663f-132">See Also</span></span>
[<span data-ttu-id="0663f-133">Финансы</span><span class="sxs-lookup"><span data-stu-id="0663f-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="0663f-134">Настройка финансов</span><span class="sxs-lookup"><span data-stu-id="0663f-134">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="0663f-135">Работа с финансовыми журналами</span><span class="sxs-lookup"><span data-stu-id="0663f-135">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="0663f-136">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0663f-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
