---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200987"
---
# <span data-ttu-id="0eb32-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="0eb32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb32-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb32-103">Usuwa zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="0eb32-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="0eb32-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0eb32-104">SYNTAX</span></span>

### <span data-ttu-id="0eb32-105">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0eb32-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb32-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb32-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb32-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0eb32-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb32-108">Polecenie **cmdlet Remove-AzBatchTask** usuwa zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="0eb32-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="0eb32-109">To polecenie cmdlet wyświetla monit o potwierdzenie, chyba że określisz parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="0eb32-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="0eb32-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0eb32-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb32-111">Przykład 1. Usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="0eb32-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="0eb32-112">To polecenie usuwa zadanie, które ma identyfikator Zadanie23 w ramach zadania o identyfikatorze Zadanie-000001.</span><span class="sxs-lookup"><span data-stu-id="0eb32-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0eb32-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0eb32-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="0eb32-114">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="0eb32-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0eb32-115">Przykład 2. Usuwanie zadania wsadowego przy użyciu potoku bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="0eb32-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="0eb32-116">To polecenie pobiera zadanie Batch o identyfikatorze Zadanie26 w zadaniu o identyfikatorze Zadanie-000001 przy użyciu polecenia cmdlet **Get-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="0eb32-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="0eb32-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="0eb32-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0eb32-118">To polecenie spowoduje usunięcie tego zadania.</span><span class="sxs-lookup"><span data-stu-id="0eb32-118">The command deletes that task.</span></span>
<span data-ttu-id="0eb32-119">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="0eb32-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0eb32-120">Dlatego polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0eb32-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0eb32-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb32-121">PARAMETERS</span></span>

### <span data-ttu-id="0eb32-122">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="0eb32-122">-BatchContext</span></span>
<span data-ttu-id="0eb32-123">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="0eb32-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0eb32-124">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0eb32-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0eb32-125">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="0eb32-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0eb32-126">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="0eb32-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0eb32-127">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0eb32-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0eb32-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb32-128">-DefaultProfile</span></span>
<span data-ttu-id="0eb32-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb32-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb32-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0eb32-130">-Force</span></span>
<span data-ttu-id="0eb32-131">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0eb32-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-132">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0eb32-132">-Id</span></span>
<span data-ttu-id="0eb32-133">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb32-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="0eb32-134">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="0eb32-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0eb32-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb32-135">-InputObject</span></span>
<span data-ttu-id="0eb32-136">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb32-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="0eb32-137">Aby uzyskać obiekt **PSCloudTask,** użyj Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb32-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="0eb32-138">- JobId</span><span class="sxs-lookup"><span data-stu-id="0eb32-138">-JobId</span></span>
<span data-ttu-id="0eb32-139">Określa identyfikator zadania zawierającego to zadanie.</span><span class="sxs-lookup"><span data-stu-id="0eb32-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="0eb32-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0eb32-140">-Confirm</span></span>
<span data-ttu-id="0eb32-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0eb32-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb32-142">-WhatIf</span></span>
<span data-ttu-id="0eb32-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb32-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb32-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0eb32-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb32-145">CommonParameters</span></span>
<span data-ttu-id="0eb32-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb32-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb32-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eb32-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb32-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb32-148">INPUTS</span></span>

### <span data-ttu-id="0eb32-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0eb32-149">System.String</span></span>

### <span data-ttu-id="0eb32-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0eb32-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0eb32-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0eb32-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb32-152">OUTPUTS</span></span>

### <span data-ttu-id="0eb32-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="0eb32-153">System.Void</span></span>

## <span data-ttu-id="0eb32-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0eb32-154">NOTES</span></span>

## <span data-ttu-id="0eb32-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eb32-155">RELATED LINKS</span></span>

[<span data-ttu-id="0eb32-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0eb32-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0eb32-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0eb32-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0eb32-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0eb32-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0eb32-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="0eb32-161">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0eb32-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
