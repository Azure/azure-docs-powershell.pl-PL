---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553319"
---
# <span data-ttu-id="5ef18-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5ef18-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="5ef18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ef18-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef18-103">Tworzy obiekt zadania przesyłania strumieniowego MapReduce.</span><span class="sxs-lookup"><span data-stu-id="5ef18-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ef18-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ef18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ef18-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef18-106">Polecenie cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definiuje strumień strumieniowy obiektu zadania MapReduce, który ma być używany w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5ef18-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5ef18-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ef18-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef18-108">Przykład 1: Tworzenie definicji zadania MapReduce strumieniowego</span><span class="sxs-lookup"><span data-stu-id="5ef18-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="5ef18-109">To polecenie tworzy definicję zadania MapReduce strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="5ef18-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="5ef18-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ef18-110">PARAMETERS</span></span>

### <span data-ttu-id="5ef18-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="5ef18-111">-Arguments</span></span>
<span data-ttu-id="5ef18-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="5ef18-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="5ef18-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="5ef18-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="5ef18-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ef18-114">-CommandEnvironment</span></span>
<span data-ttu-id="5ef18-115">Określa tablicę zmiennych środowiskowych wiersza polecenia do ustawiania czasu uruchamiania zadania w węzłach procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="5ef18-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="5ef18-116">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="5ef18-116">-Defines</span></span>
<span data-ttu-id="5ef18-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="5ef18-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="5ef18-118">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="5ef18-118">-File</span></span>
<span data-ttu-id="5ef18-119">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ef18-119">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="5ef18-120">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="5ef18-120">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="5ef18-121">-Files</span><span class="sxs-lookup"><span data-stu-id="5ef18-121">-Files</span></span>
<span data-ttu-id="5ef18-122">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="5ef18-122">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="5ef18-123">-InputPath</span><span class="sxs-lookup"><span data-stu-id="5ef18-123">-InputPath</span></span>
<span data-ttu-id="5ef18-124">Określa ścieżkę do plików wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5ef18-124">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="5ef18-125">-Maper</span><span class="sxs-lookup"><span data-stu-id="5ef18-125">-Mapper</span></span>
<span data-ttu-id="5ef18-126">Określa nazwę pliku mapera.</span><span class="sxs-lookup"><span data-stu-id="5ef18-126">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="5ef18-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="5ef18-127">-OutputPath</span></span>
<span data-ttu-id="5ef18-128">Określa ścieżkę dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="5ef18-128">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="5ef18-129">-Zmniejszenie</span><span class="sxs-lookup"><span data-stu-id="5ef18-129">-Reducer</span></span>
<span data-ttu-id="5ef18-130">Określa nazwę pliku z ograniczeniami.</span><span class="sxs-lookup"><span data-stu-id="5ef18-130">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="5ef18-131">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="5ef18-131">-StatusFolder</span></span>
<span data-ttu-id="5ef18-132">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="5ef18-132">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="5ef18-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef18-133">-DefaultProfile</span></span>
<span data-ttu-id="5ef18-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef18-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef18-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef18-135">CommonParameters</span></span>
<span data-ttu-id="5ef18-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef18-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef18-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef18-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef18-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ef18-138">INPUTS</span></span>

## <span data-ttu-id="5ef18-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ef18-139">OUTPUTS</span></span>

### <span data-ttu-id="5ef18-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5ef18-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="5ef18-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ef18-141">NOTES</span></span>

## <span data-ttu-id="5ef18-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ef18-142">RELATED LINKS</span></span>

[<span data-ttu-id="5ef18-143">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ef18-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


