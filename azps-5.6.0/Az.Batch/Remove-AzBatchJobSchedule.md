---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 5e227662e8c0ce1011172eded7b218f627efbbbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009361"
---
# <span data-ttu-id="9b15d-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9b15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b15d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b15d-103">Usuwa harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="9b15d-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="9b15d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b15d-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b15d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b15d-105">DESCRIPTION</span></span>
<span data-ttu-id="9b15d-106">Polecenie **cmdlet Remove-AzBatchJobSchedule** usuwa harmonogram zadań partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b15d-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9b15d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b15d-107">EXAMPLES</span></span>

### <span data-ttu-id="9b15d-108">Przykład 1. Usuwanie harmonogramu zadań wsadowych</span><span class="sxs-lookup"><span data-stu-id="9b15d-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="9b15d-109">To polecenie usuwa harmonogram zadań z identyfikatorem MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="9b15d-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="9b15d-110">Polecenie wyświetli monit o potwierdzenie przed usunięciem zadania.</span><span class="sxs-lookup"><span data-stu-id="9b15d-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="9b15d-111">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="9b15d-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9b15d-112">Przykład 2. Usuwanie zadania wsadowego bez potwierdzenia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="9b15d-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="9b15d-113">To polecenie pobiera harmonogram zadań, który ma identyfikator MyJobSchedule, za pomocą Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b15d-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="9b15d-114">Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9b15d-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9b15d-115">To polecenie usuwa ten harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="9b15d-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="9b15d-116">Polecenie zawiera parametr *Force,* dlatego nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b15d-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9b15d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b15d-117">PARAMETERS</span></span>

### <span data-ttu-id="9b15d-118">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="9b15d-118">-BatchContext</span></span>
<span data-ttu-id="9b15d-119">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="9b15d-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b15d-120">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9b15d-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b15d-121">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9b15d-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b15d-122">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="9b15d-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b15d-123">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9b15d-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b15d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b15d-124">-DefaultProfile</span></span>
<span data-ttu-id="9b15d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b15d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b15d-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9b15d-126">-Force</span></span>
<span data-ttu-id="9b15d-127">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9b15d-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b15d-128">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9b15d-128">-Id</span></span>
<span data-ttu-id="9b15d-129">Określa identyfikator harmonogramu zadań do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9b15d-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="9b15d-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b15d-130">-Confirm</span></span>
<span data-ttu-id="9b15d-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b15d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b15d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b15d-132">-WhatIf</span></span>
<span data-ttu-id="9b15d-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b15d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b15d-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b15d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b15d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b15d-135">CommonParameters</span></span>
<span data-ttu-id="9b15d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b15d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b15d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b15d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b15d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b15d-138">INPUTS</span></span>

### <span data-ttu-id="9b15d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b15d-139">System.String</span></span>

### <span data-ttu-id="9b15d-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b15d-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b15d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b15d-141">OUTPUTS</span></span>

### <span data-ttu-id="9b15d-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="9b15d-142">System.Void</span></span>

## <span data-ttu-id="9b15d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b15d-143">NOTES</span></span>

## <span data-ttu-id="9b15d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b15d-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b15d-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9b15d-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9b15d-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9b15d-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9b15d-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="9b15d-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b15d-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


