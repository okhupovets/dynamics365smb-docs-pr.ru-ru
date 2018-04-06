---
title: "Настройка нескольких процентных ставок"
description: "Можно вычислять финансовые сборы с несколькими процентными ставками за определенный период. Расчет процентов аналогичен для всех финансовых издержек, изменяются только проценты за определенный период."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="66afb-104">Настройка нескольких процентных ставок</span><span class="sxs-lookup"><span data-stu-id="66afb-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="66afb-105">Несколько процентных ставок используются для различных периодов для задержанных платежей в торговых транзакциях.</span><span class="sxs-lookup"><span data-stu-id="66afb-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="66afb-106">Например, государство определяет максимальный процент, начисляемый потребителю.</span><span class="sxs-lookup"><span data-stu-id="66afb-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="66afb-107">Данную процентную ставку можно изменять дважды в год 1-го января и 1-го июля.</span><span class="sxs-lookup"><span data-stu-id="66afb-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="66afb-108">Процентная ставка между компаниями (B2B) устанавливается по соглашению сторон, и для этой группе клиентов нет ограничений.</span><span class="sxs-lookup"><span data-stu-id="66afb-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="66afb-109">Объявленная ставка обычно на 4 процента выше обычного банковского процента.</span><span class="sxs-lookup"><span data-stu-id="66afb-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="66afb-110">При создании условий финансовых ставок и условий напоминания для штрафов за задержанный платеж можно определить несколько процентных ставок, чтобы начисленные пени вычислялись с разными процентными ставками за различные периоды.</span><span class="sxs-lookup"><span data-stu-id="66afb-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="66afb-111">Дополнительные сведения см. в разделе [Сбор непогашенных остатков задолженности](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="66afb-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="66afb-112">Настройка нескольких процентных ставок</span><span class="sxs-lookup"><span data-stu-id="66afb-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="66afb-113">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Процентные ставки**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="66afb-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66afb-114">В окне **Процентные ставки** выберите требуемые финансовые условия, затем выберите действие **Процентные ставки**.</span><span class="sxs-lookup"><span data-stu-id="66afb-114">In the **Finance Charge Terms** window, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="66afb-115">Заполните соответствующим образом поля.</span><span class="sxs-lookup"><span data-stu-id="66afb-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="66afb-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="66afb-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="66afb-117">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Условия напоминания**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="66afb-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="66afb-118">В окне **Условия напоминания** выберите требуемые условия напоминания, затем выберите действие **Уровни**.</span><span class="sxs-lookup"><span data-stu-id="66afb-118">In the **Reminder Terms** window, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="66afb-119">В окне **Уровни напоминаний** выберите поле **Вычислить процент**.</span><span class="sxs-lookup"><span data-stu-id="66afb-119">In the **Reminder Levels** window, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="66afb-120">При выпуске процент-ноты в ней отображаются финансовые сборы с несколькими процентными ставками за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="66afb-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="66afb-121">Кредит-нота также содержит контактные сведения клиента, организации, выпускающей кредит-ноту, дополнительную сумму и общую сумму.</span><span class="sxs-lookup"><span data-stu-id="66afb-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="66afb-122">Открывающая операция кредит-ноты отображается жирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="66afb-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="66afb-123">Финансовые сборы рассчитываются с несколькими процентными ставками для определенного временного периода и печатаются после открывающей операции кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="66afb-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66afb-124">См. также</span><span class="sxs-lookup"><span data-stu-id="66afb-124">See Also</span></span>  
[<span data-ttu-id="66afb-125">Сбор непогашенных остатков задолженности</span><span class="sxs-lookup"><span data-stu-id="66afb-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="66afb-126">Настройка финансов</span><span class="sxs-lookup"><span data-stu-id="66afb-126">Setting Up Finance</span></span>](finance-setup-finance.md)
