---
title: "Настройка конвертации банковских данных| Microsoft Docs"
description: "Вы можете настроить банковские счета для отслеживания транзакций и импорта или экспорта банковских выписок, таких как Yodlee."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 98d7215b4d8ae476fbc550ea0057e6f71a00a5fd
ms.contentlocale: ru-ru
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a><span data-ttu-id="a20f0-103">Настройка службы конвертации банковских данных</span><span class="sxs-lookup"><span data-stu-id="a20f0-103">Set Up the Bank Data Conversion Service</span></span>
<span data-ttu-id="a20f0-104">Глобальный поставщик услуг преобразования платежной информации в любой формат данных, требуемый банком, подключен и готов к включению в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a20f0-104">A global provider of services to convert payment information to any data format that your bank requires is connected and ready to be enabled in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a20f0-105">В [!INCLUDE[d365fin](includes/d365fin_md.md)] он называется службой конвертации банковских данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-105">This is referred to in [!INCLUDE[d365fin](includes/d365fin_md.md)] as the bank data conversion service.</span></span>

<span data-ttu-id="a20f0-106">Вы можете экспортировать строки платежей из окна **Журнал платежей** в файл или поток данных, который затем можно передать в банк для автоматической обработки, чтобы не проводить электронные платежи по одному.</span><span class="sxs-lookup"><span data-stu-id="a20f0-106">You can export payment lines from the **Payment Journal** window to a file or a data stream that you then upload to your bank for automatic processing so that you do not have to make electronic payments individually.</span></span> <span data-ttu-id="a20f0-107">Дополнительные сведения см. в разделе [Экспорт платежей в банковский файл](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="a20f0-107">For more information, see [Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

<span data-ttu-id="a20f0-108">Можно импортировать файлы банковской выписки в окно **Журнал выверки платежей** с помощью службы конвертации банковских данных для конвертации файла, полученного от банка, в поток данных, который может импортировать [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a20f0-108">You can import bank statement files into the **Payment Reconciliation Journal** window by using the bank data conversion service to convert a file that you receive from your bank to a data stream that [!INCLUDE[d365fin](includes/d365fin_md.md)] can import.</span></span> <span data-ttu-id="a20f0-109">Дополнительные сведения см. в разделе [Автоматическое применение платежей и выверка банковских счетов](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="a20f0-109">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="a20f0-110">В качестве альтернативы импорту банковских выписок с помощью службы конвертации банковских данных можно использовать службу банковских выписок Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="a20f0-110">As an alternative to importing bank statements with the bank data conversion service, you can use the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="a20f0-111">Дополнительные сведения см. в разделе [Настройка службы банковских выписок Envestnet Yodlee](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="a20f0-111">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

<span data-ttu-id="a20f0-112">Для импорта или экспорта банковских файлов следует настроить собственный банковский счет и банковские счета поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a20f0-112">To import or export bank files, you must set up your own bank account and your vendors' bank accounts.</span></span> <span data-ttu-id="a20f0-113">Дополнительные сведения см. в разделе [Настройка банковских счетов](bank-how-setup-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="a20f0-113">For more information, see [Set Up Bank Accounts](bank-how-setup-bank-accounts.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="a20f0-114">Служба конвертации банковских данных может налагать ограничение на число строк, экспортируемых в одном файле.</span><span class="sxs-lookup"><span data-stu-id="a20f0-114">The bank data conversion service may impose a limit on the number of lines that can be exported in one file.</span></span> <span data-ttu-id="a20f0-115">Если превысить это ограничение, будет выдано сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a20f0-115">You will receive an error message if the limit is exceeded.</span></span> <span data-ttu-id="a20f0-116">Рекомендуется, чтобы файлы банковских выписок не превышали 1000 строк, поскольку время обработки в службе конвертации банковских данных может значительно увеличиться.</span><span class="sxs-lookup"><span data-stu-id="a20f0-116">It is recommended that bank statement files do not exceed 1000 lines as the processing time in the bank data conversion service may otherwise increase significantly.</span></span>

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a><span data-ttu-id="a20f0-117">Регистрация компании на получение услуг преобразования банковских данных</span><span class="sxs-lookup"><span data-stu-id="a20f0-117">To sign your company up for the bank data conversion service</span></span>
1. <span data-ttu-id="a20f0-118">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка службы преобр. банковских данных**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="a20f0-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Data Conv. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a20f0-119">Откроется окно **Настройка службы преобр. банковских данных** с тремя полями, предварительно заполненными соответствующими URL-адресами поставщика службы преобразования банковских данных .</span><span class="sxs-lookup"><span data-stu-id="a20f0-119">The **Bank Data Conv. Service Setup** window opens with three fields prefilled with relevant URLs of the provider of bank data conversion service.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="a20f0-120">В демонстрационной базе денных CRONUS International Ltd. поля "Имя пользователя" и "Пароль" предварительно заполняются демонстрационными данными для входа, которые следует заменить фактическими сведениями об организации при подписке на службу преобразования банковских данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-120">In the CRONUS International Ltd. demonstration database, the User Name and Password fields are prefilled with demonstration logon information, which you will replace with your company’s actual information as you sign up for the bank data conversion service.</span></span>
3. <span data-ttu-id="a20f0-121">В поле **URL-адрес регистрации** нажмите кнопку браузера, чтобы открыть страницу регистрации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a20f0-121">In the **Sign-up URL** field, choose the browser button to open the service provider’s sign-up page.</span></span>  
4. <span data-ttu-id="a20f0-122">На странице регистрации поставщика службы преобразования банковских данных введите имя пользователя и пароль для подписки организации на обслуживание, а затем пройдите процесс регистрации, как указано поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="a20f0-122">On the sign-up page of the bank data service provider, enter the user name and password for your company’s subscription to the service, and then complete the sign-up process as instructed by the service provider.</span></span>

  <span data-ttu-id="a20f0-123">Организация подписана на службу преобразования банковских данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-123">Your company is now signed up for the bank data conversion service.</span></span> <span data-ttu-id="a20f0-124">Затем введите имя пользователя и пароль, указанные для службы в связанных полях настройки в [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a20f0-124">Proceed to enter the user name and password that you specified for the service in the related setup fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
5. <span data-ttu-id="a20f0-125">В окне **Настройка службы преобр. банковских данных** в поле **Имя** введите то же значение, которое было введено как имя для входа на странице поставщика услуг на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="a20f0-125">In the **Bank Data Conv. Service Setup** window, in the User **Name** field, enter the same value that you entered as logon name on the service provider’s page in step 4.</span></span>
6. <span data-ttu-id="a20f0-126">В поле **Пароль** введите то же значение, которое было введено в поле **Пароль** на странице поставщика услуг на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="a20f0-126">In the **Password** field, enter the same value that you entered in the **Password** field on the service provider’s page in step 4.</span></span>

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="a20f0-127">Шифрование реквизитов доступа</span><span class="sxs-lookup"><span data-stu-id="a20f0-127">To encrypt your login information</span></span>
<span data-ttu-id="a20f0-128">Рекомендуется защищать данные для входа, введенные в окне **Настройка службы преобр. банковских данных**.</span><span class="sxs-lookup"><span data-stu-id="a20f0-128">It is recommended that you protect the logon information that you enter in the **Bank Data Conv. Service Setup** window.</span></span> <span data-ttu-id="a20f0-129">Можно зашифровать данные на сервере [!INCLUDE[d365fin](includes/d365fin_md.md)], создав новые или импортировав существующие ключи шифрования, включаемые на экземпляре сервера [!INCLUDE[d365fin](includes/d365fin_md.md)], подключенном к базе данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-129">You can encrypt data on the [!INCLUDE[d365fin](includes/d365fin_md.md)] server by generating new or importing existing encryption keys that you enable on the [!INCLUDE[d365fin](includes/d365fin_md.md)] server instance that connects to the database.</span></span>

1. <span data-ttu-id="a20f0-130">В окне **Настройка службы преобр. банковских данных** выберите действие **Управление шифрованием**.</span><span class="sxs-lookup"><span data-stu-id="a20f0-130">In the **Bank Data Conv. Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="a20f0-131">В окне **Управление шифрованием данных** включите шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-131">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a><span data-ttu-id="a20f0-132">Просмотр или обновление списка поддерживаемых в настоящее время форматов банковских данных</span><span class="sxs-lookup"><span data-stu-id="a20f0-132">To view or update the list of currently supported bank data formats</span></span>
1. <span data-ttu-id="a20f0-133">Выберите значок ![Поиск страницы или отчета](media/ui-search/search_small.png "Значок поиска страницы или отчета"), введите **Настройка службы преобр. банковских данных**, а затем выберите связанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="a20f0-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Data Conv. Service Setup** , and then choose the related link.</span></span>
2. <span data-ttu-id="a20f0-134">В окне **Настройка службы преобр. банковских данных** выберите **Название банка – Список преобр. данных**, чтобы открыть список наименований банка, представляющих форматы банковских данных, поддерживаемые службой преобразования.</span><span class="sxs-lookup"><span data-stu-id="a20f0-134">In the **Bank Data Conv. Service Setup** window, choose the **Bank Name - Data Conversion List** action to open the list of bank names representing bank data formats that are supported by the conversion service.</span></span>
3. <span data-ttu-id="a20f0-135">На странице **Название банка – Список преобр. данных** выберите **Обновить список названий банков**.</span><span class="sxs-lookup"><span data-stu-id="a20f0-135">In the **Bank Name - Data Conversion List** page, choose the **Update Bank Name List** action.</span></span>

<span data-ttu-id="a20f0-136">Список форматов банковских данных, поддерживаемых службой преобразования банковских данных, теперь обновлен.</span><span class="sxs-lookup"><span data-stu-id="a20f0-136">The list of bank data formats that are supported by the bank data conversion service is now updated.</span></span> <span data-ttu-id="a20f0-137">Это список названий банков, отфильтрованный по странам и регионам, которые можно выбрать в поле **Название банка - преобразование данных** окна **Карточка банковского счета**.</span><span class="sxs-lookup"><span data-stu-id="a20f0-137">This is the list of bank names, filtered by the country/region, that you can select from in the **Bank Name - Data Conversion** field in the **Bank Account Card** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a20f0-138">Обновление поддерживаемых форматов банковских данных также происходит при выборе или вводе значения в поле **Название банка - преобразование данных**.</span><span class="sxs-lookup"><span data-stu-id="a20f0-138">The update of supported bank data formats also occurs when you select or enter a value in the **Bank Name - Data Conversion** field on the bank account.</span></span>

<span data-ttu-id="a20f0-139">Вы подписаны на услуги преобразования банковских данных.</span><span class="sxs-lookup"><span data-stu-id="a20f0-139">You have now signed up for the bank data conversion service.</span></span> <span data-ttu-id="a20f0-140">Продолжите для добавления сведений о регистрации в каждый банковский счет, который будет использовать эту службу.</span><span class="sxs-lookup"><span data-stu-id="a20f0-140">Proceed to reflect the sign-up information on every bank account that will use the service.</span></span>

## <a name="see-also"></a><span data-ttu-id="a20f0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a20f0-141">See Also</span></span>
[<span data-ttu-id="a20f0-142">Настройка банковских операций</span><span class="sxs-lookup"><span data-stu-id="a20f0-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="a20f0-143">Управление банковскими счетами</span><span class="sxs-lookup"><span data-stu-id="a20f0-143">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="a20f0-144">[Работа с [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a20f0-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
