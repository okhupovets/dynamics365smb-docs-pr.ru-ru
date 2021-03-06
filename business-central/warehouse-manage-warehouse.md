---
title: Складские операции | Документация Майкрософт
description: После получения товаров и перед их отгрузкой выполняется ряд внутренних складских действий, чтобы обеспечить эффективный поток через склад, а также упорядочить и обработать складские запасы организации.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 3d9f409fbcf8a9c6f7984feb3ad39a0107d89c34
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785000"
---
# <a name="warehouse-management"></a>Управление складом
После получения товаров и перед их отгрузкой выполняется ряд внутренних складских действий, чтобы обеспечить эффективный поток через склад, а также упорядочить и обработать складские запасы организации.

Типичные складские действия включают размещение товаров, перемещение товаров в пределах склада и между складами, а также подбор товаров для сборки, производства или отгрузки. Сборка товаров для продажи или в запасы также может рассматриваться как складские операции, но здесь они не рассматриваются. Дополнительные сведения см. в разделе [Управление сборкой](assembly-assemble-items.md).  

На крупных складах эти различные задачи обработки могут распределяться по отделам, а управление их интеграцией осуществляется с помощью расширенного рабочего процесса. В более простых структурах процесс менее формализован, а складские операции выполняются с использованием т. н. операций размещения запасов и подбора запасов. Дополнительные сведения о сравнении базовых и расширенных конфигурациях складов см. в разделах [Сведения о проектировании: обзор склада](design-details-warehouse-overview.md).

Прежде чем можно будет осуществлять складские операции, необходимо настроить систему для соответствующей сложности складской обработки. Дополнительные сведения см. в разделе [Настройка управления складом](warehouse-setup-warehouse.md).

Связанные с запасами задачи инвентаризации, корректировки и реклассификации товаров могут включать такие задачи склада, которые должны выполняться в складских операциях, прежде чем их можно будет синхронизировать их с соответствующими операциями книги товаров. Дополнительные сведения см. в разделе [Подсчет, корректировка и повторная классификация запасов](inventory-how-count-adjust-reclassify.md).

 В следующей таблице приводится последовательность задач со ссылками на разделы, в которых они описываются.   

|**Задача**|**Раздел**|  
|------------|-------------|  
|Регистрация приемки (включая переприход) товаров на складе, либо только с заказом на покупку, при простых настройках склада, либо со складской приходной накладной, в случае полуавтоматической или полностью автоматической обработки на складе.|[Приемка товаров](warehouse-how-receive-items.md)|
|Обход процессов размещения и подборки, чтобы ускорить передачу товара прямо с приемки или производства на отгрузку.|[Переброска товаров](warehouse-how-to-cross-dock-items.md)|    
|Разместить товары, полученные в результате покупок, возвратов продаж, перемещений или выхода продукции в соответствии с настроенным процессом склада.|[Размещение товаров](warehouse-put-away-items.md)|
|Перемещение товаров между ячейками на складе.|[Перемещение товаров](warehouse-move-items.md)|
|Выполнить подбор товаров для отгрузки, перемещения или потребления при сборке или производстве в соответствии с настроенным процессом склада.|[Подбор товаров](warehouse-pick-items.md)|
|Регистрация отгрузки товаров со склада, либо только с заказом на продажу, при простых настройках склада, либо со складской расходной накладной, в случае полуавтоматических или полностью автоматических складских процессов на складе.|[Отгрузка товаров](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>См. также  
[Наличие](inventory-manage-inventory.md)  
[Настройка управления складом](warehouse-setup-warehouse.md)     
[Управление сборкой](assembly-assemble-items.md)    
[Сведения о проектировании: управление складом](design-details-warehouse-management.md)  
[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
