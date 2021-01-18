---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/resolve-azerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
ms.openlocfilehash: 446b9e107f49b0032b4905cb9d0beee5160d3733
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500553"
---
# <span data-ttu-id="80f8e-101">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="80f8e-101">Resolve-AzError</span></span>

## <span data-ttu-id="80f8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="80f8e-103">Wyświetlanie szczegółowych informacji o błędach programu PowerShell z rozszerzonymi szczegółami dotyczącymi błędów programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="80f8e-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

## <span data-ttu-id="80f8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80f8e-104">SYNTAX</span></span>

### <span data-ttu-id="80f8e-105">AnyErrorParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80f8e-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80f8e-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f8e-106">LastErrorParameterSet</span></span>
```
Resolve-AzError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f8e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="80f8e-108">Rozpoznaje i wyświetla szczegółowe informacje o błędach w bieżącej sesji programu PowerShell, w tym miejsce wystąpienia błędu w skrypcie, śledzenie stosu i wszystkie wyjątki wewnętrzne i zbiorcze.</span><span class="sxs-lookup"><span data-stu-id="80f8e-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="80f8e-109">W przypadku błędów programu Azure PowerShell są dostępne dodatkowe szczegóły dotyczące debugowania problemów z usługą, w tym pełnych szczegółów dotyczących żądania i odpowiedzi serwera, która spowodowała błąd.</span><span class="sxs-lookup"><span data-stu-id="80f8e-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="80f8e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80f8e-110">EXAMPLES</span></span>

### <span data-ttu-id="80f8e-111">Przykład 1: Usuwanie ostatniego błędu</span><span class="sxs-lookup"><span data-stu-id="80f8e-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzError -Last

   HistoryId: 3


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="80f8e-112">Uzyskiwanie szczegółowych informacji o ostatnim błędzie.</span><span class="sxs-lookup"><span data-stu-id="80f8e-112">Get details of the last error.</span></span>

### <span data-ttu-id="80f8e-113">Przykład 2: Usuwanie wszystkich błędów w sesji</span><span class="sxs-lookup"><span data-stu-id="80f8e-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="80f8e-114">Uzyskiwanie szczegółowych informacji o wszystkich błędach, które wystąpiły w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="80f8e-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="80f8e-115">Przykład 3: usuwanie określonego błędu</span><span class="sxs-lookup"><span data-stu-id="80f8e-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="80f8e-116">Uzyskiwanie szczegółowych informacji o określonym błędzie.</span><span class="sxs-lookup"><span data-stu-id="80f8e-116">Get details of the specified error.</span></span>

## <span data-ttu-id="80f8e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80f8e-117">PARAMETERS</span></span>

### <span data-ttu-id="80f8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f8e-118">-DefaultProfile</span></span>
<span data-ttu-id="80f8e-119">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="80f8e-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f8e-120">-Błąd</span><span class="sxs-lookup"><span data-stu-id="80f8e-120">-Error</span></span>
<span data-ttu-id="80f8e-121">Jeden lub więcej rekordów błędów do rozpoznajenia.</span><span class="sxs-lookup"><span data-stu-id="80f8e-121">One or more error records to resolve.</span></span>  <span data-ttu-id="80f8e-122">Jeśli nie określono żadnych parametrów, zostaną rozwiązane wszystkie błędy w sesji.</span><span class="sxs-lookup"><span data-stu-id="80f8e-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f8e-123">-Last</span><span class="sxs-lookup"><span data-stu-id="80f8e-123">-Last</span></span>
<span data-ttu-id="80f8e-124">Usuń tylko ostatni błąd, który wystąpił w sesji.</span><span class="sxs-lookup"><span data-stu-id="80f8e-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f8e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f8e-125">CommonParameters</span></span>
<span data-ttu-id="80f8e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f8e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f8e-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80f8e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f8e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80f8e-128">INPUTS</span></span>

### <span data-ttu-id="80f8e-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="80f8e-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="80f8e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80f8e-130">OUTPUTS</span></span>

### <span data-ttu-id="80f8e-131">Microsoft. Azure. Commands. profile. Errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="80f8e-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="80f8e-132">Microsoft. Azure. Commands. profile. Errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="80f8e-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="80f8e-133">Microsoft. Azure. Commands. profile. Errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="80f8e-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="80f8e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80f8e-134">NOTES</span></span>

## <span data-ttu-id="80f8e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80f8e-135">RELATED LINKS</span></span>
