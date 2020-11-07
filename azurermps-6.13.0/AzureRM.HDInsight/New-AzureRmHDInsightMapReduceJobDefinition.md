---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 284bd75abb2a2deaeaf13ad6edeb16718cbcdacd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553576"
---
# <span data-ttu-id="cd4b4-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cd4b4-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="cd4b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4b4-103">Tworzy obiekt zadania programu MapReduce.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd4b4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd4b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd4b4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4b4-106">Polecenie cmdlet **New-AzureRmHDInsightMapReduceJobDefinition** definiuje nowe zadanie MapReduce, które ma być używane w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cd4b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd4b4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd4b4-108">Przykład 1: Tworzenie definicji zadania programu MapReduce</span><span class="sxs-lookup"><span data-stu-id="cd4b4-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cd4b4-109">To polecenie tworzy definicję zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="cd4b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd4b4-110">PARAMETERS</span></span>

### <span data-ttu-id="cd4b4-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="cd4b4-111">-Arguments</span></span>
<span data-ttu-id="cd4b4-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cd4b4-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="cd4b4-114">-ClassName</span></span>
<span data-ttu-id="cd4b4-115">Określa klasę zadania w pliku JAR.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-115">Specifies the job class in the JAR file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4b4-116">-DefaultProfile</span></span>
<span data-ttu-id="cd4b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd4b4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd4b4-118">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="cd4b4-118">-Defines</span></span>
<span data-ttu-id="cd4b4-119">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-120">-Files</span><span class="sxs-lookup"><span data-stu-id="cd4b4-120">-Files</span></span>
<span data-ttu-id="cd4b4-121">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="cd4b4-122">-JarFile</span></span>
<span data-ttu-id="cd4b4-123">Określa plik JAR, który ma być używany jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-123">Specifies the JAR file to use for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="cd4b4-124">-JobName</span></span>
<span data-ttu-id="cd4b4-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="cd4b4-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="cd4b4-126">-LibJars</span></span>
<span data-ttu-id="cd4b4-127">Określa słoiki biblioteki dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-127">Specifies the lib JARS for the job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b4-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cd4b4-128">-StatusFolder</span></span>
<span data-ttu-id="cd4b4-129">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cd4b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4b4-130">CommonParameters</span></span>
<span data-ttu-id="cd4b4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4b4-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4b4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4b4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4b4-133">INPUTS</span></span>

### <span data-ttu-id="cd4b4-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd4b4-134">None</span></span>

## <span data-ttu-id="cd4b4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd4b4-135">OUTPUTS</span></span>

### <span data-ttu-id="cd4b4-136">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cd4b4-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="cd4b4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd4b4-137">NOTES</span></span>

## <span data-ttu-id="cd4b4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd4b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd4b4-139">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cd4b4-139">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

