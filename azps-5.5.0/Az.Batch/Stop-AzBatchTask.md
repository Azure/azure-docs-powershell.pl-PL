---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199515"
---
# <span data-ttu-id="d29d2-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d29d2-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="d29d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d29d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d29d2-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="d29d2-103">Stops a Batch task.</span></span>

## <span data-ttu-id="d29d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d29d2-104">SYNTAX</span></span>

### <span data-ttu-id="d29d2-105">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="d29d2-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29d2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d29d2-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d29d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d29d2-107">DESCRIPTION</span></span>
<span data-ttu-id="d29d2-108">Polecenie **cmdlet Stop-AzBatchTask** zatrzymuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d29d2-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="d29d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d29d2-109">EXAMPLES</span></span>

### <span data-ttu-id="d29d2-110">Przykład 1. Usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d29d2-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d29d2-111">To polecenie zatrzymuje zadanie o identyfikatorze Zadanie23 w obszarze zadania o identyfikatorze Zadanie 000001.</span><span class="sxs-lookup"><span data-stu-id="d29d2-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d29d2-112">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d29d2-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d29d2-113">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="d29d2-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d29d2-114">Przykład 2. Zatrzymywanie zadania wsadowego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="d29d2-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="d29d2-115">To polecenie pobiera zadanie Batch, które ma identyfikator Zadanie26 w zadaniu, które ma zadanie identyfikatora 0000001, przy użyciu polecenia cmdlet Get-AzBatchTask identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="d29d2-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="d29d2-116">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d29d2-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d29d2-117">Polecenie zatrzyma to zadanie.</span><span class="sxs-lookup"><span data-stu-id="d29d2-117">The command stops that task.</span></span>

## <span data-ttu-id="d29d2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d29d2-118">PARAMETERS</span></span>

### <span data-ttu-id="d29d2-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="d29d2-119">-BatchContext</span></span>
<span data-ttu-id="d29d2-120">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="d29d2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d29d2-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d29d2-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d29d2-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d29d2-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d29d2-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="d29d2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d29d2-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d29d2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d29d2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29d2-125">-DefaultProfile</span></span>
<span data-ttu-id="d29d2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d29d2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29d2-127">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="d29d2-127">-Id</span></span>
<span data-ttu-id="d29d2-128">Określa identyfikator zadania, które ma zatrzymać to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29d2-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d29d2-129">- JobId</span><span class="sxs-lookup"><span data-stu-id="d29d2-129">-JobId</span></span>
<span data-ttu-id="d29d2-130">Określa identyfikator zadania zawierającego to zadanie.</span><span class="sxs-lookup"><span data-stu-id="d29d2-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="d29d2-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d29d2-131">-Task</span></span>
<span data-ttu-id="d29d2-132">Określa zadanie, które ma zatrzymać to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29d2-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="d29d2-133">Aby uzyskać obiekt **PSCloudTask,** użyj Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29d2-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="d29d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29d2-134">CommonParameters</span></span>
<span data-ttu-id="d29d2-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29d2-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d29d2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29d2-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d29d2-137">INPUTS</span></span>

### <span data-ttu-id="d29d2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d29d2-138">System.String</span></span>

### <span data-ttu-id="d29d2-139">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d29d2-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="d29d2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d29d2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d29d2-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d29d2-141">OUTPUTS</span></span>

### <span data-ttu-id="d29d2-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="d29d2-142">System.Void</span></span>

## <span data-ttu-id="d29d2-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d29d2-143">NOTES</span></span>

## <span data-ttu-id="d29d2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d29d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="d29d2-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d29d2-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="d29d2-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d29d2-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d29d2-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d29d2-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d29d2-148">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d29d2-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
