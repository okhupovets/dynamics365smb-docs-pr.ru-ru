---
title: Работа с финансовыми отчетами в России
description: Российские улучшения включают дополнительные функции, связанные с финансовыми отчетами.
author: DianaMalina
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.reviewer: edupont
ms.author: soalex
ms.openlocfilehash: cf3bfab65c82190b1ddd56d9c9c0d93c6f2ed846
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180992"
---
# <a name="work-with-account-schedules"></a>Работа с финансовыми отчетами

Используйте финансовые отчеты для получения сведений о финансовых данных, сохраненных в плане счетов. Финансовые отчеты анализируют цифры на счетах главной книги и сравнивают операции главной книги с операциями бюджета главной книги. Результаты отображаются на диаграммах на домашней странице, например на диаграмме "Движение денежных средств". 

[!INCLUDE[prodshort](../../includes/prodshort.md)] обеспечивает несколько примеров финансовых отчетов, которые можно использовать сразу же, либо можно настроить собственные строки и столбцы для указания цифр для сравнения. Например, вы можете создавать финансовые отчеты для вычисления размеров прибыли по таким измерениям, как подразделения или группы клиентов. Можно создать столько пользовательских финансовых отчетов, сколько нужно.

Настройка финансовых отчетов требует понимания финансовых данных в плане счетов. Например, можно рассматривать операции главной книги как процент от бюджетных операций. Для этого необходимо создать бюджеты. Дополнительные сведения см. в разделе [Создание бюджетов](../../finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Категории счетов и финансовые отчеты

Дл изменения макетов финансовых отчетов можно использовать категории счетов. После настройки категорий счетов в окне **Категории счетов ГК** и выбора действия **Создать финансовые отчеты** соответствующие финансовые отчеты для основных финансовых отчетов будут обновлены. При следующем выполнении одного из этих отчетов, например балансового отчета, будут добавлены новые итоговые значения и вложенные операции на основании внесенных изменений. 

## <a name="to-create-new-account-schedules"></a>Создание новых финансовых отчетов

Использование финансовых отчетов для анализа числовых значений на счетах главной книги или для сравнения операций главной книги с операциями бюджета главной книги. Например, можно рассматривать операции ГК как процент от бюджетных операций. 

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите соответствующую ссылку.

2. В окне **Названия финансовых отчетов** выберите действие **Создать**, чтобы создать новое название финансового отчета.

3. Заполните соответствующим образом поля. Выберите поле для чтения краткого описания поля или ссылки на дополнительную информацию.

4. Выберите действие **Изменение финансового отчета**.

5. В окне **Финансовый отчет** заполните все поля соответствующим образом.

   После создания нового финансового отчета и настройки строк следует настроить столбцы. Настройку можно производить либо вручную, либо предварительно задать для финансового отчета раскладку столбцов.

6. Выберите действие **Изменить настройку макета столбца**.

7. В окне **Раскладка столбцов** заполните требуемые поля.

> [!NOTE]
> Если финансовому отчету не назначена используемая по умолчанию раскладка столбцов, необходимо настроить столбцы вручную.

### <a name="to-create-a-column-that-calculates-percentages"></a>Создание столбца для вычисления процентов

Иногда может возникать потребность включить столбец в финансовый отчет для расчета процентов по итоговой сумме. Например, если имеется несколько строк, разбивающих продажи по измерениям, может потребоваться столбец с указанием процента от общих продаж для каждой строки. 

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите соответствующую ссылку.
2. В окне **Названия финансовых отчетов** выберите финансовый отчет.
3. Выберите действие **Изменение финансового отчета**, чтобы настроить строку финансового отчета для вычисления общей суммы, на которой будет основан процент.
4. Вставьте строку непосредственно перед первой строкой, для которой необходимо отобразить проценты.
5. Заполните поля в строке следующим образом: В поле **Тип группировки** укажите **Задать базу для процентов**. В поле **Подсчет итога** введите формулу для итога, на которой будет основан расчет процента. Например, если строка 11 показывает итоговые продажи, введите **11**.
6. Выберите действие **Изменить настройку макета столбца**.
7. Заполните поля в строке следующим образом: В поле **Тип столбца** выберите **Формула**. В поле **Формула** введите формулу для суммы, для которой необходимо вычислить процент, добавив в конце символ %. Например, если столбец с номером N содержит чистое изменение, то введите **N%**.
8. Повторите шаги с 4 по 7 для каждой группы строк, по которым требуется получить процент.

## <a name="to-set-up-account-schedules-with-overviews"></a>Настройка финансовых отчетов с обзорами

Финансовый отчет можно использовать для создания отчета, содержащего сравнение цифр главной книги с цифрами бюджета главной книги. 

1. Выберите значок ![Лампочка, которая открывает функцию "Что вы хотите сделать"](../../media/ui-search/search_small.png "Что вы хотите сделать"), введите **Финансовые отчеты**, затем выберите соответствующую ссылку.

2. В окне **Названия финансовых отчетов** выберите финансовый отчет.

3. Выберите действие **Изменение финансового отчета**.

4. В окне **Финансовый отчет** в поле **Имя** выберите название финансового отчета по умолчанию.

5. Выберите действие **Вставить счета**.

6. Выделите счета, по которым необходимо составить отчет, затем нажмите кнопку **ОК**.

   Теперь счета вставлены в финансовый отчет. При желании можно изменить также раскладку столбцов.

7. Выберите действие **Обзор**.

8. На экспресс-вкладке **Фильтры измерения** задайте фильтр по бюджету с требуемым названием фильтра.

9. Нажмите кнопку **ОК**.

Теперь можно копировать и вставлять бюджетные отчеты в таблицу.

## <a name="see-also"></a>См. также

[Финансы](../../finance.md)  
[Настройка финансов](../../finance-setup-finance.md)  
[Главная книга и план счетов](../../finance-general-ledger.md)  
