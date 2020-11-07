---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8bfc771ccfa8faf2c7a5eea973d214ac8a639797
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869279"
---
# <span data-ttu-id="48497-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="48497-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="48497-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48497-102">SYNOPSIS</span></span>
<span data-ttu-id="48497-103">Przekazywanie plików dziennika usługi węzła obliczeniowego do kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48497-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="48497-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48497-104">SYNTAX</span></span>

### <span data-ttu-id="48497-105">AzureBatchComputeNodeServiceLogUpload (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48497-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48497-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="48497-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48497-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="48497-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48497-108">Opis</span><span class="sxs-lookup"><span data-stu-id="48497-108">DESCRIPTION</span></span>
<span data-ttu-id="48497-109">To polecenie cmdlet zbiera pliki dziennika usługi Azure Batch z węzłów obliczeniowych, jeśli wystąpił błąd i chcesz przeprowadzić eskalację do usługi Azure support.</span><span class="sxs-lookup"><span data-stu-id="48497-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="48497-110">Pliki dziennika usługi Azure Batch powinny być udostępniane z pomocą techniczną platformy Azure, aby ułatwić Debugowanie problemów z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="48497-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="48497-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48497-111">EXAMPLES</span></span>

### <span data-ttu-id="48497-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48497-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="48497-113">Przekazywanie dzienników usługi węzłów obliczeniowych po 1 stycznia 2018 północ, które zostały uzyskane z węzła compute, podano Identyfikator puli, w którym znajduje się węzeł obliczeniowa, i obliczeniowy identyfikator węzła.</span><span class="sxs-lookup"><span data-stu-id="48497-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="48497-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48497-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="48497-115">Przekaż dzienniki usług węzłów obliczeniowych zapisane w dniu 1 stycznia 2018 północ i przed 10 stycznia 2018 północy, które zostały uzyskane z węzła obliczeniowego, podany identyfikator puli puli, w której znajduje się węzeł obliczeniowy, i Oblicz identyfikator węzła.</span><span class="sxs-lookup"><span data-stu-id="48497-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="48497-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="48497-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="48497-117">Przekaż dzienniki usługi węzła obliczeniowego zapisane w dniu 1 stycznia 2018 północ i przed 10 stycznia 2018 północy, które zostały uzyskane z obiektu węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="48497-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="48497-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48497-118">PARAMETERS</span></span>

### <span data-ttu-id="48497-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48497-119">-BatchContext</span></span>
<span data-ttu-id="48497-120">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="48497-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="48497-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="48497-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="48497-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="48497-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="48497-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="48497-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="48497-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="48497-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48497-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48497-125">-ComputeNode</span></span>
<span data-ttu-id="48497-126">Określa obiekt **PSComputeNode** , z którego są pobierane dzienniki usług.</span><span class="sxs-lookup"><span data-stu-id="48497-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="48497-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="48497-127">-ComputeNodeId</span></span>
<span data-ttu-id="48497-128">Identyfikator węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="48497-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="48497-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="48497-129">-ContainerUrl</span></span>
<span data-ttu-id="48497-130">Adres URL kontenera do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48497-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="48497-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48497-131">-DefaultProfile</span></span>
<span data-ttu-id="48497-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48497-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48497-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="48497-133">-EndTime</span></span>
<span data-ttu-id="48497-134">Godzina zakończenia dziennika usługi do przekazania (opcjonalnie).</span><span class="sxs-lookup"><span data-stu-id="48497-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="48497-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="48497-135">-PoolId</span></span>
<span data-ttu-id="48497-136">Identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="48497-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="48497-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="48497-137">-StartTime</span></span>
<span data-ttu-id="48497-138">Godzina rozpoczęcia dziennika usługi do przekazania.</span><span class="sxs-lookup"><span data-stu-id="48497-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="48497-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48497-139">-Confirm</span></span>
<span data-ttu-id="48497-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48497-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48497-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48497-141">-WhatIf</span></span>
<span data-ttu-id="48497-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48497-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48497-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48497-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48497-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48497-144">CommonParameters</span></span>
<span data-ttu-id="48497-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48497-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48497-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48497-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48497-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48497-147">INPUTS</span></span>

### <span data-ttu-id="48497-148">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48497-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="48497-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48497-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="48497-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48497-150">OUTPUTS</span></span>

### <span data-ttu-id="48497-151">Microsoft.Azure.Commands.Batch. Modele. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="48497-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="48497-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48497-152">NOTES</span></span>

## <span data-ttu-id="48497-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48497-153">RELATED LINKS</span></span>
