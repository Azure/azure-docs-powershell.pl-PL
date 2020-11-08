---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063529"
---
# <span data-ttu-id="e4ea7-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4ea7-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e4ea7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ea7-103">Tworzy obiekt zadania przesyłania strumieniowego MapReduce.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="e4ea7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4ea7-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4ea7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ea7-106">Polecenie cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** definiuje strumień strumieniowy obiektu zadania MapReduce, który ma być używany w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e4ea7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ea7-108">Przykład 1: Tworzenie definicji zadania MapReduce strumieniowego</span><span class="sxs-lookup"><span data-stu-id="e4ea7-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="e4ea7-109">To polecenie tworzy definicję zadania MapReduce strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="e4ea7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="e4ea7-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="e4ea7-111">-Arguments</span></span>
<span data-ttu-id="e4ea7-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e4ea7-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e4ea7-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="e4ea7-114">-CommandEnvironment</span></span>
<span data-ttu-id="e4ea7-115">Określa tablicę zmiennych środowiskowych wiersza polecenia do ustawiania czasu uruchamiania zadania w węzłach procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="e4ea7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ea7-116">-DefaultProfile</span></span>
<span data-ttu-id="e4ea7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4ea7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4ea7-118">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="e4ea7-118">-Defines</span></span>
<span data-ttu-id="e4ea7-119">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e4ea7-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="e4ea7-120">-File</span></span>
<span data-ttu-id="e4ea7-121">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="e4ea7-122">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="e4ea7-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="e4ea7-123">-Files</span><span class="sxs-lookup"><span data-stu-id="e4ea7-123">-Files</span></span>
<span data-ttu-id="e4ea7-124">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e4ea7-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="e4ea7-125">-InputPath</span></span>
<span data-ttu-id="e4ea7-126">Określa ścieżkę do plików wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="e4ea7-127">-Maper</span><span class="sxs-lookup"><span data-stu-id="e4ea7-127">-Mapper</span></span>
<span data-ttu-id="e4ea7-128">Określa nazwę pliku mapera.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="e4ea7-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e4ea7-129">-OutputPath</span></span>
<span data-ttu-id="e4ea7-130">Określa ścieżkę dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="e4ea7-131">-Zmniejszenie</span><span class="sxs-lookup"><span data-stu-id="e4ea7-131">-Reducer</span></span>
<span data-ttu-id="e4ea7-132">Określa nazwę pliku z ograniczeniami.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="e4ea7-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e4ea7-133">-StatusFolder</span></span>
<span data-ttu-id="e4ea7-134">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e4ea7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ea7-135">CommonParameters</span></span>
<span data-ttu-id="e4ea7-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ea7-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ea7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ea7-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4ea7-138">INPUTS</span></span>

### <span data-ttu-id="e4ea7-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e4ea7-139">None</span></span>

## <span data-ttu-id="e4ea7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4ea7-140">OUTPUTS</span></span>

### <span data-ttu-id="e4ea7-141">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4ea7-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e4ea7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4ea7-142">NOTES</span></span>

## <span data-ttu-id="e4ea7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4ea7-143">RELATED LINKS</span></span>

[<span data-ttu-id="e4ea7-144">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4ea7-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


