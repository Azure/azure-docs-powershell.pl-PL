---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 60e0f8e6799a89d673b3c9ca7de7827b197440fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959633"
---
# <span data-ttu-id="11f72-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11f72-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="11f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f72-102">SYNOPSIS</span></span>
<span data-ttu-id="11f72-103">Tworzy obiekt zadania MapReduce przesyłania strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="11f72-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="11f72-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11f72-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11f72-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11f72-105">DESCRIPTION</span></span>
<span data-ttu-id="11f72-106">Polecenie cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** definiuje obiekt zadania Streaming MapReduce do użytku z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="11f72-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="11f72-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11f72-107">EXAMPLES</span></span>

### <span data-ttu-id="11f72-108">Przykład 1. Tworzenie definicji zadania przesyłania strumieniowego MapReduce</span><span class="sxs-lookup"><span data-stu-id="11f72-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="11f72-109">To polecenie tworzy definicję zadania przesyłania strumieniowego MapReduce.</span><span class="sxs-lookup"><span data-stu-id="11f72-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="11f72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11f72-110">PARAMETERS</span></span>

### <span data-ttu-id="11f72-111">— Argumenty</span><span class="sxs-lookup"><span data-stu-id="11f72-111">-Arguments</span></span>
<span data-ttu-id="11f72-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="11f72-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="11f72-113">Argumenty są przekazywane do każdego zadania jako argumenty wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="11f72-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="11f72-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="11f72-114">-CommandEnvironment</span></span>
<span data-ttu-id="11f72-115">Określa tablicę zmiennych środowiska wiersza polecenia, które mają być ustawiane podczas pracy w węzłach pracowników.</span><span class="sxs-lookup"><span data-stu-id="11f72-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="11f72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f72-116">-DefaultProfile</span></span>
<span data-ttu-id="11f72-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="11f72-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11f72-118">— definiuje</span><span class="sxs-lookup"><span data-stu-id="11f72-118">-Defines</span></span>
<span data-ttu-id="11f72-119">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas pracy zadania.</span><span class="sxs-lookup"><span data-stu-id="11f72-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="11f72-120">— Plik</span><span class="sxs-lookup"><span data-stu-id="11f72-120">-File</span></span>
<span data-ttu-id="11f72-121">Określa ścieżkę do pliku zawierającego zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="11f72-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="11f72-122">Możesz użyć tego parametru zamiast *parametru Query.*</span><span class="sxs-lookup"><span data-stu-id="11f72-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="11f72-123">— Pliki</span><span class="sxs-lookup"><span data-stu-id="11f72-123">-Files</span></span>
<span data-ttu-id="11f72-124">Określa zbiór plików skojarzonych z zadaniem Gałąź.</span><span class="sxs-lookup"><span data-stu-id="11f72-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="11f72-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="11f72-125">-InputPath</span></span>
<span data-ttu-id="11f72-126">Określa ścieżkę do plików wejściowych.</span><span class="sxs-lookup"><span data-stu-id="11f72-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="11f72-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="11f72-127">-Mapper</span></span>
<span data-ttu-id="11f72-128">Określa nazwę pliku mapera.</span><span class="sxs-lookup"><span data-stu-id="11f72-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="11f72-129">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="11f72-129">-OutputPath</span></span>
<span data-ttu-id="11f72-130">Określa ścieżkę dla wyniku zadania.</span><span class="sxs-lookup"><span data-stu-id="11f72-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="11f72-131">- Redufikator</span><span class="sxs-lookup"><span data-stu-id="11f72-131">-Reducer</span></span>
<span data-ttu-id="11f72-132">Określa nazwę pliku Redufikatora.</span><span class="sxs-lookup"><span data-stu-id="11f72-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="11f72-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="11f72-133">-StatusFolder</span></span>
<span data-ttu-id="11f72-134">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="11f72-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="11f72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f72-135">CommonParameters</span></span>
<span data-ttu-id="11f72-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f72-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11f72-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f72-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11f72-138">INPUTS</span></span>

### <span data-ttu-id="11f72-139">Brak</span><span class="sxs-lookup"><span data-stu-id="11f72-139">None</span></span>

## <span data-ttu-id="11f72-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11f72-140">OUTPUTS</span></span>

### <span data-ttu-id="11f72-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11f72-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="11f72-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11f72-142">NOTES</span></span>

## <span data-ttu-id="11f72-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11f72-143">RELATED LINKS</span></span>

[<span data-ttu-id="11f72-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11f72-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


