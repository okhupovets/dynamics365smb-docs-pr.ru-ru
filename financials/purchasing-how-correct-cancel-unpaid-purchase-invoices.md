---
title: "Практическое руководство. Исправление или отмена неоплаченных счетов покупки | Документы Майкрософт"
description: "Практическое руководство. Исправление или отмена неоплаченных счетов покупки"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Практическое руководство. Исправление или отмена неоплаченных счетов покупки
Можно исправить или отменить учтенный счет покупки. Это используется, если нужно исправить опечатку либо внести изменение в покупку на раннем этапе обработки заказа.

Если продукты в учтенном счете покупки уже оплачены, его невозможно откорректировать или отменить из учтенного счета покупки. Вместо этого следует вручную создать кредит-ноту покупки для сторнирования покупки. Дополнительные сведения см. в разделе [Практическое руководство. Обработка возвратов покупки или отмен](purchasing-how-process-purchase-returns-cancellations.md)

В окне **Учтенный счет покупки** можно нажать кнопку **Исправить** или **Отмена**. При корректировке или отмене учтенного счета покупки корректирующая кредит-нота покупки применяется ко всем операциям ГК и журнала товаров, созданным при учете первоначального счета покупки. При этом сторнируется учтенный счет покупки в финансовых записях и оставляется корректирующая учтенная кредит-нота покупки для аудиторского следа. Ниже описано использование кнопок **Исправить** и **Отмена**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Коррекция учтенного счета покупки
1. В правом вернем углу щелкните значок **Поиск страницы или отчета** ![Поиск страницы или отчета](media/ui-search/search_small.png "значок "Поиск страницы или отчета""), введите **Учтенные счета покупки** и выберите связанную ссылку.  
2. Выберите учтенный счет покупки, который требуется откорректировать.  

    **Примечание**. Если установлен флажок **Отменено**, невозможно откорректировать учтенный счет покупки, поскольку он уже откорректирован или отменен.
3. В окне **Учтенный счет покупки** выберите **Исправить**.

    Создается новый счет покупки с теми же сведениями, в который можно внести изменения. Дополнительные сведения см. в разделе [Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md). Значение в поле **Отменено** в исходном учтенном счете покупки изменится на **Да**.

    Автоматически создается кредит-нота покупки, которая учитывается для аннулирования исходного учтенного счета покупки.
4. Выберите **Показать корректирующую кредит-ноту**, чтобы просмотреть учтенную кредит-ноту покупки, которая аннулирует исходный учтенный счет покупки.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Отмена учтенного счета покупки
1. В правом вернем углу щелкните значок **Поиск страницы или отчета** ![Поиск страницы или отчета](media/ui-search/search_small.png "значок "Поиск страницы или отчета""), введите **Учтенные счета покупки** и выберите связанную ссылку.  
2. Выберите учтенный счет покупки, который требуется отменить.

    **Примечание**. Если установлен флажок **Отменено**, невозможно отменить учтенный счет покупки, поскольку он уже откорректирован или отменен.
3. В окне **Учтенный счет покупки** выберите **Отмена**.

    Автоматически создается кредит-нота покупки, которая учитывается для аннулирования исходного учтенного счета покупки. Значение в поле **Отменено** в исходном учтенном счете покупки изменится на **Да**.
4. Выберите **Показать корректирующую кредит-ноту**, чтобы просмотреть учтенную кредит-ноту покупки, которая аннулирует исходный учтенный счет покупки.

## <a name="see-also"></a>См. также
[Покупки](purchasing-manage-purchasing.md)  
[Практическое руководство. Регистрация покупок](purchasing-how-record-purchases.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
