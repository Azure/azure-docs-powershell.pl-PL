---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: a56b8d0613946b33629fda46cc710cdbeef0814e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010890"
---
# <span data-ttu-id="06491-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="06491-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="06491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06491-102">SYNOPSIS</span></span>
<span data-ttu-id="06491-103">Usuwa plik węzła dla zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="06491-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="06491-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06491-104">SYNTAX</span></span>

### <span data-ttu-id="06491-105">Zadanie</span><span class="sxs-lookup"><span data-stu-id="06491-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06491-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="06491-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06491-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="06491-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06491-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="06491-108">DESCRIPTION</span></span>
<span data-ttu-id="06491-109">Polecenie **cmdlet Remove-AzBatchNodeFile** usuwa plik węzła usługi Azure Batch dla zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="06491-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="06491-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06491-110">EXAMPLES</span></span>

### <span data-ttu-id="06491-111">Przykład 1. Usuwanie pliku skojarzonego z zadaniem</span><span class="sxs-lookup"><span data-stu-id="06491-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="06491-112">To polecenie usuwa plik węzła o nazwie wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="06491-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="06491-113">Ten plik jest skojarzony z zadaniem o identyfikatorze Zadanie26 w ramach zadania 0000001.</span><span class="sxs-lookup"><span data-stu-id="06491-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="06491-114">Przykład 2. Usuwanie pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="06491-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="06491-115">To polecenie usuwa plik węzła o nazwie startup\testFile.txt z określonego węzła obliczeniowego w puli, która ma pulę identyfikatorów 07.</span><span class="sxs-lookup"><span data-stu-id="06491-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="06491-116">Przykład 3. Usuwanie pliku przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="06491-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="06491-117">To polecenie pobiera plik węzła przy użyciu polecenia **Get-AzBatchNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="06491-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="06491-118">Ten plik jest skojarzony z zadaniem o identyfikatorze Zadanie26 w ramach zadania 0000001.</span><span class="sxs-lookup"><span data-stu-id="06491-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="06491-119">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="06491-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="06491-120">Bieżące polecenie cmdlet usuwa plik węzła.</span><span class="sxs-lookup"><span data-stu-id="06491-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="06491-121">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="06491-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="06491-122">Dlatego to polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06491-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="06491-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06491-123">PARAMETERS</span></span>

### <span data-ttu-id="06491-124">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="06491-124">-BatchContext</span></span>
<span data-ttu-id="06491-125">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="06491-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06491-126">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06491-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="06491-127">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="06491-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="06491-128">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="06491-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="06491-129">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="06491-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="06491-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="06491-130">-ComputeNodeId</span></span>
<span data-ttu-id="06491-131">Określa identyfikator węzła obliczeniowego zawierającego plik węzła Batch usunięty przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06491-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06491-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06491-132">-DefaultProfile</span></span>
<span data-ttu-id="06491-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06491-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06491-134">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="06491-134">-Force</span></span>
<span data-ttu-id="06491-135">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="06491-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06491-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06491-136">-InputObject</span></span>
<span data-ttu-id="06491-137">Określa **obiekt PSNodeFile** reprezentujący plik węzła usunięty przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06491-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="06491-138">Aby uzyskać **plik PSNodeFile,** użyj Get-AzBatchNodeFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06491-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06491-139">- JobId</span><span class="sxs-lookup"><span data-stu-id="06491-139">-JobId</span></span>
<span data-ttu-id="06491-140">Określa identyfikator zadania zawierającego to zadanie.</span><span class="sxs-lookup"><span data-stu-id="06491-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06491-141">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="06491-141">-Path</span></span>
<span data-ttu-id="06491-142">Ścieżka pliku węzła do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="06491-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06491-143">- PoolId</span><span class="sxs-lookup"><span data-stu-id="06491-143">-PoolId</span></span>
<span data-ttu-id="06491-144">Określa identyfikator puli zawierającej węzły obliczeniowe, z których to polecenie cmdlet usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="06491-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06491-145">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="06491-145">-Recursive</span></span>
<span data-ttu-id="06491-146">Wskazuje, że to polecenie cmdlet usuwa folder oraz wszystkie podfoldery i pliki w ramach określonej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="06491-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="06491-147">To polecenie cmdlet ma zastosowanie tylko wtedy, gdy ścieżka jest folderem.</span><span class="sxs-lookup"><span data-stu-id="06491-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="06491-148">- TaskId</span><span class="sxs-lookup"><span data-stu-id="06491-148">-TaskId</span></span>
<span data-ttu-id="06491-149">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="06491-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06491-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06491-150">-Confirm</span></span>
<span data-ttu-id="06491-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06491-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06491-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06491-152">-WhatIf</span></span>
<span data-ttu-id="06491-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06491-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06491-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06491-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06491-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06491-155">CommonParameters</span></span>
<span data-ttu-id="06491-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06491-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06491-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06491-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06491-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06491-158">INPUTS</span></span>

### <span data-ttu-id="06491-159">System.String</span><span class="sxs-lookup"><span data-stu-id="06491-159">System.String</span></span>

### <span data-ttu-id="06491-160">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="06491-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="06491-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="06491-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="06491-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06491-162">OUTPUTS</span></span>

### <span data-ttu-id="06491-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="06491-163">System.Void</span></span>

## <span data-ttu-id="06491-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06491-164">NOTES</span></span>

## <span data-ttu-id="06491-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06491-165">RELATED LINKS</span></span>

[<span data-ttu-id="06491-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="06491-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="06491-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="06491-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="06491-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="06491-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


