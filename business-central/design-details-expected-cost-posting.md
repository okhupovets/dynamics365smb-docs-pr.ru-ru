---
title: "Сведения о проектировании — учет ожидаемой себестоимости | Документы Майкрософт"
description: "Ожидаемые значения себестоимости представляют оценку, например, себестоимости приобретенного товара, регистрируемую до получения счета на товар."
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
ms.openlocfilehash: 50ac9cbb946fedc687eb5ea1373c99d68f3d322b
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-expected-cost-posting"></a><span data-ttu-id="57b02-103">Сведения о проектировании: учет ожидаемой себестоимости</span><span class="sxs-lookup"><span data-stu-id="57b02-103">Design Details: Expected Cost Posting</span></span>
<span data-ttu-id="57b02-104">Ожидаемые значения себестоимости представляют оценку, например, себестоимости приобретенного товара, регистрируемую до получения счета на товар.</span><span class="sxs-lookup"><span data-stu-id="57b02-104">Expected costs represent the estimation of, for example, a purchased item’s cost that you record before you receive the invoice for the item.</span></span>  

 <span data-ttu-id="57b02-105">Можно выполнить учет ожидаемой себестоимости в запасах и главной книге.</span><span class="sxs-lookup"><span data-stu-id="57b02-105">You can post expected cost to inventory and to the general ledger.</span></span> <span data-ttu-id="57b02-106">При учете количества, которое было получено или отгружено, но счет за которое не выставлен, создается операция стоимости с ожидаемой себестоимостью.</span><span class="sxs-lookup"><span data-stu-id="57b02-106">When you post a quantity that is only received or shipped but not invoiced, then a value entry is created with the expected cost.</span></span> <span data-ttu-id="57b02-107">Ожидаемая себестоимость влияет на стоимость запасов, но не учитывается в ГК, если только система специально на это не настроена.</span><span class="sxs-lookup"><span data-stu-id="57b02-107">This expected cost affects the inventory value, but is not posted to the general ledger unless you set up the system up to do so.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="57b02-108">Управление ожидаемыми значениями себестоимости осуществляется только для транзакций товаров.</span><span class="sxs-lookup"><span data-stu-id="57b02-108">Expected costs are only managed for item transactions.</span></span> <span data-ttu-id="57b02-109">Ожидаемые значения себестоимости не являются типами нематериальных транзакций, например производственные мощности и товарные издержки.</span><span class="sxs-lookup"><span data-stu-id="57b02-109">Expected costs are not for immaterial transaction types, such as capacity and item charges.</span></span>  

 <span data-ttu-id="57b02-110">Если учитывается только часть количества прихода склада, стоимость запасов в главной книге не меняется, если не установлен флажок **Учет ожидаемой себест. в ГК** в окне **Настройка модуля "Запасы"**.</span><span class="sxs-lookup"><span data-stu-id="57b02-110">If only the quantity part of an inventory increase has been posted, then the inventory value in the general ledger does not change unless you have selected the **Expected Cost Posting to G/L** check box in the **Inventory Setup** window.</span></span> <span data-ttu-id="57b02-111">В этом случае ожидаемая себестоимость учитывается на промежуточных счетах во время приемки.</span><span class="sxs-lookup"><span data-stu-id="57b02-111">In that case, the expected cost is posted to interim accounts at the time of receipt.</span></span> <span data-ttu-id="57b02-112">После выставления счета по приходу в полном размере промежуточные счета балансируют, и фактическая себестоимость учитывается на финансовом счете товаров.</span><span class="sxs-lookup"><span data-stu-id="57b02-112">After the receipt has been fully invoiced, the interim accounts are then balanced and the actual cost is posted to the inventory account.</span></span>  

 <span data-ttu-id="57b02-113">Для обеспечения поддержки выверки и отслеживания операция оценки, за которую выставлен счет, показывает ожидаемое количество затрат, учтенное для того, чтобы уравновесить промежуточные счета.</span><span class="sxs-lookup"><span data-stu-id="57b02-113">To support reconciliation and traceability work, the invoiced value entry shows the expected cost amount that has been posted to balance the interim accounts.</span></span>  

