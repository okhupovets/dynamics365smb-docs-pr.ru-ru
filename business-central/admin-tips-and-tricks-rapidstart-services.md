---
title: Советы и подсказки — RapidStart Services | Документация Майкрософт
description: При настройке организаций с помощью RapidStart Services можно воспользоваться некоторыми советами и подсказками для упрощения реализации.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: e1c3dfe37e6288934d05c4e2d9294cf87da49537
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786125"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Советы и подсказки: RapidStart Services

При настройке организаций с помощью RapidStart Services можно воспользоваться некоторыми советами и подсказками для упрощения реализации.  

## <a name="take-advantage-of-configuration-templates"></a>Воспользуйтесь шаблонами конфигураций

Шаблоны конфигураций помогают упростить процесс внедрения. Используя их, можно включить аналогичные клиентов в сегменты, а затем разработать протокол реализации, обрабатывающий всех клиентов в сегменте подобным образом. В этом способе можно применить уровень предварительных настроек к каждому сегменту и продолжить быстрое внедрение.  

## <a name="configuration-questionnaires"></a>Анкеты конфигурации

Чтобы упростить процесс заполнения анкеты конфигурации, определите значения по умолчанию в соответствии с оптимальными методами работы.  

## <a name="batch-creation-of-journal-lines"></a>Пакетное создание строк журнала

Рекомендуется использовать инструменты переноса данных, предоставленные для переноса записей журнала. В противном случае при использовании пакетного задания для создания строки журнала, он имеет ограниченный объем и генерирует предварительно созданные по умолчанию поля в журнале. Остальные поля журнала необходимо затем заполнить вручную.  

## <a name="migrating-transactions"></a>Перенос транзакций

Рекомендуется переносить начальные сальдо в указанном ниже порядке. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Выполните миграцию начальных сальдо без использования вложенных книг счетов Главной книги. Используйте определенные корреспондирующие счета с начальным сальдо для каждой книги. Настройте корреспондирующие счета, чтобы включить непосредственный учет.  
2. Перенесите открытые операции книги клиентов.  <!--work on these-->
3. Перенесите открытые операции книги, связанные товарами.  
4. Выполните миграцию открытых операций основных средств.  

## <a name="make-each-package-manageable"></a>Сделайте каждый пакет управляемым

Когда вы используете пакеты конфигурации для переноса данных, разделяйте данные на отдельные пакеты для упрощения переноса. Например, если вы хотите перенести записи книги за 20 лет, импорт может занять много часов и дней. Вместо этого разделите данные на части, чтобы каждый пакет стал более управляемым. В настоящее время нет твердых правил относительно того, что делает пакет эффективным, но если вы видите проблемы с импортом или экспортом пакета, попробуйте уменьшить его и посмотрите, поможет ли это.  

## <a name="see-also"></a>См. также

[Настройка организации со службами RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Администрация](admin-setup-and-administration.md)  
