---
title: "Управление отчетами по НДС для налоговых органов | Документы Майкрософт"
description: "Узнайте, как подготовить отчет по НДС с продаж за указанный период, и подать этот отчет в налоговый орган."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: ru-ru
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Практическое руководство. Подача отчета об НДС в налоговые органы
В отчете "Список продаж ЕС (Европейский Союз)" указываются суммы НДС (налог на добавленную стоимость), которые вы собрали за продажи внутри ЕС, чтобы вы могли предоставить эти суммы налоговому органу через его веб-службу.

> [!NOTE]  
>   В Великобритании все организации, которые продают каждый год больше определенной суммы клиентам в ЕС, должна подавать электронную версию списка продаж ЕС в формате XML через веб-сайт HMRC (Her Majesty's Revenue and Customs).

Список продаж ЕС применим только к странам-членам ЕС. Например, он не включает НДС по продажам в такие страны как Китай или США.

Для подачи отчетности по НДС в налоговый орган в электронном необходимо подключить [!INCLUDE[d365fin](includes/d365fin_md.md)] к веб-службе налогового органа. Для этого нужно настроить учетную запись в налоговом органе. После настройки этой учетной записи вы можете создать подключение к службе через [!INCLUDE[d365fin](includes/d365fin_md.md)]. Например, в Великобритании можно использовать службу **GovTalk**.

Отчет содержит одну строку для каждого типа транзакций с клиентом и отображает общую сумму для каждого типа транзакций. Есть три типа транзакции, которые могут входить в отчет:  
  
* Товары B2B  
* Услуги B2B  
* Товары B2B с триангуляцией  
  
Товары и услуги B2B определяет, что вы продали товар или услугу, и задаются параметром **Сервис ЕС** в настройке учета НДС. Товары B2B с триангуляцией показывают, что вы участвовали в торговле с посредником и задаются параметром **Торговля вне ЕС** в документах продажи, таких как заказы на продажу, счета, кредит-ноты и т. д.  
  
После отправки отчета [!INCLUDE[d365fin](includes/d365fin_md.md)] следит за службой и фиксирует ваши коммуникации. Поле **Состояние** указывается, на каком этапе находится обработка отчета. Например, после обработки отчета налоговыми органами состояние отчета изменяется на **Успешно**. Если налоговый орган нашел ошибку в отправленном отчете, отчет будет иметь состояние **Ошибка**. Ошибки можно просмотреть в разделе **Ошибки и предупреждения**, исправить их, а затем подать отчет заново. Чтобы просмотреть список всех отчетов "Список продаж ЕС", перейдите на страницу **Отчеты по списку продаж EC**.  
  
> [!NOTE]  
>   Если используется другой способ подачи отчета, например путем экспорта XML и его отправки на веб-сайт налогового органа, можно потом выбрать **Отметить как отправленное**, чтобы закрыть отчетный период. При отметке отчета как отправленного, он становится недоступным для редактирования. Если необходимо изменить отчет после его отметки как отправленного, его нужно повторно открыть. 
  
После проверки отчета в налоговом органе, они отправят сообщение электронной почты контактному лицу вашей компании. В [!INCLUDE[d365fin](includes/d365fin_md.md)] контактное лицо указывается на странице **Информация об организации**. Перед отправкой отчета убедитесь, что выбрано контактное лицо.

<!--> [!NOTE]  
>   Отчет "Список продаж ЕС" может содержать до 1000 строк. При строк больше, нужно отправить еще один отчет. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Подключение к веб-службе налогового органа
[!INCLUDE[d365fin](includes/d365fin_md.md)] предоставляет служебные подключения для связи с веб-сайтами налоговых органов. Например, если вы находитесь в Великобритании, вы должны включить служебное подключение **GovTalk**.  

1. В поле **Поиск страниц или отчетов** введите **Подключения к службе** и выберите соответствующую ссылку. <!-- remember to get the updated text for this-->  
2. Заполните обязательные поля.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Настройка отчета "Список продаж ЕС"
1. В поле **Поиск страниц или отчетов** введите **Настройка отчетов по НДС** и выберите соответствующую ссылку.  
2. Если требуется разрешить пользователям изменять и повторно отправлять этот отчет, установите флажок **Изменить отправленные отчеты**.  
3. Определение серию номеров для использования в отчетах "Список продаж ЕС".  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Подготовка и отправка отчета "Список продаж ЕС"
1. В поле **Поиск страниц или отчетов** введите **Список продаж ЕС** и выберите соответствующую ссылку.  
2. Выберите **Создать**, а затем заполните обязательные поля.  
3. Для генерации содержимого отчета выберите действие **Предложить строки**.  

    > [!NOTE]  
>   Перед отправкой отчета вы можете просмотреть транзакции, включенные в строку. Для этого выберите строку, а затем выберите действие **Показать операции НДС**.  
4. Для подготовки отчета к отправке выберите действие **Выпустить**.  
5. Для отправки отчета выберите действие **Отправить**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] проверяет, настроен ли отчет правильно. Если обнаружены ошибки, они будут показаны в разделе **Ошибки и предупреждения**, чтобы вы могли внести соответствующие изменения.

## <a name="viewing-communications-with-your-tax-authority"></a>Просмотр взаимодействий с налоговыми органами
В некоторых странах при отправке отчета вы обмениваетесь сообщениями с налоговыми органами. Вы можете просмотреть первое и последнее отправленное или полученное сообщение с помощью действий **Загрузить сообщение отправки** и **Загрузить сообщение отклика**.  

## <a name="configuring-your-own-vat-reports"></a>Настройка собственных отчетов об НДС
Вы можете использовать готовый отчет "Список продаж в ЕС" или создать собственные отчеты. При этом создается несколько модулей codeunit. Если требуется помощью, обратитесь к партнеру Майкрософт.  
    
В следующей таблице описываются модули codeunit, которые необходимо создать для отчета.

| Модуль Codeunit | Что должен делать |
|----|-----|
|Предложить строки| Получить сведения из таблицы операций НДС и показать их в строках отчета по НДС.|
|Содержимое | Контролировать формат отчета. Например, выбрать между JSON и XML. Используемый формат зависит от требований веб-службы налогового органа. |
|Отправка | Определяет как и когда подается отчет на основе требований налоговых органов. |
|Обработчик отклика | Обработка отклика от налогового органа. Например, он может отправить сообщение электронной контактному лицу в вашей организации. |
|Отмена | Отправить отмену отчета по НДС, который ранее был подан в налоговый орган. |

> [!NOTE]  
>   При создании модулей codeunit для отчета следует следить за значением поля **Версия отчета по НДС**. Это поле должно отражать версию отчета, которая требуется налоговыми органами. Например, в этом поле можно ввести **2017** для указания того, что отчет соответствует требованиям, действующим в этом году. Чтобы узнать текущую версию, обратитесь в свой налоговый орган.  

## <a name="see-also"></a>См. также
[Настройка НДС](finance-setup-vat.md)  
[Настройка продаж](sales-setup-sales.md)  
[Практическое руководство. Выставление счетов продажи](sales-setup-sales.md)  
