---
title: Настройка табелей учета рабочего времени и их утверждение | Документация Майкрософт
description: Вы можете настроить табели учета рабочего времени для отслеживания затраченного времени и использования ресурсов в работах, что помогает при управлении проектами, комплектации штата и планировании производственной мощности.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1a5bb6f15f568c09aa2e897a7f986bfbcd63de56
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781814"
---
# <a name="set-up-time-sheets"></a>Настройка табелей учета рабочего времени
Табели учета рабочего времени в [!INCLUDE[d365fin](includes/d365fin_md.md)] регистрируются на еженедельной основе с периодичностью в семь дней. Их можно использовать для отслеживания времени, затраченного на работы, а также для записи простой регистрации затрат времени ресурса. Прежде чем использовать табели, необходимо указать, как они должны быть установлены и настроены.

После настройки того, как организация будет использовать табели учета времени, можно указать, требуется ли утверждение табелей и как будет производиться утверждение. В зависимости от потребностей организации, могут быть указаны:

* Один или несколько пользователей в качестве администратора и утверждающего табелей для всех табелей.
* Утверждающий табели для каждого ресурса.

После настройки табелей можно создавать табели для ресурсов, назначать им строки планирования работ и учитывать строки табелей. Дополнительные сведения см. в разделе [Использование табелей учета рабочего времени](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Настройка общей информации для табелей.
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка модуля "Ресурсы"**, затем выберите соответствующую ссылку.  
2. Заполните соответствующим образом поля. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Для поля **Табель учета рабочего времени по утверждению работы** выберите один из следующих вариантов.

| Параметр | Описание |
| --- | --- |
| **Никогда** |Пользователь в поле **Код пользователя, утверждающего табель** на карточке ресурса утверждает табель. |
| **Всегда** |Пользователь в поле **Ответственное лицо** на карточке работы утверждает табель. |
| **Только машина** |Если машинный табель связан с работой, то сотрудник, указанный в поле **Ответственное лицо** на карточке работы, утверждает этот табель. Если машинный табель связан с ресурсом, то сотрудник, указанный в поле **Код пользователя, утверждающего табель** на карточке ресурса, утверждает этот табель. |

## <a name="to-assign-a-time-sheet-administrator"></a>Назначение администратора табелей
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка пользователя**, затем выберите соответствующую ссылку.  
2. Добавьте нового пользователя, если список пользователей не включает лицо, которое вы хотите назначить администратором табелей. Дополнительные сведения см. в разделе [Назначение разрешений пользователям и группам](ui-define-granular-permissions.md).
3. Выберите пользователя, который будет администратором табеля, затем установите флажок **Админ. табеля учета рабочего времени**.  

> [!TIP]  
>   Рекомендуется назначать только одного пользователя в качестве администратора табелей в организации. В следующей процедуре настраиваются владелец табеля и утверждающий, где утверждающий табелей назначается для каждого ресурса.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Назначение владельца и утверждающего для табелей
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Ресурсы**, затем выберите соответствующую ссылку.
2. Выберите ресурс, для которого требуется настроить возможность использовать табели, затем установите флажок **Использовать табель**.  
3. В поле **Код пользователя владельца табеля** введите код владельца табеля. Держатель может ввести расход времени в табель и представить его для утверждения. В целом, когда ресурс — физическое лицо, это лицо также является владельцем.  
4. В поле **Код пользователя, утверждающего табель** введите код утверждающего табеля. Утверждающий может утвердить, отклонить или повторно открыть табель.  

> [!NOTE]  
>   Нельзя изменить код пользователя, утверждающего табели, если имеются табели, которые еще не были обработаны и имеют статус **Отправлено** или **Открыто**.

## <a name="see-also"></a>См. также
[Настройка управления проектами](projects-setup-projects.md)  
[Управление проектами](projects-manage-projects.md)  
[Финансы](finance.md)  
[Покупки](purchasing-manage-purchasing.md)         
[Продажи](sales-manage-sales.md)      
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
