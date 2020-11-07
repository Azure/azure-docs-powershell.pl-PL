---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 4b30d27555f12cb768c87cabfc7277aa592f2c63
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710805"
---
# <span data-ttu-id="152a0-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="152a0-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="152a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="152a0-102">SYNOPSIS</span></span>
<span data-ttu-id="152a0-103">Usuwa plik węzła zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="152a0-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="152a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="152a0-104">SYNTAX</span></span>

### <span data-ttu-id="152a0-105">Zadanie</span><span class="sxs-lookup"><span data-stu-id="152a0-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152a0-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="152a0-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152a0-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="152a0-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152a0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="152a0-108">DESCRIPTION</span></span>
<span data-ttu-id="152a0-109">Polecenie cmdlet **Remove-AzBatchNodeFile** usuwa plik węzła usługi Azure Batch dla węzła zadania lub obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="152a0-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="152a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="152a0-110">EXAMPLES</span></span>

### <span data-ttu-id="152a0-111">Przykład 1: usuwanie pliku assocated z zadaniem</span><span class="sxs-lookup"><span data-stu-id="152a0-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="152a0-112">To polecenie powoduje usunięcie pliku węzła o nazwie wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="152a0-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="152a0-113">Ten plik jest skojarzony z zadaniem o IDENTYFIKATORze Task26 w obszarze zadanie zadania-000001.</span><span class="sxs-lookup"><span data-stu-id="152a0-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="152a0-114">Przykład 2: usuwanie pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="152a0-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="152a0-115">To polecenie usuwa plik węzła o nazwie startup\testFile.txt z określonego węzła obliczeniowego w puli o IDENTYFIKATORze Pool07.</span><span class="sxs-lookup"><span data-stu-id="152a0-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="152a0-116">Przykład 3: usuwanie pliku za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="152a0-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="152a0-117">To polecenie pobiera plik węzła za pomocą polecenia **Get-AzBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="152a0-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="152a0-118">Ten plik jest skojarzony z zadaniem o IDENTYFIKATORze Task26 w obszarze zadanie zadania-000001.</span><span class="sxs-lookup"><span data-stu-id="152a0-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="152a0-119">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="152a0-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="152a0-120">Bieżące polecenie cmdlet powoduje usunięcie pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="152a0-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="152a0-121">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="152a0-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="152a0-122">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="152a0-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="152a0-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="152a0-123">PARAMETERS</span></span>

### <span data-ttu-id="152a0-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="152a0-124">-BatchContext</span></span>
<span data-ttu-id="152a0-125">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="152a0-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="152a0-126">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="152a0-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="152a0-127">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="152a0-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="152a0-128">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="152a0-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="152a0-129">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="152a0-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="152a0-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="152a0-130">-ComputeNodeId</span></span>
<span data-ttu-id="152a0-131">Określa identyfikator węzła obliczeniowego zawierającego plik węzła partii, który zostanie usunięty przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152a0-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="152a0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152a0-132">-DefaultProfile</span></span>
<span data-ttu-id="152a0-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="152a0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="152a0-134">-Force</span><span class="sxs-lookup"><span data-stu-id="152a0-134">-Force</span></span>
<span data-ttu-id="152a0-135">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="152a0-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="152a0-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="152a0-136">-InputObject</span></span>
<span data-ttu-id="152a0-137">Określa obiekt **PSNodeFile** reprezentujący plik węzła, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152a0-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="152a0-138">Aby uzyskać **PSNodeFile** , użyj polecenia cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="152a0-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="152a0-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="152a0-139">-JobId</span></span>
<span data-ttu-id="152a0-140">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="152a0-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="152a0-141">-Path</span><span class="sxs-lookup"><span data-stu-id="152a0-141">-Path</span></span>
<span data-ttu-id="152a0-142">Ścieżka pliku węzła do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="152a0-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="152a0-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="152a0-143">-PoolId</span></span>
<span data-ttu-id="152a0-144">Określa identyfikator puli zawierającej węzły obliczeniowe, dla których to polecenie cmdlet usunie plik.</span><span class="sxs-lookup"><span data-stu-id="152a0-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="152a0-145">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="152a0-145">-Recursive</span></span>
<span data-ttu-id="152a0-146">Wskazuje, że to polecenie cmdlet usunie folder oraz wszystkie podfoldery i pliki znajdujące się pod określoną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="152a0-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="152a0-147">To polecenie cmdlet jest istotne tylko wtedy, gdy ścieżka jest folderem.</span><span class="sxs-lookup"><span data-stu-id="152a0-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="152a0-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="152a0-148">-TaskId</span></span>
<span data-ttu-id="152a0-149">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="152a0-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="152a0-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="152a0-150">-Confirm</span></span>
<span data-ttu-id="152a0-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152a0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152a0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152a0-152">-WhatIf</span></span>
<span data-ttu-id="152a0-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152a0-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152a0-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="152a0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152a0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152a0-155">CommonParameters</span></span>
<span data-ttu-id="152a0-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152a0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152a0-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="152a0-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152a0-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="152a0-158">INPUTS</span></span>

### <span data-ttu-id="152a0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="152a0-159">System.String</span></span>

### <span data-ttu-id="152a0-160">Microsoft.Azure.Commands.Batch. Modele. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="152a0-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="152a0-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="152a0-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="152a0-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="152a0-162">OUTPUTS</span></span>

### <span data-ttu-id="152a0-163">System. void</span><span class="sxs-lookup"><span data-stu-id="152a0-163">System.Void</span></span>

## <span data-ttu-id="152a0-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="152a0-164">NOTES</span></span>

## <span data-ttu-id="152a0-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="152a0-165">RELATED LINKS</span></span>

[<span data-ttu-id="152a0-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="152a0-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="152a0-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="152a0-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="152a0-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="152a0-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


