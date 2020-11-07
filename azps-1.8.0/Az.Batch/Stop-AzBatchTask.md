---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7e9a7a5dbcb730bb5aa2be653b32ef4c9690e139
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896897"
---
# <span data-ttu-id="8ac5d-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ac5d-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="8ac5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac5d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac5d-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-103">Stops a Batch task.</span></span>

## <span data-ttu-id="8ac5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac5d-104">SYNTAX</span></span>

### <span data-ttu-id="8ac5d-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="8ac5d-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ac5d-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ac5d-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac5d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac5d-107">DESCRIPTION</span></span>
<span data-ttu-id="8ac5d-108">Polecenie cmdlet **stop-AzBatchTask** zatrzymuje zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="8ac5d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac5d-109">EXAMPLES</span></span>

### <span data-ttu-id="8ac5d-110">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="8ac5d-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="8ac5d-111">To polecenie zatrzymuje zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="8ac5d-112">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="8ac5d-113">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-113">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8ac5d-114">Przykład 2: zatrzymanie zadania wsadowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="8ac5d-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="8ac5d-115">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="8ac5d-116">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8ac5d-117">Polecenie zatrzyma to zadanie.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-117">The command stops that task.</span></span>

## <span data-ttu-id="8ac5d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac5d-118">PARAMETERS</span></span>

### <span data-ttu-id="8ac5d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8ac5d-119">-BatchContext</span></span>
<span data-ttu-id="8ac5d-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ac5d-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8ac5d-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8ac5d-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8ac5d-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8ac5d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac5d-125">-DefaultProfile</span></span>
<span data-ttu-id="8ac5d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac5d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="8ac5d-127">-Id</span></span>
<span data-ttu-id="8ac5d-128">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac5d-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="8ac5d-129">-JobId</span></span>
<span data-ttu-id="8ac5d-130">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac5d-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="8ac5d-131">-Task</span></span>
<span data-ttu-id="8ac5d-132">Określa zadanie, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="8ac5d-133">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac5d-134">CommonParameters</span></span>
<span data-ttu-id="8ac5d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac5d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac5d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac5d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac5d-137">INPUTS</span></span>

### <span data-ttu-id="8ac5d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac5d-138">System.String</span></span>

### <span data-ttu-id="8ac5d-139">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8ac5d-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="8ac5d-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ac5d-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8ac5d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac5d-141">OUTPUTS</span></span>

### <span data-ttu-id="8ac5d-142">System. void</span><span class="sxs-lookup"><span data-stu-id="8ac5d-142">System.Void</span></span>

## <span data-ttu-id="8ac5d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac5d-143">NOTES</span></span>

## <span data-ttu-id="8ac5d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac5d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8ac5d-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ac5d-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="8ac5d-146">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ac5d-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="8ac5d-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ac5d-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="8ac5d-148">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8ac5d-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


