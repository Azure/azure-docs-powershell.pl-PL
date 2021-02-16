---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199538"
---
# <span data-ttu-id="01b6d-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="01b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="01b6d-103">Usuwa zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="01b6d-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="01b6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01b6d-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01b6d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="01b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="01b6d-106">Polecenie **cmdlet Remove-AzBatchJob** usuwa zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="01b6d-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="01b6d-107">To polecenie cmdlet wyświetli monit o potwierdzenie przed usunięciem zadania, chyba że określisz *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="01b6d-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="01b6d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01b6d-108">EXAMPLES</span></span>

### <span data-ttu-id="01b6d-109">Przykład 1. Usuwanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="01b6d-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="01b6d-110">To polecenie usuwa zadanie o identyfikatorze Zadanie-000001.</span><span class="sxs-lookup"><span data-stu-id="01b6d-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="01b6d-111">Polecenie wyświetli monit o potwierdzenie przed usunięciem zadania.</span><span class="sxs-lookup"><span data-stu-id="01b6d-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="01b6d-112">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="01b6d-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="01b6d-113">Przykład 2. Usuwanie zadania wsadowego bez potwierdzenia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="01b6d-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="01b6d-114">To polecenie pobiera zadanie o identyfikatorze Zadanie-000002 przy użyciu Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b6d-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="01b6d-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="01b6d-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="01b6d-116">Polecenie usuwa to zadanie.</span><span class="sxs-lookup"><span data-stu-id="01b6d-116">The command deletes that job.</span></span>
<span data-ttu-id="01b6d-117">Ponieważ to polecenie zawiera parametr *Force,* nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01b6d-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="01b6d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b6d-118">PARAMETERS</span></span>

### <span data-ttu-id="01b6d-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="01b6d-119">-BatchContext</span></span>
<span data-ttu-id="01b6d-120">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="01b6d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="01b6d-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01b6d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="01b6d-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="01b6d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="01b6d-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="01b6d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="01b6d-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="01b6d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="01b6d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b6d-125">-DefaultProfile</span></span>
<span data-ttu-id="01b6d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01b6d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01b6d-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="01b6d-127">-Force</span></span>
<span data-ttu-id="01b6d-128">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="01b6d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01b6d-129">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="01b6d-129">-Id</span></span>
<span data-ttu-id="01b6d-130">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b6d-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="01b6d-131">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="01b6d-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b6d-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01b6d-132">-Confirm</span></span>
<span data-ttu-id="01b6d-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01b6d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b6d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b6d-134">-WhatIf</span></span>
<span data-ttu-id="01b6d-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b6d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b6d-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01b6d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b6d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b6d-137">CommonParameters</span></span>
<span data-ttu-id="01b6d-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b6d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b6d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01b6d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b6d-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01b6d-140">INPUTS</span></span>

### <span data-ttu-id="01b6d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="01b6d-141">System.String</span></span>

### <span data-ttu-id="01b6d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="01b6d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="01b6d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01b6d-143">OUTPUTS</span></span>

### <span data-ttu-id="01b6d-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="01b6d-144">System.Void</span></span>

## <span data-ttu-id="01b6d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01b6d-145">NOTES</span></span>

## <span data-ttu-id="01b6d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01b6d-146">RELATED LINKS</span></span>

[<span data-ttu-id="01b6d-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="01b6d-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="01b6d-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="01b6d-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="01b6d-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="01b6d-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="01b6d-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="01b6d-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="01b6d-153">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="01b6d-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
