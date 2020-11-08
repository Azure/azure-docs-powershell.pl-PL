---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054976"
---
# <span data-ttu-id="d881f-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d881f-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="d881f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d881f-102">SYNOPSIS</span></span>
<span data-ttu-id="d881f-103">Definiuje nowe zadanie wieprzowe dla usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d881f-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="d881f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d881f-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d881f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d881f-105">DESCRIPTION</span></span>
<span data-ttu-id="d881f-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="d881f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d881f-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="d881f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d881f-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d881f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d881f-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d881f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d881f-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d881f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d881f-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d881f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d881f-112">**Nowe-AzureHDInsightPigJobDefinition** definiuje zadanie świni w usłudze HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="d881f-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="d881f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d881f-113">EXAMPLES</span></span>

### <span data-ttu-id="d881f-114">Przykład 1. Zdefiniuj nowe zadanie wieprzowe</span><span class="sxs-lookup"><span data-stu-id="d881f-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="d881f-115">Pierwsze polecenie deklaruje wartość ciągu, a następnie przechowuje zmienną $0.</span><span class="sxs-lookup"><span data-stu-id="d881f-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="d881f-116">Drugie polecenie tworzy kwerendę dotyczącą zadania wieprzowego, a następnie zapisuje ją w zmiennej $QueryString.</span><span class="sxs-lookup"><span data-stu-id="d881f-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="d881f-117">Ostatnie polecenie tworzy definicję zadania wieprzowego korzystającą z zapytania w $QueryString, a następnie zapisuje definicję zadania w zmiennej $PigJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="d881f-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="d881f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d881f-118">PARAMETERS</span></span>

### <span data-ttu-id="d881f-119">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="d881f-119">-Arguments</span></span>
<span data-ttu-id="d881f-120">Określa tablicę argumentów dla zadania w ramach świni.</span><span class="sxs-lookup"><span data-stu-id="d881f-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="d881f-121">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="d881f-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d881f-122">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="d881f-122">-File</span></span>
<span data-ttu-id="d881f-123">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d881f-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="d881f-124">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="d881f-124">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d881f-125">-Files</span><span class="sxs-lookup"><span data-stu-id="d881f-125">-Files</span></span>
<span data-ttu-id="d881f-126">Określa zbiór plików skojarzonych z zadaniem w ramach świni.</span><span class="sxs-lookup"><span data-stu-id="d881f-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="d881f-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="d881f-127">-Profile</span></span>
<span data-ttu-id="d881f-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d881f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d881f-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d881f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d881f-130">-Query</span><span class="sxs-lookup"><span data-stu-id="d881f-130">-Query</span></span>
<span data-ttu-id="d881f-131">Określa zapytanie o pracę z świnią.</span><span class="sxs-lookup"><span data-stu-id="d881f-131">Specifies a Pig job query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d881f-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d881f-132">-StatusFolder</span></span>
<span data-ttu-id="d881f-133">Określa lokalizację folderu zawierającego wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="d881f-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="d881f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d881f-134">CommonParameters</span></span>
<span data-ttu-id="d881f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d881f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d881f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d881f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d881f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d881f-137">INPUTS</span></span>

## <span data-ttu-id="d881f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d881f-138">OUTPUTS</span></span>

## <span data-ttu-id="d881f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d881f-139">NOTES</span></span>

## <span data-ttu-id="d881f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d881f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d881f-141">Nowe — AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d881f-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d881f-142">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d881f-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="d881f-143">Nowe — AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d881f-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="d881f-144">Nowe — AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d881f-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


