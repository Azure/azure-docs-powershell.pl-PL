---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547044"
---
# <span data-ttu-id="7cf10-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="7cf10-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="7cf10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cf10-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf10-103">Usuwa plik węzła zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="7cf10-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cf10-104">SYNTAX</span></span>

### <span data-ttu-id="7cf10-105">Zadanie</span><span class="sxs-lookup"><span data-stu-id="7cf10-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf10-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7cf10-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf10-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="7cf10-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cf10-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7cf10-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf10-109">Polecenie cmdlet **Remove-AzureBatchNodeFile** usuwa plik węzła usługi Azure Batch dla węzła zadania lub obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="7cf10-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="7cf10-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cf10-110">EXAMPLES</span></span>

### <span data-ttu-id="7cf10-111">Przykład 1: usuwanie pliku assocated z zadaniem</span><span class="sxs-lookup"><span data-stu-id="7cf10-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="7cf10-112">To polecenie powoduje usunięcie pliku węzła o nazwie wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="7cf10-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="7cf10-113">Ten plik jest skojarzony z zadaniem o IDENTYFIKATORze Task26 w obszarze zadanie zadania-000001.</span><span class="sxs-lookup"><span data-stu-id="7cf10-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="7cf10-114">Przykład 2: usuwanie pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="7cf10-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="7cf10-115">To polecenie usuwa plik węzła o nazwie startup\testFile.txt z określonego węzła obliczeniowego w puli o IDENTYFIKATORze Pool07.</span><span class="sxs-lookup"><span data-stu-id="7cf10-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="7cf10-116">Przykład 3: usuwanie pliku za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="7cf10-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="7cf10-117">To polecenie pobiera plik węzła za pomocą polecenia **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="7cf10-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="7cf10-118">Ten plik jest skojarzony z zadaniem o IDENTYFIKATORze Task26 w obszarze zadanie zadania-000001.</span><span class="sxs-lookup"><span data-stu-id="7cf10-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="7cf10-119">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="7cf10-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="7cf10-120">Bieżące polecenie cmdlet powoduje usunięcie pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="7cf10-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="7cf10-121">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="7cf10-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7cf10-122">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cf10-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7cf10-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cf10-123">PARAMETERS</span></span>

### <span data-ttu-id="7cf10-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7cf10-124">-BatchContext</span></span>
<span data-ttu-id="7cf10-125">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7cf10-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7cf10-126">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="7cf10-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7cf10-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7cf10-127">-ComputeNodeId</span></span>
<span data-ttu-id="7cf10-128">Określa identyfikator węzła obliczeniowego zawierającego plik węzła partii, który zostanie usunięty przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7cf10-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf10-129">-Force</span></span>
<span data-ttu-id="7cf10-130">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7cf10-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cf10-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7cf10-131">-InputObject</span></span>
<span data-ttu-id="7cf10-132">Określa obiekt **PSNodeFile** reprezentujący plik węzła, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="7cf10-133">Aby uzyskać **PSNodeFile** , użyj polecenia cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="7cf10-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="7cf10-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="7cf10-134">-JobId</span></span>
<span data-ttu-id="7cf10-135">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="7cf10-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="7cf10-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7cf10-136">-Name</span></span>
<span data-ttu-id="7cf10-137">Określa nazwę pliku węzła, który zostanie usunięty przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7cf10-138">-PoolId</span></span>
<span data-ttu-id="7cf10-139">Określa identyfikator puli zawierającej węzły obliczeniowe, dla których to polecenie cmdlet usunie plik.</span><span class="sxs-lookup"><span data-stu-id="7cf10-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="7cf10-140">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="7cf10-140">-Recursive</span></span>
<span data-ttu-id="7cf10-141">Wskazuje, że to polecenie cmdlet usunie folder oraz wszystkie podfoldery i pliki znajdujące się pod określoną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="7cf10-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="7cf10-142">To polecenie cmdlet jest istotne tylko wtedy, gdy ścieżka jest folderem.</span><span class="sxs-lookup"><span data-stu-id="7cf10-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="7cf10-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="7cf10-143">-TaskId</span></span>
<span data-ttu-id="7cf10-144">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="7cf10-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="7cf10-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf10-145">-Confirm</span></span>
<span data-ttu-id="7cf10-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf10-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf10-147">-WhatIf</span></span>
<span data-ttu-id="7cf10-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf10-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cf10-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf10-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf10-150">-DefaultProfile</span></span>
<span data-ttu-id="7cf10-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf10-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf10-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf10-152">CommonParameters</span></span>
<span data-ttu-id="7cf10-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf10-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf10-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf10-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf10-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf10-155">INPUTS</span></span>

### <span data-ttu-id="7cf10-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7cf10-156">BatchAccountContext</span></span>
<span data-ttu-id="7cf10-157">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7cf10-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7cf10-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="7cf10-158">PSNodeFile</span></span>
<span data-ttu-id="7cf10-159">Parametr "Inputobject" przyjmuje wartość typu "PSNodeFile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7cf10-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="7cf10-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cf10-160">OUTPUTS</span></span>

## <span data-ttu-id="7cf10-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cf10-161">NOTES</span></span>

## <span data-ttu-id="7cf10-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf10-162">RELATED LINKS</span></span>

[<span data-ttu-id="7cf10-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7cf10-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7cf10-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="7cf10-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="7cf10-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="7cf10-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


