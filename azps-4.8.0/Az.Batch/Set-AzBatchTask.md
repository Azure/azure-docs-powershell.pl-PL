---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063634"
---
# <span data-ttu-id="99037-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="99037-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="99037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99037-102">SYNOPSIS</span></span>
<span data-ttu-id="99037-103">Aktualizuje właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="99037-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="99037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99037-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99037-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99037-105">DESCRIPTION</span></span>
<span data-ttu-id="99037-106">Polecenie cmdlet **Set-AzBatchTask** aktualizuje właściwości zadania w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="99037-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="99037-107">Użyj polecenia cmdlet Get-AzBatchTask, aby uzyskać obiekt **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="99037-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="99037-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="99037-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="99037-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99037-109">EXAMPLES</span></span>

### <span data-ttu-id="99037-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="99037-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="99037-111">Pierwsze polecenie pobiera zadanie przy użyciu polecenia **Get-AzBatchTask** , a następnie zapisuje je w zmiennej $Task.</span><span class="sxs-lookup"><span data-stu-id="99037-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="99037-112">Następne dwa polecenia modyfikują ograniczenia zadania w $Task.</span><span class="sxs-lookup"><span data-stu-id="99037-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="99037-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Task.</span><span class="sxs-lookup"><span data-stu-id="99037-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="99037-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99037-114">PARAMETERS</span></span>

### <span data-ttu-id="99037-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99037-115">-BatchContext</span></span>
<span data-ttu-id="99037-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="99037-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99037-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="99037-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99037-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="99037-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99037-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="99037-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99037-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="99037-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99037-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99037-121">-DefaultProfile</span></span>
<span data-ttu-id="99037-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99037-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99037-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="99037-123">-Task</span></span>
<span data-ttu-id="99037-124">Określa **PSCloudTask** , do którego to polecenie cmdlet aktualizuje usługę wsadową.</span><span class="sxs-lookup"><span data-stu-id="99037-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="99037-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99037-125">CommonParameters</span></span>
<span data-ttu-id="99037-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99037-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99037-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99037-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99037-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99037-128">INPUTS</span></span>

### <span data-ttu-id="99037-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="99037-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="99037-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99037-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99037-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99037-131">OUTPUTS</span></span>

### <span data-ttu-id="99037-132">System. void</span><span class="sxs-lookup"><span data-stu-id="99037-132">System.Void</span></span>

## <span data-ttu-id="99037-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99037-133">NOTES</span></span>

## <span data-ttu-id="99037-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99037-134">RELATED LINKS</span></span>

[<span data-ttu-id="99037-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="99037-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="99037-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="99037-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="99037-137">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="99037-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="99037-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="99037-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="99037-139">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="99037-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="99037-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="99037-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