## <a name="example"></a><span data-ttu-id="57b02-114">Пример</span><span class="sxs-lookup"><span data-stu-id="57b02-114">Example</span></span>  
 <span data-ttu-id="57b02-115">В следующем примере показана ожидаемая стоимость, если флажки **Автомат. учет себест.** и **Учет ожидаемой себест. в ГК** установлены в окне **Настройка модуля "Запасы"**.</span><span class="sxs-lookup"><span data-stu-id="57b02-115">The following example shows expected cost if the **Automatic Cost Posting** check box and the **Expected Cost Posting to G/L** check box are selected in the **Inventory Setup** window.</span></span>  

 <span data-ttu-id="57b02-116">Заказ на покупку учитывается как полученный.</span><span class="sxs-lookup"><span data-stu-id="57b02-116">You post a purchase order as received.</span></span> <span data-ttu-id="57b02-117">Ожидаемая стоимость равна 95,00 руб.</span><span class="sxs-lookup"><span data-stu-id="57b02-117">The expected cost is LCY 95.00.</span></span>  

 <span data-ttu-id="57b02-118">**Операции стоимости**</span><span class="sxs-lookup"><span data-stu-id="57b02-118">**Value Entries**</span></span>  

|<span data-ttu-id="57b02-119">Дата учета</span><span class="sxs-lookup"><span data-stu-id="57b02-119">Posting Date</span></span>|<span data-ttu-id="57b02-120">Тип операции</span><span class="sxs-lookup"><span data-stu-id="57b02-120">Entry Type</span></span>|<span data-ttu-id="57b02-121">Сумма себестоимости (ожид.)</span><span class="sxs-lookup"><span data-stu-id="57b02-121">Cost Amount (Expected)</span></span>|<span data-ttu-id="57b02-122">Ожид. стоимость, учтенная в ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-122">Expected Cost Posted to G/L</span></span>|<span data-ttu-id="57b02-123">Ожидаемая себестоимость</span><span class="sxs-lookup"><span data-stu-id="57b02-123">Expected Cost</span></span>|<span data-ttu-id="57b02-124">Номер товарной операции</span><span class="sxs-lookup"><span data-stu-id="57b02-124">Item Ledger Entry No.</span></span>|<span data-ttu-id="57b02-125">Номер операции</span><span class="sxs-lookup"><span data-stu-id="57b02-125">Entry No.</span></span>|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="57b02-126">01-01-20</span><span class="sxs-lookup"><span data-stu-id="57b02-126">01-01-20</span></span>|<span data-ttu-id="57b02-127">Прямая себестоимость</span><span class="sxs-lookup"><span data-stu-id="57b02-127">Direct Cost</span></span>|<span data-ttu-id="57b02-128">95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-128">95.00</span></span>|<span data-ttu-id="57b02-129">95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-129">95.00</span></span>|<span data-ttu-id="57b02-130">Да</span><span class="sxs-lookup"><span data-stu-id="57b02-130">Yes</span></span>|<span data-ttu-id="57b02-131">1</span><span class="sxs-lookup"><span data-stu-id="57b02-131">1</span></span>|<span data-ttu-id="57b02-132">1</span><span class="sxs-lookup"><span data-stu-id="57b02-132">1</span></span>|  

 <span data-ttu-id="57b02-133">**Операции отношений в ГК – Таблица Связь с книгой товаров**</span><span class="sxs-lookup"><span data-stu-id="57b02-133">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="57b02-134">Номер операции ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-134">G/L Entry No.</span></span>|<span data-ttu-id="57b02-135">Номер операции стоимости</span><span class="sxs-lookup"><span data-stu-id="57b02-135">Value Entry No.</span></span>|<span data-ttu-id="57b02-136">Номер регистра ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-136">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="57b02-137">1</span><span class="sxs-lookup"><span data-stu-id="57b02-137">1</span></span>|<span data-ttu-id="57b02-138">1</span><span class="sxs-lookup"><span data-stu-id="57b02-138">1</span></span>|<span data-ttu-id="57b02-139">1</span><span class="sxs-lookup"><span data-stu-id="57b02-139">1</span></span>|  
