---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716592"
---
# <span data-ttu-id="8b991-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b991-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="8b991-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b991-102">SYNOPSIS</span></span>
<span data-ttu-id="8b991-103">Aktualizuje właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="8b991-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b991-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b991-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b991-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b991-105">DESCRIPTION</span></span>
<span data-ttu-id="8b991-106">Polecenie cmdlet **Set-AzureBatchTask** aktualizuje właściwości zadania w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="8b991-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="8b991-107">Użyj polecenia cmdlet Get-AzureBatchTask, aby uzyskać obiekt **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="8b991-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="8b991-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8b991-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8b991-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b991-109">EXAMPLES</span></span>

### <span data-ttu-id="8b991-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="8b991-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="8b991-111">Pierwsze polecenie pobiera zadanie przy użyciu polecenia **Get-AzureBatchTask** , a następnie zapisuje je w zmiennej $Task.</span><span class="sxs-lookup"><span data-stu-id="8b991-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="8b991-112">Następne dwa polecenia modyfikują ograniczenia zadania w $Task.</span><span class="sxs-lookup"><span data-stu-id="8b991-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="8b991-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Task.</span><span class="sxs-lookup"><span data-stu-id="8b991-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="8b991-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b991-114">PARAMETERS</span></span>

### <span data-ttu-id="8b991-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8b991-115">-BatchContext</span></span>
<span data-ttu-id="8b991-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8b991-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8b991-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8b991-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8b991-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b991-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8b991-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b991-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8b991-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8b991-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b991-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b991-121">-DefaultProfile</span></span>
<span data-ttu-id="8b991-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b991-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b991-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="8b991-123">-Task</span></span>
<span data-ttu-id="8b991-124">Określa **PSCloudTask** , do którego to polecenie cmdlet aktualizuje usługę wsadową.</span><span class="sxs-lookup"><span data-stu-id="8b991-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b991-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b991-125">CommonParameters</span></span>
<span data-ttu-id="8b991-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b991-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b991-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b991-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b991-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b991-128">INPUTS</span></span>

### <span data-ttu-id="8b991-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8b991-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="8b991-130">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b991-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="8b991-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8b991-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8b991-132">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b991-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8b991-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b991-133">OUTPUTS</span></span>

### <span data-ttu-id="8b991-134">System. void</span><span class="sxs-lookup"><span data-stu-id="8b991-134">System.Void</span></span>

## <span data-ttu-id="8b991-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b991-135">NOTES</span></span>

## <span data-ttu-id="8b991-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b991-136">RELATED LINKS</span></span>

[<span data-ttu-id="8b991-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b991-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="8b991-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8b991-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8b991-139">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b991-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="8b991-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b991-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="8b991-141">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b991-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="8b991-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8b991-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


