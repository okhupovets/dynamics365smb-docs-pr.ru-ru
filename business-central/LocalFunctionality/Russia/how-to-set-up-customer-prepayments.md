---
title: Настройка предоплат клиентов в России
description: Российские улучшения включают предоплату клиентов.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 3c34709ee9a40b291245b7c1d8c1d88dbbe4a5ee
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738249"
---
# <a name="how-to-set-up-customer-prepayments"></a>Практическое руководство. Настройка предоплат клиентов

Предоплаты — это авансовые платежи по заказам на продажу, которые получены, для которых создан счет и которые учтены, но до окончательного выставления счетов. Например, вам может потребоваться задаток, чтобы произвести товар и отгрузить его клиенту. Предоплаты позволяют создавать счета и собирать авансовые платежи от клиентов и учитывать платежи для правильных счетов.

## <a name="to-set-up-customer-prepayments"></a>Настройка предоплат клиентов

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка модуля "Продажи"**, затем выберите связанную ссылку.

2. На экспресс-вкладке **Нумерация** убедитесь, что серия номеров **Серия номеров учт. счетов предопл.** совпадает с **Серия номеров учт. счетов**. Убедитесь также, что серия номеров для **Серия номеров учт. кр.-нот предопл.** совпадает с серией для **Серия номеров учт. кредит-нот**.

3. На экспресс-вкладке **Предоплата** введите следующие сведения.

   | Поле                             | Описание                                                  |
   | :-------------------------------- | :----------------------------------------------------------- |
   | **Использовать счет ГК предоплаты**        | Выберите это поле, чтобы учесть предоплаты поставщикам, используя субсчет, указанный в поле **Счет предоплаты** в окне **Учетные группы клиента**. |
   | **Создание счета на предоплату**     | Выберите, чтобы создать счет на предоплату. Если это поле не выбрано, счет на предоплату создан не будет. |
   | **Серия номеров учт. предоплат**        | Введите код серии номеров, который требуется использовать для счетов на предоплату. |
   | **Учт. разн. по предопл. - серия ном. док.**           | Введите код серии номеров, который требуется использовать для документов предоплаты. |
   | **Разн. по предопл. - тип серии номеров док.**             | Укажите, требуется ли использовать серию номеров или символ для идентификации документов предоплаты. |
   | **Символ для док. разн. по предопл.**            | Введите символ, который будет печататься на документах предоплаты.        |
   | **Разн. по предопл.: прибыль - знач. изм. условия**  | Введите код для измерения, которое используется для создания условной прибыли от предоплаты. |
   | **Разн. по предопл.: убытки - знач. изм. условия** | Введите код для измерения, которое используется для создания условного убытка от предоплаты. |
   | **Разн. по предопл.: прибыль - знач. изм. вида**       | Введите код для измерения, которое используется для создания платежа с точки зрения прибыли от предоплаты. |
   | **Разн. по предопл.: убытки - знач. изм. вида**      | Введите код для измерения, которое используется для создания платежа с точки зрения прибыли от предоплаты. |

4. Откройте окно **Учетные группы клиента**.

5. В поле **Счет предоплаты** укажите счет главной книги, который должен использоваться для учета предоплаты клиентов.

6. Нажмите кнопку **Закрыть**, чтобы закрыть окно и сохранить введенные данные.

Теперь вы можете создавать счета и собирать авансовые платежи от клиентов и учитывать платежи для правильных счетов.

## <a name="see-also"></a>См. также

[Выставление счетов на предоплату](../../finance-invoice-prepayments.md)  
[Пошаговое руководство. Настройка и выставление счетов на продажу](../../walkthrough-setting-up-and-invoicing-sales-prepayments.md)  