|<span data-ttu-id="57b02-140">2</span><span class="sxs-lookup"><span data-stu-id="57b02-140">2</span></span>|<span data-ttu-id="57b02-141">1</span><span class="sxs-lookup"><span data-stu-id="57b02-141">1</span></span>|<span data-ttu-id="57b02-142">1</span><span class="sxs-lookup"><span data-stu-id="57b02-142">1</span></span>|  

 <span data-ttu-id="57b02-143">**Записи Главной книги**</span><span class="sxs-lookup"><span data-stu-id="57b02-143">**General Ledger Entries**</span></span>  

|<span data-ttu-id="57b02-144">Дата учета</span><span class="sxs-lookup"><span data-stu-id="57b02-144">Posting Date</span></span>|<span data-ttu-id="57b02-145">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-145">G/L Account</span></span>|<span data-ttu-id="57b02-146">Номер счета (пример для En-US)</span><span class="sxs-lookup"><span data-stu-id="57b02-146">Account No. (En-US Demo)</span></span>|<span data-ttu-id="57b02-147">Сумма</span><span class="sxs-lookup"><span data-stu-id="57b02-147">Amount</span></span>|<span data-ttu-id="57b02-148">Номер операции</span><span class="sxs-lookup"><span data-stu-id="57b02-148">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="57b02-149">01-01-20</span><span class="sxs-lookup"><span data-stu-id="57b02-149">01-01-20</span></span>|<span data-ttu-id="57b02-150">Нарастающий счет запасов (промежуточный)</span><span class="sxs-lookup"><span data-stu-id="57b02-150">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="57b02-151">5530</span><span class="sxs-lookup"><span data-stu-id="57b02-151">5530</span></span>|<span data-ttu-id="57b02-152">-95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-152">-95.00</span></span>|<span data-ttu-id="57b02-153">2</span><span class="sxs-lookup"><span data-stu-id="57b02-153">2</span></span>|  
|<span data-ttu-id="57b02-154">01-01-20</span><span class="sxs-lookup"><span data-stu-id="57b02-154">01-01-20</span></span>|<span data-ttu-id="57b02-155">Счет запасов (промежуточный)</span><span class="sxs-lookup"><span data-stu-id="57b02-155">Inventory Account (Interim)</span></span>|<span data-ttu-id="57b02-156">2131</span><span class="sxs-lookup"><span data-stu-id="57b02-156">2131</span></span>|<span data-ttu-id="57b02-157">95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-157">95.00</span></span>|<span data-ttu-id="57b02-158">1</span><span class="sxs-lookup"><span data-stu-id="57b02-158">1</span></span>|  

 <span data-ttu-id="57b02-159">Позже заказ на покупку можно учесть как заказ, по которому выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="57b02-159">At a later date, you post the purchase order as invoiced.</span></span> <span data-ttu-id="57b02-160">Стоимость по счету — 100,00 руб.</span><span class="sxs-lookup"><span data-stu-id="57b02-160">The invoiced cost is LCY 100.00.</span></span>  

 <span data-ttu-id="57b02-161">**Операции стоимости**</span><span class="sxs-lookup"><span data-stu-id="57b02-161">**Value Entries**</span></span>  

