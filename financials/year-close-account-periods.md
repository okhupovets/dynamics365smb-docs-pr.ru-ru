---
title: "Практическое руководство. Закрытие учетных периодов | Документы Майкрософт"
description: "Описывает, как закрывать учетные периоды."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 69bea225084f239523c4ed67471b52ad91e914d9
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-close-accounting-periods"></a>Как завершать учетные периоды
При завершении финансового года следует завершить периоды, которые его образуют.

## <a name="to-close-accounting-periods"></a>Практическое руководство. Закрытие учетных периодов
1. В правом вернем углу щелкните значок **Поиск страницы или отчета** ![Поиск страницы или отчета](media/ui-search/search_small.png "значок "Поиск страницы или отчета""), введите **Учетные периоды** и выберите связанную ссылку.
2. В окне **Учетные периоды** выберите действие **Закрыть год**.

    Если открыто несколько финансовых лет, автоматически считается, что должен быть закрыт более ранний год. Отображается сообщение, указывающее подлежащий закрытию год и сообщающее о последствиях закрытия года.
3. Для закрытия года нажмите кнопку **Да**.

Финансовый год закрыт, и выбираются поля **Закрыто** и **Дата закрыта** для всех периодов в таком году. Финансовый год не может быть открыт снова, и флажок из полей **Закрыто** или **Дата закрыта** удалить нельзя.

**Примечание**. Нельзя закрыть финансовый год, если прежде не будет открыт новый финансовый год. Следует отметить, что после закрытия финансового года уже невозможно изменить дату начала следующего финансового года.

Несмотря на то, что финансовый год закрыт, можно по-прежнему производить учет ГК операций по нему. При этом операции будут помечаться как учтенные по закрытому финансовому году, и будет выбрано поле **Операция прошлого года**.

После закрытия финансового года счета прибылей и убытков следует закрыть, а результаты года должны быть перемещены на счет в балансовом отчете. Эти действия можно повторять при каждом учете закрытого финансового года.

## <a name="see-also"></a>См. также
[Закрытие книг](year-close-books.md)  
[Практическое руководство. Учет операции закрытия года](year-how-post-year-end-close-entry.md)  
[Практическое руководство. Открытие нового финансового года](finance-how-open-new-fiscal-year.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
