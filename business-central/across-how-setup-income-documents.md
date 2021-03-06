---
title: Настройка входящих документов| Документация Майкрософт
description: Используйте функцию входящих документов для создания документов, управления задачами OCR, импорта счетов преобразования файлов изображений.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 08/10/2020
ms.author: edupont
ms.openlocfilehash: 1b0942c53f435a79cae733fe4d7287e628cf7478
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780514"
---
# <a name="set-up-incoming-documents"></a>Настройка входящих документов

При создании строк финансового журнала на основании записей входящих документов необходимо выбрать на странице **Настройка входящих документов** шаблон и раздел журнала.

Если пользователи не должны создавать счета или строки общего журнала по записям входящих документов до их утверждения, необходимо настроить утверждающих рабочего процесса.

Чтобы преобразовать PDF-файлы и файлы изображений в электронные документы, которые можно будет преобразовывать, например, счета покупки в [!INCLUDE[d365fin](includes/d365fin_md.md)], следует сначала настроить функцию OCR и включить этот сервис. Выберите пакет услуг, подходящий для вашей организации и/или страны/региона. Кроме того, вы можете создавать записи вручную для представления внешних документов.  

Если функция входящих документов настроена, можно использовать различные функции для просмотра квитанций по расходам, управления задачами OCR, а также преобразования входящих файлов документов, вручную и автоматически, в соответствующие документы либо строки журналов. Внешние файлы можно прикреплять на любом этапе обработки, в том числе к учтенным документам и к полученным записям поставщика, клиента и главной книги. Дополнительные сведения см. в разделе [Обработка входящих документов](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Настройка возможности входящих документов

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка входящих документов**, затем выберите соответствующую ссылку.
2. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

В рамках настройки вы должны решить, хотите ли вы требовать утверждения входящих документов. Чтобы требовать утверждения, вы должны настроить утверждающих и рабочие процессы утверждения. Если ваша организация не намерена требовать утверждения, вы можете пропустить следующий раздел.  

Наконец, если вы используете службу для преобразования файлов PDF или изображений, представляющих входящие документы, вы должны ее настроить. В противном случае вы также можете пропустить этот раздел.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Настройка утверждающих для записей входящих документов

При желании настройте процесс утверждения для входящих документов. Утверждающие входящих документов должны быть настроены в качестве пользователей рабочего процесса утверждения.

Прежде чем можно будет создавать рабочие процессы, которые включают шаги утверждения, необходимо настроить пользователей рабочих процессов, участвующих в процессах утверждения. На странице **Настройка пользователя для утверждений** также можно задавать лимиты по суммам для отдельных типов запросов и определять заместителей утверждающих лиц, которым делегируются запросы на утверждение в случае отсутствия исходного утверждающего лица. Дополнительные сведения см. в разделе [Настройка утверждающих пользователей](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Настройка службы распознавания

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка OCR**, затем выберите соответствующую ссылку.
2. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Ваши учетные данные автоматически шифруются.

Дополнительные сведения см. в разделе [Использование OCR для преобразования PDF-файлов и графических файлов в электронные документы](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>См. также

[Обработка входящих документов](across-process-income-documents.md)  
[Входящие документы](across-income-documents.md)  
[Покупки](purchasing-manage-purchasing.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
