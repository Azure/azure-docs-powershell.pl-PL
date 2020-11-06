---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: f74d0e56265e5b976de9cf289f3b6a4900b76d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545724"
---
# <span data-ttu-id="cf1b4-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cf1b4-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="cf1b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1b4-103">Tworzy obiekt zadania przesyłania strumieniowego MapReduce.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf1b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf1b4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf1b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf1b4-105">DESCRIPTION</span></span>
<span data-ttu-id="cf1b4-106">Polecenie cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definiuje strumień strumieniowy obiektu zadania MapReduce, który ma być używany w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cf1b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf1b4-107">EXAMPLES</span></span>

### <span data-ttu-id="cf1b4-108">Przykład 1: Tworzenie definicji zadania MapReduce strumieniowego</span><span class="sxs-lookup"><span data-stu-id="cf1b4-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cf1b4-109">To polecenie tworzy definicję zadania MapReduce strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="cf1b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf1b4-110">PARAMETERS</span></span>

### <span data-ttu-id="cf1b4-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="cf1b4-111">-Arguments</span></span>
<span data-ttu-id="cf1b4-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cf1b4-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b4-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="cf1b4-114">-CommandEnvironment</span></span>
<span data-ttu-id="cf1b4-115">Określa tablicę zmiennych środowiskowych wiersza polecenia do ustawiania czasu uruchamiania zadania w węzłach procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1b4-116">-DefaultProfile</span></span>
<span data-ttu-id="cf1b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cf1b4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf1b4-118">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="cf1b4-118">-Defines</span></span>
<span data-ttu-id="cf1b4-119">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b4-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="cf1b4-120">-File</span></span>
<span data-ttu-id="cf1b4-121">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="cf1b4-122">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="cf1b4-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="cf1b4-123">-Files</span><span class="sxs-lookup"><span data-stu-id="cf1b4-123">-Files</span></span>
<span data-ttu-id="cf1b4-124">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-124">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b4-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="cf1b4-125">-InputPath</span></span>
<span data-ttu-id="cf1b4-126">Określa ścieżkę do plików wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-126">Specifies the path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b4-127">-Maper</span><span class="sxs-lookup"><span data-stu-id="cf1b4-127">-Mapper</span></span>
<span data-ttu-id="cf1b4-128">Określa nazwę pliku mapera.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="cf1b4-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="cf1b4-129">-OutputPath</span></span>
<span data-ttu-id="cf1b4-130">Określa ścieżkę dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="cf1b4-131">-Zmniejszenie</span><span class="sxs-lookup"><span data-stu-id="cf1b4-131">-Reducer</span></span>
<span data-ttu-id="cf1b4-132">Określa nazwę pliku z ograniczeniami.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="cf1b4-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cf1b4-133">-StatusFolder</span></span>
<span data-ttu-id="cf1b4-134">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cf1b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1b4-135">CommonParameters</span></span>
<span data-ttu-id="cf1b4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1b4-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1b4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1b4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf1b4-138">INPUTS</span></span>

### <span data-ttu-id="cf1b4-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cf1b4-139">None</span></span>
<span data-ttu-id="cf1b4-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cf1b4-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf1b4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf1b4-141">OUTPUTS</span></span>

### <span data-ttu-id="cf1b4-142">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cf1b4-142">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="cf1b4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf1b4-143">NOTES</span></span>

## <span data-ttu-id="cf1b4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf1b4-144">RELATED LINKS</span></span>

[<span data-ttu-id="cf1b4-145">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf1b4-145">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


