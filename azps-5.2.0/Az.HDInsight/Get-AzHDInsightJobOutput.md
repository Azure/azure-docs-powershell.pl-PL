---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338242"
---
# <span data-ttu-id="083f7-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="083f7-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="083f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="083f7-102">SYNOPSIS</span></span>
<span data-ttu-id="083f7-103">Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.</span><span class="sxs-lookup"><span data-stu-id="083f7-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="083f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="083f7-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="083f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="083f7-105">DESCRIPTION</span></span>
<span data-ttu-id="083f7-106">Polecenie cmdlet **Get-AzHDInsightJobOutput** pobiera dane wyjściowe dziennika zadania z konta magazynu skojarzonego z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="083f7-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="083f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="083f7-107">EXAMPLES</span></span>

### <span data-ttu-id="083f7-108">Przykład 1. Pobieranie danych wyjściowych dziennika dla zadania</span><span class="sxs-lookup"><span data-stu-id="083f7-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="083f7-109">To polecenie pobiera dane wyjściowe dziennika z klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="083f7-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="083f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="083f7-110">PARAMETERS</span></span>

### <span data-ttu-id="083f7-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="083f7-111">-ClusterName</span></span>
<span data-ttu-id="083f7-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="083f7-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="083f7-113">-DefaultContainer</span></span>
<span data-ttu-id="083f7-114">Określa domyślną nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="083f7-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083f7-115">-DefaultProfile</span></span>
<span data-ttu-id="083f7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="083f7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="083f7-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="083f7-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="083f7-118">Określa domyślny klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="083f7-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="083f7-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="083f7-120">Określa domyślną nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="083f7-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="083f7-121">-DisplayOutputType</span></span>
<span data-ttu-id="083f7-122">Określa żądany typ danych wyjściowych zadania.</span><span class="sxs-lookup"><span data-stu-id="083f7-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="083f7-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="083f7-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="083f7-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="083f7-124">StandardOutput</span></span>
- <span data-ttu-id="083f7-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="083f7-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="083f7-126">-HttpCredential</span></span>
<span data-ttu-id="083f7-127">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="083f7-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="083f7-128">-JobId</span></span>
<span data-ttu-id="083f7-129">Określa identyfikator zadania, którego dane wyjściowe będą pobierane.</span><span class="sxs-lookup"><span data-stu-id="083f7-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="083f7-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="083f7-131">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083f7-132">CommonParameters</span></span>
<span data-ttu-id="083f7-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083f7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083f7-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083f7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083f7-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="083f7-135">INPUTS</span></span>

### <span data-ttu-id="083f7-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="083f7-136">None</span></span>

## <span data-ttu-id="083f7-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="083f7-137">OUTPUTS</span></span>

### <span data-ttu-id="083f7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="083f7-138">System.String</span></span>

## <span data-ttu-id="083f7-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="083f7-139">NOTES</span></span>

## <span data-ttu-id="083f7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="083f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="083f7-141">Nowe — AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="083f7-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="083f7-142">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="083f7-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


