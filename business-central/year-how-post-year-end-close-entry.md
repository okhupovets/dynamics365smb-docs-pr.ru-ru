---
title: Проверка и учет операции закрытия года | Документация Майкрософт
description: Описывается порядок открытия журнала, указанного в пакетном задании "Закрытие отчета о прибылях и убытках", и проверки и учета операции закрытия года.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191743"
---
# <a name="post-the-year-end-closing-entry"></a>Учет операции закрытия года
После использования пакетного задания **Закрытие отчета о прибылях и убытках** для создания закрывающей операции (операций) на конец года необходимо открыть журнал, указанный для пакетного задания, и затем просмотреть и учесть записи.

## <a name="to-post-the-year-end-closing-entry"></a>Учет операции закрытия года
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовый журнал**, затем выберите соответствующую ссылку.
2. На странице **Финансовый журнал** в поле **Код раздела** выберите раздел, который содержит закрывающие операции.
3. Проверьте записи.
4. Чтобы учесть журнал, выберите действие **Учет**.

> [!NOTE]  
>   При обнаружении ошибки отображается сообщение об ошибке. Если учет выполнен успешно, система удалит учтенные записи из журнала. После завершения учета запись учитывается во всех счетах прибылей и убытков, при этом ее сальдо становится нулевым, и результат года переносится в балансовый отчет.

## <a name="see-also"></a>См. также
[Закрытие учетных периодов](year-close-account-periods.md)  
[Закрытие книг](year-close-books.md)  
[Закрытие отчета о прибылях и убытках](year-close-income-statement.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