|<span data-ttu-id="57b02-162">Дата учета</span><span class="sxs-lookup"><span data-stu-id="57b02-162">Posting Date</span></span>|<span data-ttu-id="57b02-163">Сумма себестоимости (факт.)</span><span class="sxs-lookup"><span data-stu-id="57b02-163">Cost Amount (Actual)</span></span>|<span data-ttu-id="57b02-164">Сумма себестоимости (ожид.)</span><span class="sxs-lookup"><span data-stu-id="57b02-164">Cost Amount (Expected)</span></span>|<span data-ttu-id="57b02-165">Стоимость, учтенная в ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-165">Cost Posted to G/L</span></span>|<span data-ttu-id="57b02-166">Ожидаемая себестоимость</span><span class="sxs-lookup"><span data-stu-id="57b02-166">Expected Cost</span></span>|<span data-ttu-id="57b02-167">Номер товарной операции</span><span class="sxs-lookup"><span data-stu-id="57b02-167">Item Ledger Entry No.</span></span>|<span data-ttu-id="57b02-168">Номер операции</span><span class="sxs-lookup"><span data-stu-id="57b02-168">Entry No.</span></span>|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="57b02-169">01-15-20</span><span class="sxs-lookup"><span data-stu-id="57b02-169">01-15-20</span></span>|<span data-ttu-id="57b02-170">100,00</span><span class="sxs-lookup"><span data-stu-id="57b02-170">100.00</span></span>|<span data-ttu-id="57b02-171">-95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-171">-95.00</span></span>|<span data-ttu-id="57b02-172">100,00</span><span class="sxs-lookup"><span data-stu-id="57b02-172">100.00</span></span>|<span data-ttu-id="57b02-173">Нет</span><span class="sxs-lookup"><span data-stu-id="57b02-173">No</span></span>|<span data-ttu-id="57b02-174">1</span><span class="sxs-lookup"><span data-stu-id="57b02-174">1</span></span>|<span data-ttu-id="57b02-175">2</span><span class="sxs-lookup"><span data-stu-id="57b02-175">2</span></span>|  

 <span data-ttu-id="57b02-176">**Операции отношений в ГК – Таблица Связь с книгой товаров**</span><span class="sxs-lookup"><span data-stu-id="57b02-176">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="57b02-177">Номер операции ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-177">G/L Entry No.</span></span>|<span data-ttu-id="57b02-178">Номер операции стоимости</span><span class="sxs-lookup"><span data-stu-id="57b02-178">Value Entry No.</span></span>|<span data-ttu-id="57b02-179">Номер регистра ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-179">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="57b02-180">3</span><span class="sxs-lookup"><span data-stu-id="57b02-180">3</span></span>|<span data-ttu-id="57b02-181">2</span><span class="sxs-lookup"><span data-stu-id="57b02-181">2</span></span>|<span data-ttu-id="57b02-182">2</span><span class="sxs-lookup"><span data-stu-id="57b02-182">2</span></span>|  
|<span data-ttu-id="57b02-183">4</span><span class="sxs-lookup"><span data-stu-id="57b02-183">4</span></span>|<span data-ttu-id="57b02-184">2</span><span class="sxs-lookup"><span data-stu-id="57b02-184">2</span></span>|<span data-ttu-id="57b02-185">2</span><span class="sxs-lookup"><span data-stu-id="57b02-185">2</span></span>|  
|<span data-ttu-id="57b02-186">5</span><span class="sxs-lookup"><span data-stu-id="57b02-186">5</span></span>|<span data-ttu-id="57b02-187">2</span><span class="sxs-lookup"><span data-stu-id="57b02-187">2</span></span>|<span data-ttu-id="57b02-188">2</span><span class="sxs-lookup"><span data-stu-id="57b02-188">2</span></span>|  
|<span data-ttu-id="57b02-189">6</span><span class="sxs-lookup"><span data-stu-id="57b02-189">6</span></span>|<span data-ttu-id="57b02-190">2</span><span class="sxs-lookup"><span data-stu-id="57b02-190">2</span></span>|<span data-ttu-id="57b02-191">2</span><span class="sxs-lookup"><span data-stu-id="57b02-191">2</span></span>|  

 <span data-ttu-id="57b02-192">**Записи Главной книги**</span><span class="sxs-lookup"><span data-stu-id="57b02-192">**General Ledger Entries**</span></span>  

