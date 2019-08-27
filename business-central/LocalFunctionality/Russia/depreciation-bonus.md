---
title: Амортизационная премия в России
description: Российские улучшения включают амортизацию.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 07/02/2019
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: d2425f2f1fb27a6d0d039012422da2bffbce76e8
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1738222"
---
# <a name="depreciation-bonus"></a>Амортизационная премия

Амортизационная премия представляет собой метод ускоренной амортизации, применяемый в налоговом учете в связи с положениями налогового законодательства России. Амортизационная премия позволяет включить затраты на основные средства и капиталовложения в текущий период по ставке, равной 10 или 30 процентам.

## <a name="depreciation-bonus-calculation"></a>Расчет амортизационной премии

Амортизационная премия может рассчитываться и применяться для следующих типов транзакций:

- Затраты на приобретение основных средств.
- Затраты на приобретение и повышение оценочной стоимости капиталовложений для всех предшествующих периодов, исключая текущий. 

Ставка амортизационной премии составляет 10 или 30 процентов в зависимости от класса основных средств. Ставка установлена для группы амортизации с помощью поля **Процент амортизационной премии** в окне **Группа амортизации**. 

После того как амортизационная премия рассчитана и учтена для периода, все транзакции очищаются для подготовки к следующему периоду.

## <a name="depreciation-bonus-settings"></a>Параметры амортизационной премии

Перед расчетом амортизационной премии необходимо убедиться в том, были применены соответствующие параметры в окне **Настройка налоговых регистров**. Используйте информацию в следующей таблице для применения параметров амортизационной премии.

| Поле                              | Описание                                                  |
| :--------------------------------- | :----------------------------------------------------------- |
| **Вкл. акт ввода в эксп. в расчет аморт. премии**   | Выберите, требуется ли использовать прием-передачу ОС для расчета базы амортизационной премии. |
| **Код нал. разн. по аморт. премии**            | Введите код налоговой разницы, который используется для вычисления амортизационной премии. Выбранный код налоговой разницы должен быть задан как амортизационная премия во время настройки налоговой разницы. |
| **Восстановление аморт. премии c**      | Введите начальную дату восстановления амортизации в случае продажи ОС. Если основное средство продано до этой даты и уже была применена амортизационная премия, амортизационная премия не будет восстанавливаться. |
| **Период восстановл. аморт. премии (лет)** | Введите период, в который производится восстановления амортизационной премии в случае продажи ОС. |
| **Код нал.разн. для восстановл. аморт.премии**   | Ведите код налоговой разницы, который используется для вычисления суммы восстановления амортизационной премии в налоговом учете. |

## <a name="selecting-and-canceling-depreciation-bonus-transactions"></a>Выбор и отмена транзакций амортизационной премии 

Транзакции амортизационной премии должны учитываться до расчета и учета суммы ежемесячной амортизации.

Для выбора транзакций амортизационной премии публикации для учета за период выберите **Аморт. премия** в окне **Журнал ОС** и окне **Журнал ГК основных средств**. 

Можно отменять транзакции амортизационной премии путем выполнения пакетного задания **Отменить операции книги ОС**. После учета отмены амортизационной премии все операции, включенные в базу амортизационной премии, необходимо вручную выбрать как базу амортизационной премии.

## <a name="see-also"></a>См. также

[Основные Средства](fixed-assets.md)