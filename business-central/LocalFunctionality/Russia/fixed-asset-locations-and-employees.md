---
title: 'ОС: местоположения и ответственные сотрудники в России'
description: Российские улучшения включают местоположения и ответственных сотрудников для основных средств.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: 99c9eb7e4f4b6028f934b978999e59a48dadfeeb
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738267"
---
# <a name="fixed-asset-locations-and-employees"></a>ОС: местоположения и ответственные сотрудники

Функция местоположений и ответственных сотрудников для основных средств позволяет: 

- управлять движением основных средств и хранить историю перемещений ОС между различными местоположениями и подотчетными лицами;
- указывать местоположение и подотчетное лицо для ОС в документах и журналах для учета основных средств. Эти данные будут отражены в операциях основных средств;
- создавать отчеты и расчеты, в которых используется история перемещений основных средств. Кроме того, можно связать сотрудников (по умолчанию), местоположения (склад товара) и регионы в официальной классификации (код ОКАТО) с любым местоположением основных средств.

 

## <a name="setup"></a>Настройка 

Ниже показано, как обеспечить, чтобы поля **Код местонахождения ОС** и **Код сотрудника** были всегда заполнены для основных средств. 

1. Выберите значок ![Лампочка, которая открывает функцию Что вы хотите сделать](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Настройка ОС*, затем выберите связанную ссылку.
2. На экспресс-вкладке **Общие** установите флажок **Местонахождение ОС обязательно**.

 

> :speech_balloon: **Примечание**
>
> Если этот флажок установлен, процедуры учета основных средств управляются, пока они генерируют операции ОС с ненулевым значением в поле **Кол-во**.



1. Установите флажок **Код сотрудника обязателен**.

 

> :speech_balloon: **Примечание**
>
> Если этот флажок установлен, процедуры учета основных средств управляются, пока они генерируют операции ОС с ненулевым значением в поле **Кол-во**.

 

## <a name="added-fields"></a>Добавленные поля 

Поля со ссылками на местоположения и подотчетных лиц для ОС были добавлены к следующим элементам: 

- строки документов покупки;
- журналы основных средств;
- финансовые журналы основных средств;
- журналы реклассификации основных средств;
- акты основных средств. 

Если установлен флажок **Код сотрудника обязателен** или **Местонахождение ОС обязательно** в окне **Настройка основных средств**, поля со ссылками на соответствующие таблицы должны быть заполнены для операций с основными средствами. Вы вводите значение в поле **Код местоположения ОС** в строке, затем поля **Код сотрудника** и **Код склада** (если оно существует в строке) заполняются соответствующими значениями по умолчанию из таблицы местоположения основных средств. Затем значения этих полей можно изменить вручную.

При учете документов и журналов значения в этих полях переносятся в соответствующие новые операции ОС и в соответствующие поля в карточках основных средств.

 

## <a name="see-also"></a>См. также 

[Инвентаризация основных средств](Fixed-Asset-Inventory.md)