---
title: Как учесть несколько документов одновременно | Документация Майкрософт
description: Вместо того чтобы учитывать отдельные документы по одному, вы можете выбрать несколько неучтенных документов в списке для пакетного учета, — либо немедленного, либо запланированного (например, в конце дня).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782522"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Одновременный учет нескольких документов

Вместо того чтобы учитывать отдельные документы по одному, вы можете выбрать несколько неучтенных документов в списке для немедленного учета или для пакетного учета по расписанию (например, в конце дня). Это имеет смысл делать, если только контролер может учитывать документы, созданные другими пользователями, или во избежание проблем с быстродействием системы из-за учета документов в рабочие часы.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Немедленный одновременный учет нескольких заказов на покупку

В следующей процедуре рассматривается, как немедленно учесть несколько заказов на покупку. Действия для всех остальных документов продажи и покупки аналогичны.

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на покупку**, затем выберите соответствующую ссылку.
2. На странице **Заказы** выберите все заказы для учета:
3. В поле **Номер** выберите три вертикальные точки, чтобы открыть контекстное меню, а затем выберите действие **Выбрать больше**.
4. Установите флажки для всех строк, представляющих заказы, которые вы хотите одновременно учесть.
5. Выберите действие **Учет**, а затем выберите действие **Учет**.
6. Нажмите кнопку **Да** в сообщении подтверждения.

## <a name="to-batch-post-multiple-purchase-orders"></a>Пакетный учет нескольких заказов на покупку

В следующей процедуре рассматривается пакетный учет заказов на покупку. Действия для всех остальных документов покупки и продажи, где доступно действие **Пакетный учет**, аналогичны.

> [!NOTE]
> Пакетный учет документов происходит в фоновом режиме. [!INCLUDE [prodshort](includes/prodshort.md)] Online включает задания по умолчанию для фонового учета и пакетного учета. Дополнительные сведения см. в разделе [Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md).

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Заказы на покупку**, затем выберите соответствующую ссылку.  
2. На странице **Заказы** выберите все заказы для учета:
3. В поле **Номер** выберите три вертикальные точки, чтобы открыть контекстное меню, а затем выберите действие **Выбрать больше**.
4. Установите флажки для всех строк, представляющих заказы, которые вы хотите одновременно учесть.
5. Выберите действие **Учет**, а затем выберите действие **Пакетный учет**.
6. На странице **Пакет. учет заказов на покупку** заполните поля требуемым образом. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Нажмите кнопку **ОК**.
8. Для просмотра потенциальных проблем, возникших во время пакетного учета документов, откройте страницу **Регистр сообщений об ошибках**.

Заказы на покупку теперь будут добавлены в отдельную операцию очереди работ, которая определяет, когда будут учтены документы. Дополнительные сведения см. в разделе [Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md).

Если вы выберете **PDF** в поле **Тип вывода отчета**, успешно учтенные заказы на покупку будут доступны в части **Входящие отчеты** вашего ролевого центра.

## <a name="see-also"></a>См. также

[Учет документов и журналов](ui-post-documents-journals.md)  
[Использование очередей работ для планирования задач](admin-job-queues-schedule-tasks.md)  
[Изменение учтенных документов](across-edit-posted-document.md)  
[Исправление или отмена неоплаченных счетов покупки](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Поиск страниц и информации с помощью функции "Что вы хотите сделать"](ui-search.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
