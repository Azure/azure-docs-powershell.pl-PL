---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199547"
---
# <span data-ttu-id="4da16-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="4da16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da16-102">SYNOPSIS</span></span>
<span data-ttu-id="4da16-103">Ponowne aktywowanie zadania.</span><span class="sxs-lookup"><span data-stu-id="4da16-103">Reactivates a task.</span></span>

## <span data-ttu-id="4da16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4da16-104">SYNTAX</span></span>

### <span data-ttu-id="4da16-105">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="4da16-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da16-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4da16-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da16-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4da16-107">DESCRIPTION</span></span>
<span data-ttu-id="4da16-108">Polecenie cmdlet **Enable-AzBatchTask** ponownie aktywuje zadanie.</span><span class="sxs-lookup"><span data-stu-id="4da16-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="4da16-109">Jeśli liczba ponownych prób zadania została wyczerpana, to polecenie cmdlet jednak umożliwia jego uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="4da16-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="4da16-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4da16-110">EXAMPLES</span></span>

### <span data-ttu-id="4da16-111">Przykład 1. Ponowne aktywowanie zadania</span><span class="sxs-lookup"><span data-stu-id="4da16-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="4da16-112">To polecenie ponownie aktywuje zadanie Zadanie2 w zadaniu Job7.</span><span class="sxs-lookup"><span data-stu-id="4da16-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="4da16-113">Przykład 2. Ponowne aktywowanie zadania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="4da16-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="4da16-114">To polecenie pobiera zadanie Batch, które ma identyfikator Zadanie3 w zadaniu, które ma identyfikator Job8, za pomocą Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da16-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="4da16-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4da16-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4da16-116">To polecenie aktywuje ponownie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="4da16-116">The command reactivates that task.</span></span>

## <span data-ttu-id="4da16-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4da16-117">PARAMETERS</span></span>

### <span data-ttu-id="4da16-118">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="4da16-118">-BatchContext</span></span>
<span data-ttu-id="4da16-119">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="4da16-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4da16-120">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4da16-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4da16-121">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4da16-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4da16-122">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="4da16-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4da16-123">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4da16-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4da16-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da16-124">-DefaultProfile</span></span>
<span data-ttu-id="4da16-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4da16-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da16-126">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="4da16-126">-Id</span></span>
<span data-ttu-id="4da16-127">Określa identyfikator zadania do ponownego aktywowania.</span><span class="sxs-lookup"><span data-stu-id="4da16-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="4da16-128">- JobId</span><span class="sxs-lookup"><span data-stu-id="4da16-128">-JobId</span></span>
<span data-ttu-id="4da16-129">Określa identyfikator zadania zawierającego zadanie.</span><span class="sxs-lookup"><span data-stu-id="4da16-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="4da16-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4da16-130">-Task</span></span>
<span data-ttu-id="4da16-131">Określa zadanie, które zostanie uaktywnione ponownie przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da16-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="4da16-132">Aby uzyskać obiekt **PSCloudTask,** użyj Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da16-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="4da16-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4da16-133">-Confirm</span></span>
<span data-ttu-id="4da16-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4da16-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da16-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da16-135">-WhatIf</span></span>
<span data-ttu-id="4da16-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da16-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da16-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4da16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da16-138">CommonParameters</span></span>
<span data-ttu-id="4da16-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da16-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4da16-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da16-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4da16-141">INPUTS</span></span>

### <span data-ttu-id="4da16-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4da16-142">System.String</span></span>

### <span data-ttu-id="4da16-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="4da16-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="4da16-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4da16-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4da16-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4da16-145">OUTPUTS</span></span>

### <span data-ttu-id="4da16-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="4da16-146">System.Void</span></span>

## <span data-ttu-id="4da16-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4da16-147">NOTES</span></span>

## <span data-ttu-id="4da16-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4da16-148">RELATED LINKS</span></span>

[<span data-ttu-id="4da16-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4da16-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4da16-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="4da16-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="4da16-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="4da16-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="4da16-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4da16-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


