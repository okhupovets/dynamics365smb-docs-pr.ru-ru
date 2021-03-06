---
title: Поиск документов без вложений| Документация Майкрософт
Description: Вы можете осуществлять поиск операций главной книги для учтенных документов покупок и продаж, у которых нет входящих электронных документов, например для импортированных счетов.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e1b5c2b5e2615e5051a410c88b5e972036b0d98e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780564"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Поиск учтенных документов без записей входящих документов
На страницах **План счетов** и **Операции главной книги** с помощью функции поиска можно найти операции главной книги для учтенных документов покупки и продажи, которые не имеют записей входящих документов, и затем централизованно связать их с существующими записями или создать новые записи с прикрепленными файлами документов.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Поиск учтенных документов без записей входящих документов
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **План счетов**, затем выберите соответствующую ссылку.
2. Выберите строку счета ГК для тех операций главной книги, для которых вы ходите увидеть учтенные документы покупки и продажи без записей входящих документов, а затем выберите действие **Учтенные документы без входящего документа**.
3. Альтернативный вариант — выберите действие **Книга операций**.
4. На странице **Операции главной книги** выберите действие **Учтенные документы без входящих документов**.

Откроется страница **Учтенные документы без входящего документа**, содержащее сведения об учтенных документах покупки и продажи без записей входящего документа, представленных записями ГК в счете ГК, для которого открыто эту страницу. Страница может содержать до 1000 строк. Таким образом, по умолчанию поле **Фильтр по дате** содержит фильтр, который ограничивает строки записями, имеющими дату учета с начала отчетного периода до рабочей даты.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Подключение найденных документов к существующим записям входящих документов
1. На странице **Учтенные документы без входящего документа** выберите строку для учтенного документа, который нужно связать с существующей записью входящего документа, и выберите действие **Выбрать входящий документ**.
2. На странице **Входящие документы** выберите запись входящего документа, которую требуется связать с найденным учтенным документом, а затем нажмите кнопку **ОК**.
3. На странице **Учтенные документы без входящего документа** выбранная запись входящего документа будет связана с учтенным документом, как показано на информационной панели **Файлы входящих документов** .

Если нужная запись входящего документа отсутствует на странице **Входящие документы**, ее можно создать. Дополнительные сведения см. в разделе [Создание записей входящих документов](across-how-create-income-document-records.md).

## <a name="see-also"></a>См. также
[Обработка входящих документов](across-process-income-documents.md)  
[Входящие документы](across-income-documents.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