|<span data-ttu-id="57b02-193">Дата учета</span><span class="sxs-lookup"><span data-stu-id="57b02-193">Posting Date</span></span>|<span data-ttu-id="57b02-194">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="57b02-194">G/L Account</span></span>|<span data-ttu-id="57b02-195">Номер счета (пример для En-US)</span><span class="sxs-lookup"><span data-stu-id="57b02-195">Account No. (En-US Demo)</span></span>|<span data-ttu-id="57b02-196">Сумма</span><span class="sxs-lookup"><span data-stu-id="57b02-196">Amount</span></span>|<span data-ttu-id="57b02-197">Номер операции</span><span class="sxs-lookup"><span data-stu-id="57b02-197">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="57b02-198">01-15-20</span><span class="sxs-lookup"><span data-stu-id="57b02-198">01-15-20</span></span>|<span data-ttu-id="57b02-199">Нарастающий счет запасов (промежуточный)</span><span class="sxs-lookup"><span data-stu-id="57b02-199">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="57b02-200">5530</span><span class="sxs-lookup"><span data-stu-id="57b02-200">5530</span></span>|<span data-ttu-id="57b02-201">95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-201">95.00</span></span>|<span data-ttu-id="57b02-202">4</span><span class="sxs-lookup"><span data-stu-id="57b02-202">4</span></span>|  
|<span data-ttu-id="57b02-203">01-15-20</span><span class="sxs-lookup"><span data-stu-id="57b02-203">01-15-20</span></span>|<span data-ttu-id="57b02-204">Счет запасов (промежуточный)</span><span class="sxs-lookup"><span data-stu-id="57b02-204">Inventory Account (Interim)</span></span>|<span data-ttu-id="57b02-205">2131</span><span class="sxs-lookup"><span data-stu-id="57b02-205">2131</span></span>|<span data-ttu-id="57b02-206">-95,00</span><span class="sxs-lookup"><span data-stu-id="57b02-206">-95.00</span></span>|<span data-ttu-id="57b02-207">3</span><span class="sxs-lookup"><span data-stu-id="57b02-207">3</span></span>|  
|<span data-ttu-id="57b02-208">01-15-20</span><span class="sxs-lookup"><span data-stu-id="57b02-208">01-15-20</span></span>|<span data-ttu-id="57b02-209">Счет для примененных прямых затрат</span><span class="sxs-lookup"><span data-stu-id="57b02-209">Direct Cost Applied Account</span></span>|<span data-ttu-id="57b02-210">7291</span><span class="sxs-lookup"><span data-stu-id="57b02-210">7291</span></span>|<span data-ttu-id="57b02-211">-100</span><span class="sxs-lookup"><span data-stu-id="57b02-211">-100</span></span>|<span data-ttu-id="57b02-212">6</span><span class="sxs-lookup"><span data-stu-id="57b02-212">6</span></span>|  
|<span data-ttu-id="57b02-213">01-15-20</span><span class="sxs-lookup"><span data-stu-id="57b02-213">01-15-20</span></span>|<span data-ttu-id="57b02-214">Счет запасов</span><span class="sxs-lookup"><span data-stu-id="57b02-214">Inventory Account</span></span>|<span data-ttu-id="57b02-215">2130</span><span class="sxs-lookup"><span data-stu-id="57b02-215">2130</span></span>|<span data-ttu-id="57b02-216">100</span><span class="sxs-lookup"><span data-stu-id="57b02-216">100</span></span>|<span data-ttu-id="57b02-217">5</span><span class="sxs-lookup"><span data-stu-id="57b02-217">5</span></span>|  

## <a name="see-also"></a><span data-ttu-id="57b02-218">См. также</span><span class="sxs-lookup"><span data-stu-id="57b02-218">See Also</span></span>
 <span data-ttu-id="57b02-219">[Сведения о проектировании: себестоимость запасов](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="57b02-219">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="57b02-220">[Сведения о проектировании: коррекция себестоимости](design-details-cost-adjustment.md) </span><span class="sxs-lookup"><span data-stu-id="57b02-220">[Design Details: Cost Adjustment](design-details-cost-adjustment.md) </span></span>  
 <span data-ttu-id="57b02-221">[Сведения о проектировании: выверка с главной книгой](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="57b02-221">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
 <span data-ttu-id="57b02-222">[Сведения о проектировании: учет запасов](design-details-inventory-posting.md) </span><span class="sxs-lookup"><span data-stu-id="57b02-222">[Design Details: Inventory Posting](design-details-inventory-posting.md) </span></span>  
 [<span data-ttu-id="57b02-223">Сведения о проектировании: отклонение</span><span class="sxs-lookup"><span data-stu-id="57b02-223">Design Details: Variance</span></span>](design-details-variance.md)  
 [<span data-ttu-id="57b02-224">Управление себестоимостью товаров</span><span class="sxs-lookup"><span data-stu-id="57b02-224">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="57b02-225">Финансы</span><span class="sxs-lookup"><span data-stu-id="57b02-225">Finance</span></span>](finance.md)  
 <span data-ttu-id="57b02-226">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57b02-226">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
