---
title: Настройка предпочтительных способов отправки документов продажи | Документация Майкрософт
description: Описывается порядок настройки предпочитаемого способа отправки документов продажи, например электронная почта, PDF, электронные документы и т. д.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 528ee49dda35055872c7ebe2d241456383028434
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780814"
---
# <a name="set-up-document-sending-profiles"></a>Настройка профилей отправки документов
Для каждого клиента можно настроить предпочтительный способ отправки документов продажи, так что не придется каждый раз выбирать вариант отправки при выборе действия **Учесть и отправить**.

На странице **Профили отправки документов** можно настроить различные профили отправки, которые затем можно будет выбирать в поле **Профиль отправки документов** в карточке клиента. Вы можете установить флажок **По умолчанию**, чтобы указать, что профиль отправки документа является профилем по умолчанию для всех клиентов, кроме тех, у которых в поле **Профиль отправки документов** указан иной профиль.

При выборе действия **Учесть и отправить** в документе продажи появляется диалоговое окно **Учесть и отправить подтверждение**, в котором отображается используемый профиль отправки — либо установленный для данного клиента, либо профиль по умолчанию для всех клиентов. В этом диалоговом окне можно изменить профиль отправки для конкретного документа продаж. Дополнительные сведения см. в разделе [Выставление счетов продажи](sales-how-invoice-sales.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a>Настройка профиля отправки документов
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Профили отправки документов**, затем выберите соответствующую ссылку.
2. На странице **Профили отправки документов** выберите действие **Создать**.
3. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Определение профиля отправки в карточке клиента
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Клиенты**, затем выберите соответствующую ссылку.
2. Откройте карточку клиента, для которого нужно настроить профиль отправки.
3. В поле **Профиль отправки документов** выберите профиль, настроенный, как описано в предыдущей процедуре.

## <a name="see-also"></a>См. также
[Настройка продаж](sales-setup-sales.md)  
[Продажи](sales-manage-sales.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
