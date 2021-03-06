---
title: Как создавать сервисные предложения | Документация Майкрософт
description: Страницу **Сервисное предложение** можно использовать для создания документов, в которые вводится информация о сервисе, например ремонте и обслуживании, для сервисных товаров по запросу клиента. Можно использовать сервисное предложение как предварительный черновик сервисного заказа, а затем преобразовать предложение в сервисный заказ.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 26b250a6c902e70bd4badf712d620f835d4ebb5a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784438"
---
# <a name="create-service-quotes"></a>Создание сервисных предложений
Сервисные предложения можно рассматривать как основу для сервисных заказов. Фактически, они почти полностью идентичны. Они содержат такие сведения, как клиент, тип заказа, товар, который требует обслуживания, сведения для выставления счетов и отгрузки, а также информацию о фактической сервисной работе.
 
Можно использовать сервисное предложение как предварительный черновик сервисного заказа, а затем преобразовать предложение в сервисный заказ.  
  
## <a name="to-create-a-service-quote"></a>Создание сервисного предложения  
1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](media/ui-search/search_small.png "Что вы хотите сделать"), введите **Сервисные предложения**, затем выберите соответствующую ссылку.  
2. Создание нового сервисного предложения.  
3. В поле **Номер** введите номер сервисного предложения. Вместо этого, если на странице **Сервисный центр - настройка** настроены серии номеров сервисных предложений, можно нажать клавишу ВВОД, чтобы выбрать следующий доступный номер сервисного предложения.  
4. В поле **Номер клиента**  выберите соответствующего клиента из списка.  

  > [!Note]  
  >  Соответствующие поля для клиента заполняются автоматически данными из карточки **Клиент**. Если карточка **Клиент** не существует для клиента, но шаблон клиента настроен, можно создать клиента из сервисного предложения. Заполните соответствующие поля, затем выберите действие **Создать клиента**.  
  
5. В зависимости от настроек на экспресс-вкладке **Обязательные поля**, возможно, на странице **Сервисный центр - настройка** нужно будет заполнить поля **Тип сервисного заказа** и **Код менеджера**.  
6. Заполните строки сервисных товаров.  
7. Зарегистрируйте ожидаемые себестоимости в строках сервиса.  
  
## <a name="see-also"></a>См. также  
[Создание сервисных заказов](service-how-to-create-service-orders.md)  
[Работа с сервисными задачами](service-how-to-work-on-service-tasks.md)  

 