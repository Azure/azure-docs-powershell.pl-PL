---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 84d0d1711c9ed29aa48c4845787529a46686da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975953"
---
# <span data-ttu-id="e159c-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="e159c-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="e159c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e159c-102">SYNOPSIS</span></span>
<span data-ttu-id="e159c-103">Przekaż pliki dziennika usługi węzła obliczeniowego do kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e159c-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="e159c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e159c-104">SYNTAX</span></span>

### <span data-ttu-id="e159c-105">AzureBatchComputeNodeServiceLogUpload (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e159c-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e159c-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e159c-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e159c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="e159c-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e159c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e159c-108">DESCRIPTION</span></span>
<span data-ttu-id="e159c-109">To polecenie cmdlet zbiera pliki dziennika usługi wsadowej platformy Azure z węzłów obliczeniowych, jeśli występuje błąd i chcesz eskalować do obsługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e159c-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="e159c-110">Pliki dziennika usługi wsadowej platformy Azure powinny być udostępniane pomocy technicznej platformy Azure, aby pomóc w debugowaniu problemów z usługą wsadową.</span><span class="sxs-lookup"><span data-stu-id="e159c-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="e159c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e159c-111">EXAMPLES</span></span>

### <span data-ttu-id="e159c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e159c-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="e159c-113">Przekaż dzienniki usługi węzła obliczeniowego napisane po 1 stycznia 2018 r. o północy, uzyskane z węzła obliczeniowego, podanego identyfikatora puli puli, w której znajduje się węzeł obliczeniowy, i identyfikatora węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e159c-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="e159c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e159c-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="e159c-115">Przekaż dzienniki usługi węzła obliczeniowego napisane po 1 stycznia 2018 r. (północ) i przed 10 stycznia 2018 r., które zostały uzyskane z węzła obliczeniowego, podanego identyfikatora puli puli, w której znajduje się węzeł obliczeniowy, i identyfikatora węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e159c-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="e159c-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e159c-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="e159c-117">Przekazywanie dzienników usługi węzła obliczeniowego napisanych 1 stycznia 2018 r. (północ) i przed 10 stycznia 2018 r., które zostały uzyskane z obiektu węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e159c-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="e159c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e159c-118">PARAMETERS</span></span>

### <span data-ttu-id="e159c-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="e159c-119">-BatchContext</span></span>
<span data-ttu-id="e159c-120">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą batch.</span><span class="sxs-lookup"><span data-stu-id="e159c-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e159c-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e159c-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e159c-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e159c-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e159c-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="e159c-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e159c-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e159c-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e159c-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e159c-125">-ComputeNode</span></span>
<span data-ttu-id="e159c-126">Określa obiekt **PSComputeNode,** z którego są pobierane dzienniki usługi.</span><span class="sxs-lookup"><span data-stu-id="e159c-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e159c-127">-ComputeNodeId</span></span>
<span data-ttu-id="e159c-128">Identyfikator węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e159c-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e159c-129">-ContainerUrl</span></span>
<span data-ttu-id="e159c-130">Adres URL kontenera do usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e159c-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e159c-131">-DefaultProfile</span></span>
<span data-ttu-id="e159c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e159c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e159c-133">- EndTime</span><span class="sxs-lookup"><span data-stu-id="e159c-133">-EndTime</span></span>
<span data-ttu-id="e159c-134">Czas zakończenia przekazywanego dziennika usługi (opcjonalnie).</span><span class="sxs-lookup"><span data-stu-id="e159c-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-135">- PoolId</span><span class="sxs-lookup"><span data-stu-id="e159c-135">-PoolId</span></span>
<span data-ttu-id="e159c-136">Identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="e159c-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-137">— StartTime</span><span class="sxs-lookup"><span data-stu-id="e159c-137">-StartTime</span></span>
<span data-ttu-id="e159c-138">Godzina rozpoczęcia pracy dziennika usługi do przesłania.</span><span class="sxs-lookup"><span data-stu-id="e159c-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e159c-139">-Confirm</span></span>
<span data-ttu-id="e159c-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e159c-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e159c-141">-WhatIf</span></span>
<span data-ttu-id="e159c-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e159c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e159c-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e159c-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e159c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e159c-144">CommonParameters</span></span>
<span data-ttu-id="e159c-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e159c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e159c-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e159c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e159c-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e159c-147">INPUTS</span></span>

### <span data-ttu-id="e159c-148">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e159c-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="e159c-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e159c-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e159c-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e159c-150">OUTPUTS</span></span>

### <span data-ttu-id="e159c-151">Microsoft.Azure.Commands.Batch. Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="e159c-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="e159c-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e159c-152">NOTES</span></span>

## <span data-ttu-id="e159c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e159c-153">RELATED LINKS</span></span>
