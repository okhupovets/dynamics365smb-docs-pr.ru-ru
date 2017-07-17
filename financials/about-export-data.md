---
title: "Экспорт данных в Excel из Dynamics 365 for Financials | Документы Майкрософт"
description: "Узнайте, как экспортировать данные в Excel из Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 02/22/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 94b2bbcd3db4b5071221b6f24e0f960355db3af1
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="exporting-your-data-to-excel-from-dynamics-365-for-financials"></a>Экспорт данных в Excel из Dynamics 365 for Financials
Если вы хотите работать с данными из [!INCLUDE[d365fin](includes/d365fin_md.md)] в Excel, вы можете открыть все списки в Excel и работать с ними там. Аналогично, если требуется отменить подписку на [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], вы можете экспортировать данные в Excel, чтобы забрать их с собой.

## <a name="opening-lists-in-excel"></a>Открытие списков в Excel
Можно открыть данные в Excel из любого журнала, списка или листа. Для откройте требуемую станицу и выберите **Открыть в Excel**. Например, откройте список клиентов (поиск по слову **Клиенты**) и выберите **Открыть в Excel**. Ваш браузер выдаст запрос на открытие или сохранение созданной книги Excel.  

Каждый список включает число столбцов, а экспорт в Excel будет включать все столбцы, имеющиеся в текущем представлении. Если вы хотите добавить или удалить столбцы перед открытием списка в Excel, достаточно открыть контекстное меню для любого столбца, а затем указать, какие столбцы требуется отображать. Этот список столбцов отличается для большинства списков и отражает структуру в базе данных, в которой хранятся данные. Если вы не уверены, какой тип данных содержится в определенном столбце, вы можете добавить его в представление, а затем решить, требуется ли его снова удалить.  

## <a name="exporting-data-to-other-finance-systems"></a>Экспорт данных в другие финансовые системы
Если требуется отменить подписку на [!INCLUDE[d365fin](includes/d365fin_md.md)], вы можете экспортировать данные в Excel и перенести их в следующую финансовую систему.  

Конечно же, можно экспортировать все страницы, но, возможно, вам не потребуются все они. Таким образом, рассмотрите возможность экспортировать следующие важные страницы и не забудьте добавить столбцы, как описано ранее:  

* План счетов  
* Клиенты  
* Поставщики  
* Банки  
* Товары  

Если вам также требуются все финансовые транзакции, это большой объем данных, поэтому часто экспорт займет больше, чем несколько минут. Финансовые транзакции будут показаны на странице **Операции главной книги**.  

Рекомендуется также рассмотреть возможность экспорта данных со следующих страниц:  

* Книга операций по клиентам  
* Книга операций по поставщикам  
* Книга операций по банку/кассе  
* Книга операций по товарам  
* Общая настройка учета  
* Учетные группы клиента  
* Учетные группы поставщика  
* Товарные учетные группы  
* Учетная группа банка  
* Бюджеты ГК  
* Операции бюджета ГК  
* Предложения по продаже  
* Счета продажи  
* Счета покупок  
* Контакты  
* Менеджеры  

**Примечание**. Если настроено несколько организаций в [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], необходимо экспортировать соответствующие данные из каждой организации.

## <a name="see-also"></a>См. также
[Отмена подписки на [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](madeira-cancel.md)  
[Импорт бизнес-данных из других финансовых систем](upload-data.md)  
[Финансы](finance.md)  
[Общие бизнес-функции](ui-across-business-areas.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
