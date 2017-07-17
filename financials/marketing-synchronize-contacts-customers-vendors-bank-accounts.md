---
title: "Синхронизация контактов с клиентами, поставщиками и банковскими счетами | Документы Майкрософт"
description: "Описывается синхронизация контактов с клиентами, поставщиками и банковскими счетами в Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b28cd00659b077403e3174ac69c32ad5d9a8bf83
ms.contentlocale: ru-ru
ms.lasthandoff: 05/04/2017


---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Синхронизация контактов с клиентами, поставщиками и банковскими счетами
Если какие-то контакты являются еще и клиентами, поставщиками или банковскими счетами, можно синхронизировать контактную информацию с соответствующим клиентом, поставщиком или банковским счетом. Синхронизация делает общую информацию между контактами и клиентами, поставщиками или банковским счетом одинаковой.  

Прежде чем синхронизировать контакты с клиентами, поставщиками или банковскими счетами, следует указать код делового отношения для клиентов, поставщиков и банковских счетов в окне **Настройка модуля Маркетинг**. Дополнительные сведения см. в разделе [Настройка управления отношениями](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Различные способы синхронизации контактов с клиентами, поставщиками и банковскими счетами
Контакты можно синхронизировать с заказчиками, поставщиками или банковскими счетами тремя способами:

* Свяжите контакты с имеющимися клиентами, поставщиками или банковскими счетами. Дополнительные сведения см. в разделе [Практическое руководство. Связывание контактов с клиентами, поставщиками и банковскими счетами](marketing-how-link-contact.md).
* Создавайте клиентов, поставщиков или банковские счета из контакта. Дополнительные сведения см. в разделе [Создание клиента, поставщика или банковского счета из клиента](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Создать контакты из клиентов, поставщиков или банковских счетов. Дополнительные сведения см. в разделе [Создание контакта организации из клиента, поставщика или банковского счета](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Последствия синхронизации
Когда контакт синхронизирован с клиентом, поставщиком или банковским счетом:

* Необходимо обновить информацию только в одном месте. Например, если изменить номер телефона в контакте, те же изменения будут автоматически внесены в запись клиента, поставщика или банковского счета.
* Если была указана серия номеров для контактов, при создании карточки клиента, поставщика или банковского счета будет автоматически создана карточка контакта для клиента, поставщика или банковского счета.
* Непосредственно из контакта можно создавать предложения и заказы на продажу, а также предложения и заказы на покупку;
* Можно регистрировать взаимодействия при выполнении действий, таких как печать заказов и общих заказов, создание сервисных заказов на продажу, отправка сообщений электронной почты и т. д.
* При удалении контакта, связанного с клиентом, поставщиком или банковским счетом, удаляется только контакт. Клиент, поставщик или банковский счет остаются.
* При удалении клиента, поставщика или банковского счета, связанного с контактом, контакт сохраняется.

**Примечание**. Некоторые подробности, например сведения о счетах и учете, не отображаются в карточке контакта. Следовательно, может потребоваться добавить их вручную в карточку клиента, поставщика или банковского счета при создании контактов как клиентов, поставщиков или банковских счетов.

## <a name="see-also"></a>См. также
[Управление контактами](marketing-contacts.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
