---
title: Как планировать складские перемещения в журналах | Документация Майкрософт
description: Перемещения планируются в журнале с использованием функции пополнения ячейки или путем планирования строк, необходимых для создания инструкций по передвижению, вручную.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8c751d6925af74e7e4c1a0e37f6d22ea9144adff
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779390"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Планирование складских перемещений в журналах
Перемещения планируются в журнале с использованием функции пополнения ячейки или путем планирования строк, необходимых для создания инструкций по передвижению, вручную.  

## <a name="to-calculate-a-replenishment-movement"></a>Расчет передвижения для пополнения  
По мере того, как склад отгружает товары клиентам, в ячейках с наибольшим рейтингом остается меньше и меньше товаров. Для того чтобы заполнить эти ячейки с высоким рейтингом товарами из других ячеек, используется функция **Расчет пополнения ячеек** на странице **Журнал перемещения**

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал перемещения**, затем выберите соответствующую ссылку.  
2.  Выберите действие **Расчет пополнения ячеек**.  

    В [!INCLUDE[d365fin](includes/d365fin_md.md)] создаются строки, которые точно указывают, каким образом товары из ячеек с более низким рейтингом перемещаются в ячейки с более высоким рейтингом.  

    > [!NOTE]  
    >  Предлагается перемещение согласно методу FEFO при активации функции **Создать передвижение**, если для товара удовлетворяются следующие условия:  
    >   
    >  -   Указан срок годности товара.  
    > -   Установлен флажок **Выбрать по методу FEFO** в карточке склада.  
    > -   Установлен флажок **Ячейка обязательна** в карточке склада.  
    > -   Поля **Из зоны** и **Из ячейки** пусты.  

    Дополнительные сведения см. в разделе [Подбор по методу FEFO](warehouse-picking-by-fefo.md).  

3.  Просмотрите строки и, при необходимости, выберите их или удалите некоторые из них, если нет времени обработать их все.  
4.  Выберите действие **Создать передвижение**, чтобы создать складскую инструкцию для работников склада.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Перемещение всего содержимого одной или нескольких ячеек с помощью функции "Получить содержимое ячейки"  
Журнал перемещений используется также для планирования других перемещений товаров внутри склада. Например, если товар нужно поместить в ячейку для контроля качества, то для планирования этого действия можно воспользоваться журналом передвижений, а затем создать передвижение, чтобы сформировать инструкции для сотрудника.  

1.  Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Журнал перемещения**, затем выберите соответствующую ссылку.  
2.  Выберите действие **Получить содержимое ячейки**. С помощью страницы запроса можно отфильтровать те ячейки и товары, которые должны быть отображены в строках журнала перемещений.  
3.  Заполните соответствующие поля на странице запроса пакетного задания. Например, если требуется просмотреть содержимое всех ячеек определенной складской зоны, заполните поле **Код зоны**. Если требуется получить строки для всех ячеек, содержащих определенный товар, заполните поле **Код товара**.  

    > [!NOTE]  
    >  Невозможно переместить вручную товары в ячейку или из нее, если у этой ячейки тип ПОЛУЧЕНИЕ, поскольку товары, находящиеся в ячейке с этим типом, должны быть зарегистрированы как размещенные до того, как станут частью доступных складских запасов.  

4.  Если получено много строк, выберите **Сортировка**, чтобы определить способ сортировки для упорядочивания строк, отображаемых в журнале, а затем нажмите **ОК**.  

    > [!NOTE]  
    >  Строки перемещения извлекаются согласно методу FEFO при активации функции **Получить содержимое ячейки**, если для товара выполняются следующие условия:  
    >   
    >  -   Указан срок годности товара.  
    > -   Установлен флажок **Выбрать по методу FEFO** в карточке склада.  
    > -   Установлен флажок **Ячейка обязательна** в карточке склада.  
    > -   Поля **Из зоны** и **Из ячейки** пусты.  

5.  Чтобы отразить изменения, которые предполагается сделать, внесите недостающую информацию в некоторые из полученных строк. Для каждого перемещаемого товара необходимо заполнить поля **Номер товара**, **Из кода ячейки**, **В код ячейки** и **Кол-во**.  
6.  Удалите незаполненные строки, которые служили для информационных целей.  
7.  Когда в строках журнала будут точно отражено, каким образом работник склада должен выполнять перемещение, выберите действие **Создать передвижение**, чтобы создать инструкции для сотрудника.  

## <a name="see-also"></a>См. также  
[Управление складом](warehouse-manage-warehouse.md)  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
