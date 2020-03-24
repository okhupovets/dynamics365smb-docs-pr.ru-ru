---
title: Использование средства изменения ставки НДС | Microsoft Docs
description: Использование средства изменения ставки НДС
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992238"
---
# <a name="use-the-vat-rate-change-tool"></a>Использование средства изменения ставки НДС

## <a name="understanding-the-vat-rate-conversion-process"></a>Общее представление о процессе преобразования ставки НДС  
Средство измерения ставки НДС выполняет изменение ставок НДС по основным данным, журналам и заказам разными способами. Выбранные основные данные и журналы будут обновлены с помощью новой общей товарной учетной группы или товарной группы НДС. Если заказ полностью или частично отгружен, отгруженные товары будут содержать текущую общую товарную учетную группу или НДС товарной группы. Будет создана новая строка заказа для неотгруженных товаров и обновлена для согласования текущих и новых товарных групп или групп НДС. Кроме того, распределение товарных издержек, резервирования и информация о трассировке товара будут обновлены соответствующим образом.  

Однако есть несколько элементов, которые этот инструмент не преобразует:

* Заказы на продажи или на покупку и счета, для которых были учтены отгрузки. Эти документы учитываются с использованием текущей ставки НДС.  
* Документы, в которых учтены счета на предоплату. Например, вы отправили или получили предоплату по счетам, которые не были полностью завершены перед настройкой средства изменения ставки НДС. В этом случае будет разница между начисленным НДС и НДС, который был предварительно оплачен на момент завершения этого счета-фактура. Средство изменения ставки НДС пропустит эти документы, и вам потребуется выполнить обновление вручную.  
* Прямая поставка или специальные заказы.  
* Заказы на продажу или на покупку с интеграцией склада, если они были частично отгружены или получены.  
* Сервисные контракты.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Подготовка преобразований при изменении ставки НДС  
Перед настройкой средства изменения ставки НДС следует выполнить следующие подготовительные действия.

* Если имеются транзакции, которые используют различные ставки, то их необходимо разделить на две различные группы, создав новые счета Главной книги для каждой ставки, или с помощью фильтров к транзакциям групп в соответствии со ставкой.  
* При создании новых счетов Главной книги необходимо создать новые общие учетные группы.  
* Для уменьшения числа документов, которые преобразуются, учитывайте максимально возможное число документов и сократите число неучтенных документов до минимума.  
* Выполните резервное копирование данных.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Настройка средства изменения ставки НДС  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка изменения ставки НДС**, затем выберите соответствующую ссылку.  
2. На экспресс-вкладках **Мастер-данные**, **Журналы** и **Документы** выберите значение учетной группы из списка вариантов для требуемых вариантов полей. Для каждой группы вы можете выбрать, следует ли преобразовывать НДС товарные группы или общие товарные группы, иле же нужно преобразовывать оба значения, если они доступны в элементе основных данных. Для некоторых областей вы также можете установить фильтр для преобразования только подмножества значений, например счетов ГК. 

### <a name="to-set-up-product-posting-group-conversion"></a>Настройка преобразования групп учета товаров  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка изменения ставки НДС**, затем выберите соответствующую ссылку.  
2. На странице **Настройка изменения ставки НДС** выберите действие **Конвертация группы разноски прод. НДС** или **Конвертация общ. прод. группы разноски**.  
3. В поле **От кода** введите текущую группу учета.  
4. В поле **До кода** введите новую группу учета.  

### <a name="to-perform-vat-rate-change-conversion"></a>Выполнение преобразования изменения ставки НДС  
Средство изменения ставки НДС используется для управления изменениями стандартной ставки НДС. Вы выполняете преобразования НДС и общей учетной группы с целью изменения ставок НДС и поддержания точности отчетов по НДС. В зависимости от настройки вносятся следующие изменения:  

* Преобразование НДС учетных групп и общих учетных групп.  
* Изменения внедряются в счетах Главной книги, клиентах, поставщиках, открытых документах, строках журнала и т. п.  

> [!IMPORTANT]  
>  Перед проведением преобразования изменения ставки НДС можно выполнить тестирование преобразования. Для этого выполните приведенные ниже шаги, но обязательно снимите флажки **Выполнить преобразование** и **Средство изменения ставки НДС завершило работу**. В ходе тестового преобразования поле **Преобразовано** в таблице **Запись журнала изменения ставки НДС** очищается, а поле **Преобразованная дата** в таблице **Запись журнала изменения ставки НДС** остается пустым. После завершения преобразования выберите **Записи журнала изменения тарифа НДС**, чтобы просмотреть результаты тестового преобразования. Проверьте все операции перед начало преобразования. В частности, проверьте транзакций, которые используют старую ставку НДС.     

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Изменение ставки НДС**, затем выберите ссылку **Настройка изменения ставки НДС**.  
2. Удостоверьтесь, что вы уже настроили преобразование НДС товарной группы или общей товарной группы.  
3. Установите флажок **Выполнить преобразование**.  

    > [!IMPORTANT]  
    >  Снимите флажок **Средство изменения ставки НДС завершило работу**. Флажок устанавливается автоматически при завершении преобразования изменения ставки НДС.  

4. Выберите действие **Конвертировать**.  
5. После завершения преобразования выберите действие **Записи журнала изменения тарифа НДС**, чтобы просмотреть результаты тестового преобразования.  

> [!IMPORTANT]  
>  После преобразования выбирается поле **Преобразовано** в таблице **Запись журнала изменения ставки НДС**, а поле **Преобразованная дата** в таблице **Запись журнала изменения ставки НДС** отображает дату преобразования.  
## <a name="see-also"></a>См. также  
[Настройка налога на добавленную стоимость](finance-setup-vat.md)  
[Настройка нереализованного НДС](finance-setup-unrealized-vat.md)      
[Подача отчета об НДС в налоговый орган](finance-how-report-vat.md)  
[Работа с НДС по продажам и покупкам](finance-work-with-vat.md)  
[Локальная функциональность в Business Central](about-localization.md)