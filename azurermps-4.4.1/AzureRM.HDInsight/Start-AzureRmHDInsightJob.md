---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 5512482b6b8edc0d9c336c8879eb43072143ff53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719307"
---
# <span data-ttu-id="f570a-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f570a-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="f570a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f570a-102">SYNOPSIS</span></span>
<span data-ttu-id="f570a-103">Rozpoczynanie zdefiniowanego zadania usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="f570a-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f570a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f570a-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f570a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f570a-105">DESCRIPTION</span></span>
<span data-ttu-id="f570a-106">Polecenie cmdlet **Start-AzureRMHDInsightJob** uruchamia zdefiniowane zadanie usługi Azure HDInsight dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="f570a-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="f570a-107">Może to być zadanie MapReduce, strumieniowe zadanie MapReduce, zadanie gałęzi lub zadanie wieprzowe.</span><span class="sxs-lookup"><span data-stu-id="f570a-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="f570a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f570a-108">EXAMPLES</span></span>

### <span data-ttu-id="f570a-109">Przykład 1. Uruchom zadanie w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="f570a-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f570a-110">To polecenie uruchamia zadanie w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f570a-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f570a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f570a-111">PARAMETERS</span></span>

### <span data-ttu-id="f570a-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="f570a-112">-ClusterName</span></span>
<span data-ttu-id="f570a-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f570a-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f570a-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f570a-114">-HttpCredential</span></span>
<span data-ttu-id="f570a-115">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f570a-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f570a-116">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="f570a-116">-JobDefinition</span></span>
<span data-ttu-id="f570a-117">Określa zadanie, które ma zostać uruchomione w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f570a-117">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f570a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f570a-118">-ResourceGroupName</span></span>
<span data-ttu-id="f570a-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f570a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f570a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f570a-120">-DefaultProfile</span></span>
<span data-ttu-id="f570a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f570a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f570a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f570a-122">CommonParameters</span></span>
<span data-ttu-id="f570a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f570a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f570a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f570a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f570a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f570a-125">INPUTS</span></span>

### <span data-ttu-id="f570a-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f570a-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="f570a-127">Parametr "JobDefinition" akceptuje wartość typu "AzureHDInsightJobDefinition" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f570a-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="f570a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f570a-128">OUTPUTS</span></span>

### <span data-ttu-id="f570a-129">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f570a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f570a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f570a-130">NOTES</span></span>

## <span data-ttu-id="f570a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f570a-131">RELATED LINKS</span></span>

[<span data-ttu-id="f570a-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f570a-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="f570a-133">Nowe — AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f570a-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f570a-134">Zatrzymaj — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f570a-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="f570a-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f570a-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


