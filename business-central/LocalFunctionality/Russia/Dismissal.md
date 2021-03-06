---
title: Увольнение в России
description: Российские улучшения включают увольнение сотрудников.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: e17b607a7e7adb8b437f4433ed5917e1a9b34fed
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180996"
---
# <a name="dismissal"></a>Увольнение

Для уволенного создается дополнительная строка трудового договора, где **Тип операции** — *Увольнение*. 

Оформление приказа об увольнении осуществляется в следующей последовательности. 

1. Для бессрочных трудовых договоров заполните поле **Дата окончания** в заголовке трудового договора. Поле должно содержать дату увольнения сотрудника.
2. Создайте новую строку и укажите *Увольнение* в поле **Тип операции**.
3. Заполните поля договора:

| Поле              | Описание                                                  |
| ------------------ | ------------------------------------------------------------ |
| Причина увольнения   | Код причины увольнения                                    |
| Документ увольнения | В этом поле вы можете указать документ о причине увольнения, если это необходимо |

Если работнику при увольнении полагаются компенсационные выплаты, они должны быть указаны в условиях договора.

Код обязательной компенсационной выплаты также связан с причиной расторжения трудового договора.

4. Утвердите строку договора (Функция - **Утвердить строку**). 

5. Следующая последовательность действий будет выполнена во время утверждения строки трудового договора с типом "Увольнение". 

- Трудовому договору будет присвоен статус "Закрыт".
- Создает новую запись об увольнении в истории работника на предприятии. 

6. Карточка сотрудника содержит информацию об увольнении (в поле **Статус** установлено значение *Уволен*, заполнены поля **Дата увольнения** и **Код причины увольнения**).

## <a name="see-also"></a>См. также

[Персонал](Human-Resources.md)
