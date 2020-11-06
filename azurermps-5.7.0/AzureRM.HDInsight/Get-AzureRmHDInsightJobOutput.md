---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 2f63ba552931f70b745816a1d1b892977b6626e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554155"
---
# <span data-ttu-id="02e1f-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="02e1f-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="02e1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="02e1f-103">Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.</span><span class="sxs-lookup"><span data-stu-id="02e1f-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02e1f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e1f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="02e1f-106">Polecenie cmdlet **Get-AzureRmHDInsightJobOutput** pobiera dane wyjściowe dziennika zadania z konta magazynu skojarzonego z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="02e1f-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="02e1f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="02e1f-108">Przykład 1. Pobieranie danych wyjściowych dziennika dla zadania</span><span class="sxs-lookup"><span data-stu-id="02e1f-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="02e1f-109">To polecenie pobiera dane wyjściowe dziennika z klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="02e1f-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="02e1f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02e1f-110">PARAMETERS</span></span>

### <span data-ttu-id="02e1f-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="02e1f-111">-ClusterName</span></span>
<span data-ttu-id="02e1f-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="02e1f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="02e1f-113">-DefaultContainer</span></span>
<span data-ttu-id="02e1f-114">Określa domyślną nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="02e1f-114">Specifies the default container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e1f-115">-DefaultProfile</span></span>
<span data-ttu-id="02e1f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02e1f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="02e1f-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="02e1f-118">Określa domyślny klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="02e1f-118">Specifies the default Storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02e1f-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="02e1f-120">Określa domyślną nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="02e1f-120">Specifies the default Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="02e1f-121">-DisplayOutputType</span></span>
<span data-ttu-id="02e1f-122">Określa żądany typ danych wyjściowych zadania.</span><span class="sxs-lookup"><span data-stu-id="02e1f-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="02e1f-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="02e1f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02e1f-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="02e1f-124">StandardOutput</span></span>
- <span data-ttu-id="02e1f-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="02e1f-125">StandardError</span></span>

```yaml
Type: JobDisplayOutputType
Parameter Sets: (All)
Aliases: 
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="02e1f-126">-HttpCredential</span></span>
<span data-ttu-id="02e1f-127">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="02e1f-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="02e1f-128">-JobId</span></span>
<span data-ttu-id="02e1f-129">Określa identyfikator zadania, którego dane wyjściowe będą pobierane.</span><span class="sxs-lookup"><span data-stu-id="02e1f-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e1f-130">-ResourceGroupName</span></span>
<span data-ttu-id="02e1f-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02e1f-131">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e1f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e1f-132">CommonParameters</span></span>
<span data-ttu-id="02e1f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e1f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e1f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e1f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e1f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02e1f-135">INPUTS</span></span>

### <span data-ttu-id="02e1f-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="02e1f-136">None</span></span>
<span data-ttu-id="02e1f-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="02e1f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02e1f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02e1f-138">OUTPUTS</span></span>

### <span data-ttu-id="02e1f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02e1f-139">System.String</span></span>

## <span data-ttu-id="02e1f-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02e1f-140">NOTES</span></span>

## <span data-ttu-id="02e1f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02e1f-141">RELATED LINKS</span></span>

[<span data-ttu-id="02e1f-142">Nowe — AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="02e1f-142">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="02e1f-143">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="02e1f-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


