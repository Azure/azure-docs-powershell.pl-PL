---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547559"
---
# <span data-ttu-id="5d6a8-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="5d6a8-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="5d6a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6a8-103">Przekazywanie plików dziennika usługi węzła obliczeniowego do kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d6a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d6a8-104">SYNTAX</span></span>

### <span data-ttu-id="5d6a8-105">AzureBatchComputeNodeServiceLogUpload (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d6a8-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d6a8-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="5d6a8-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d6a8-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="5d6a8-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d6a8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="5d6a8-109">To polecenie cmdlet zbiera pliki dziennika usługi Azure Batch z węzłów obliczeniowych, jeśli wystąpił błąd i chcesz przeprowadzić eskalację do usługi Azure support.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="5d6a8-110">Pliki dziennika usługi Azure Batch powinny być udostępniane z pomocą techniczną platformy Azure, aby ułatwić Debugowanie problemów z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="5d6a8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d6a8-111">EXAMPLES</span></span>

### <span data-ttu-id="5d6a8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d6a8-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="5d6a8-113">Przekazywanie dzienników usługi węzłów obliczeniowych po 1 stycznia 2018 północ, które zostały uzyskane z węzła compute, podano Identyfikator puli, w którym znajduje się węzeł obliczeniowa, i obliczeniowy identyfikator węzła.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="5d6a8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d6a8-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="5d6a8-115">Przekaż dzienniki usług węzłów obliczeniowych zapisane w dniu 1 stycznia 2018 północ i przed 10 stycznia 2018 północy, które zostały uzyskane z węzła obliczeniowego, podany identyfikator puli puli, w której znajduje się węzeł obliczeniowy, i Oblicz identyfikator węzła.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="5d6a8-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5d6a8-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="5d6a8-117">Przekaż dzienniki usługi węzła obliczeniowego zapisane w dniu 1 stycznia 2018 północ i przed 10 stycznia 2018 północy, które zostały uzyskane z obiektu węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="5d6a8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d6a8-118">PARAMETERS</span></span>

### <span data-ttu-id="5d6a8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5d6a8-119">-BatchContext</span></span>
<span data-ttu-id="5d6a8-120">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5d6a8-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5d6a8-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5d6a8-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5d6a8-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5d6a8-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5d6a8-125">-ComputeNode</span></span>
<span data-ttu-id="5d6a8-126">Określa obiekt **PSComputeNode** , z którego są pobierane dzienniki usług.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="5d6a8-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="5d6a8-127">-ComputeNodeId</span></span>
<span data-ttu-id="5d6a8-128">Identyfikator węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="5d6a8-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="5d6a8-129">-ContainerUrl</span></span>
<span data-ttu-id="5d6a8-130">Adres URL kontenera do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="5d6a8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6a8-131">-DefaultProfile</span></span>
<span data-ttu-id="5d6a8-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d6a8-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5d6a8-133">-EndTime</span></span>
<span data-ttu-id="5d6a8-134">Godzina zakończenia dziennika usługi do przekazania (opcjonalnie).</span><span class="sxs-lookup"><span data-stu-id="5d6a8-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="5d6a8-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5d6a8-135">-PoolId</span></span>
<span data-ttu-id="5d6a8-136">Identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="5d6a8-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5d6a8-137">-StartTime</span></span>
<span data-ttu-id="5d6a8-138">Godzina rozpoczęcia dziennika usługi do przekazania.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="5d6a8-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d6a8-139">-Confirm</span></span>
<span data-ttu-id="5d6a8-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d6a8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d6a8-141">-WhatIf</span></span>
<span data-ttu-id="5d6a8-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d6a8-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d6a8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6a8-144">CommonParameters</span></span>
<span data-ttu-id="5d6a8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6a8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6a8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d6a8-147">INPUTS</span></span>

### <span data-ttu-id="5d6a8-148">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5d6a8-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="5d6a8-149">Parametry: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d6a8-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="5d6a8-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d6a8-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5d6a8-151">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d6a8-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5d6a8-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d6a8-152">OUTPUTS</span></span>

### <span data-ttu-id="5d6a8-153">Microsoft.Azure.Commands.Batch. Modele. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="5d6a8-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="5d6a8-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d6a8-154">NOTES</span></span>

## <span data-ttu-id="5d6a8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d6a8-155">RELATED LINKS</span></span>
