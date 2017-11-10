---
title: "Определение статических распределений на основе отношения распределений | Документы Майкрософт"
description: "Метод статического распределения основан на конкретном значении, таком как занятая площадь в квадратных метрах или заданное соотношение распределения (например, 5:2: 4)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: ru-ru
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Пример сценария. Определение статических распределений на основе отношения распределений
Метод статического распределения основан на конкретном значении, таком как занятая площадь в квадратных метрах или заданное соотношение распределения (например, 5:2: 4).  

В этом разделе описывается, как определить три новых объекта затрат цели распределения для места возникновения затрат ПРОД источника распределения с использованием принятого соотношения распределения 5:2:4. Три целевых объекта затрат: ПРИНАДЛЕЖНОСТИ, КРАСКА и ФИТИНГИ.  

> [!NOTE]  
>  В примере используются демонстрационные данные в [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Определение места возникновения затрат ПРОД по источнику распределения на экспресс-вкладке "Общее"  

1.  Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Распределение затрат**, затем выберите связанную ссылку.  
2.  В окне **Распределение затрат** выберите действие **Создать**.  
3.  В поле **ИД** нажмите кнопку ВВОД или введите идентификатор.  
4.  В поле **Уровень** введите **1**.  
5.  В полях **Действительно с** и **Действительно по** введите соответствующие даты.  
6.  В поле **Код центра затрат** введите **ПРОИЗВ**.  
7.  В поле **Кредит по типу затрат** введите тип затрат **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Определение объектов затрат по целям распределения на экспресс-вкладке "Строки"  

1.  В первой строке, в поле **Тип назначения затрат** укажите **9903**.  
2.  В первой строке, в поле **Целевой объект затрат** выберите **ACCESSO**.  
3.  На первой строке в поле **Тип назначения распределения** выберите **Все затраты**, чтобы определить способ распределения всех начисленных средств.  
4.  В первой строке в поле **База** выберите **Статический**, чтобы использовать метод статического распределения.  
5.  В первой строке в поле **Доля** введите соотношение распределения **5**.  
6.  Во второй строке в поле **Тип назначения затрат** укажите **9903**.  
7.  Во второй строке в поле **Целевой объект затрат** выберите **PAINT**.  
8.  На второй строке в поле **Тип назначения распределения** выберите **Все затраты**, чтобы определить способ распределения всех начисленных средств.  
9. Во второй строке в поле **База** выберите **Статический**, чтобы использовать метод статического распределения.  
10. Во второй строке в поле **Доля** введите соотношение распределения **2**.  
11. В третьей строке в поле **Тип назначения затрат** укажите **9903**.  
12. В третьей строке в поле **Целевой объект затрат** выберите **FITTINGS**.  
13. В третьей строке в поле **Тип назначения распределения** выберите **Все затраты**, чтобы определить способ распределения всех начисленных средств.  
14. В третьей строке в поле **База** выберите **Статический**, чтобы использовать метод статического распределения.  
15. В третьей строке в поле **Доля** введите соотношение распределения **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] автоматически вычисляет поле **Процент** с помощью процента, который зависит от всех трех соотношений распределения, которые вводятся в поле **Доля** для всех трех строк.  

## <a name="see-also"></a>См. также  
[Практическое руководство. Настройка источника и целей распределения](finance-how-to-set-up-allocation-source-and-targets.md)   
[Определение и распределение затрат](finance-define-and-allocate-costs.md)   
[Пример сценария. Определение динамических распределений на основе проданных товаров](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Определение и распределение затрат](finance-define-and-allocate-costs.md)
