---
title: Планирование со складами или без складов | Документация Майкрософт
description: Важно понимать планирование с кодом склада или без кода склада в строках требования.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d9afd30c3b81912797ad95871256207d135b673
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783986"
---
# <a name="planning-with-or-without-locations"></a>Планирование со складами и без складов
Что касается планирования с кодом склада или без кода склада в строке требования, работа системы планирования упрощается при следующих условиях:  

-   в строках требования всегда имеются коды склада, а в системе полностью используются единицы хранения, включая соответствующую настройку склада.  
-   в строках требования всегда отсутствуют коды склада, а в системе не используются единицы хранения или какие-либо настройки складов (см. последний из сценариев, приведенных ниже).  

Но если строки требований то содержат коды склада, то нет, система планирования, в зависимости от настройки, будет следовать определенным правилам.  

## <a name="demand-at-location"></a>Спрос на складе  
Если система планирования обнаруживает спрос на складе (строку с кодом склада), дальнейшие действия определяются 3 важнейшими параметрами настройки.  

Во время исполнения планирования в системе поочередно проверяются 3 параметра настройки, и планирование проводится в соответствии с их значениями.  

1.  Установлен ли флажок **Склад обязателен**?  

    Если да, то:  

2.  Существует ли для товара единица хранения?  

    Если да, то:  

    Планирование товара производится в соответствии с параметрами планирования, указанными в карточке единицы хранения.  

    Если нет, то:  

3.  Содержится ли в поле **Компоненты по складам** код склада требования?  

    Если да, то:  

    Планирование товара производится в соответствии с параметрами планирования, указанными в карточке товара.  

    Если нет, то:  

    Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа =  *Партия-на-партию*, Вкл. товар =  *Да*, прочие параметры планирования = Пусто. (Товары, использующие политику повторного заказа  *Заказ*, продолжают использовать политику  *Заказ* так же, как и другие параметры.)  

> [!NOTE]  
>  Эта минимальная альтернатива касается только конкретного спроса. Все определенные параметры планирования игнорируются.  

См. варианты в сценариях, приведенные ниже.  

## <a name="demand-at-blank-location"></a>Спрос на складе "Пустой"  
Даже если установлен флажок **Код склада обязателен**, система допускает создание строк требования без кода склада — так называемый *ПУСТОЙ* склад. Это отклонение для системы, поскольку сюда включены значения различных параметров настройки, касающиеся складов (см. выше), и в результате модуль планирования не создаст строку планирования для такой строки спроса. Если флажок в поле **Склад обязателен** не установлен, а значения настройки склада существуют, то это также считается отклонением, и система планирования прореагируют, выдав "минимальную альтернативу":   
Планирование товара в этом случае производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ)*, Вкл. товар = *Да*, прочие параметры планирования = Пусто.  

См. варианты в сценариях настройки, приведенных ниже.  

### <a name="setup-1"></a>Настройка 1:  

-   Код склада обязателен = *Да*  
-   Настройка единицы хранения —  *КРАСНЫЙ*  
-   Компоненты по складам =  *СИНИЙ*  

#### <a name="case-11-demand-is-at--red-location"></a>Случай 1.1: спрос на складе *КРАСНЫЙ*  

Планирование товара производится в соответствии с параметрами планирования, указанными в карточке единицы хранения (включая возможное перемещение).  

#### <a name="case-12-demand-is-at--blue-location"></a>Случай 1.2: спрос на складе *СИНИЙ*  

Планирование товара производится в соответствии с параметрами планирования, указанными в карточке товара.  

#### <a name="case-13-demand-is-at--green-location"></a>Случай 1.3: спрос на складе  *ЗЕЛЕНЫЙ*  

Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ*), Вкл. товар = *Да*, все прочие параметры планирования = Пусто.  

#### <a name="case-14-demand-is-at--blank-location"></a>Случай 1.4: спрос на складе  *ПУСТОЙ*  

Планирование товара не производится, поскольку в строке требования не задан склад.  

### <a name="setup-2"></a>Настройка 2:  

-   Код склада обязателен = *Да*  
-   Единица хранения не существует  
-   Компоненты по складам =  *СИНИЙ*  

#### <a name="case-21-demand-is-at--red-location"></a>Случай 2.1: спрос на складе  *КРАСНЫЙ*  

Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ*), Вкл. товар = *Да*, все прочие параметры планирования = Пусто.  

#### <a name="case-22-demand-is-at--blue-location"></a>Случай 2.2: спрос на складе *СИНИЙ*  

Планирование товара производится в соответствии с параметрами планирования, указанными в карточке товара.  

### <a name="setup-3"></a>Настройка 3:  

-   Код склада обязателен = *Нет*  
-   Единица хранения не существует  
-   Компоненты по складам =  *СИНИЙ*  

#### <a name="case-31-demand-is-at--red-location"></a>Случай 3.1: спрос на складе  *КРАСНЫЙ*  

Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ*), Вкл. товар = *Да*, все прочие параметры планирования = Пусто.  

#### <a name="case-32-demand-is-at--blue-location"></a>Случай 3.2: спрос на складе *СИНИЙ*  

Планирование товара производится в соответствии с параметрами планирования, указанными в карточке товара.  

#### <a name="case-33-demand-is-at--blank-location"></a>Случай 3.3: спрос на складе  *ПУСТОЙ*  

Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ*), Вкл. товар = *Да*, все прочие параметры планирования = Пусто.  

### <a name="setup-4"></a>Настройка 4:  

-   Код склада обязателен = *Нет*  
-   Единица хранения не существует  
-   Компоненты по складам =  *ПУСТОЙ*  

#### <a name="case-41-demand-is-at--blue-location"></a>Случай 4.1: спрос на складе  *СИНИЙ*  

Планирование товара производится в соответствии со следующими параметрами: Политика повторного заказа = *Партия-на-партию* (политика *Заказ* остается равной *Заказ*), Вкл. товар = *Да*, все прочие параметры планирования = Пусто.  

#### <a name="case-42-demand-is-at--blank-location"></a>Случай 4.2: спрос на складе  *ПУСТОЙ*  

Планирование товара производится в соответствии с параметрами планирования, указанными в карточке товара.  

Как показывает последний сценарий, единственный способ получить правильный результат для строки требования без кода склада - это отключить все значения настройки, относящиеся к складам. Кроме того, единственным способом получить стабильные результаты планирования для требований на складе - является использование складских единиц учета.  

Следовательно, при частом проведении планирования с учетом требований на складах рекомендуется использовать функцию «Единицы хранения».  

## <a name="see-also"></a>См. также
[Планирование](production-planning.md)    
[Настройка производства](production-configure-production-processes.md)  
[Производство](production-manage-manufacturing.md)    
[Наличие](inventory-manage-inventory.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Сведения о проектировании: планирование поставок](design-details-supply-planning.md)   
[Рекомендации по настройке. Планирование поставок](setup-best-practices-supply-planning.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
