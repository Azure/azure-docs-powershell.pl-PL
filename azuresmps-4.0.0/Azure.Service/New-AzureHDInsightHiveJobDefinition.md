---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054883"
---
# <span data-ttu-id="fda4e-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fda4e-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="fda4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fda4e-102">SYNOPSIS</span></span>
<span data-ttu-id="fda4e-103">Definiuje nowe zadanie gałęzi dla usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fda4e-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="fda4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fda4e-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fda4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fda4e-105">DESCRIPTION</span></span>
<span data-ttu-id="fda4e-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="fda4e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="fda4e-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="fda4e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="fda4e-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fda4e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="fda4e-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="fda4e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="fda4e-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="fda4e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="fda4e-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fda4e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="fda4e-112">Polecenie cmdlet **New-AzureHDInsightHiveJobDefinition** definiuje zadanie gałęzi dla usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fda4e-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="fda4e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fda4e-113">EXAMPLES</span></span>

### <span data-ttu-id="fda4e-114">Przykład 1: Tworzenie definicji zadania w gałęzi</span><span class="sxs-lookup"><span data-stu-id="fda4e-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="fda4e-115">To polecenie tworzy definicję zadania usługi Hive używającą wstępnie zdefiniowanego ciągu kwerendy, a następnie zapisuje ją w zmiennej $HiveJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="fda4e-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="fda4e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fda4e-116">PARAMETERS</span></span>

### <span data-ttu-id="fda4e-117">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="fda4e-117">-Arguments</span></span>
<span data-ttu-id="fda4e-118">Określa tablicę argumentów dla zadania usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="fda4e-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="fda4e-119">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="fda4e-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="fda4e-120">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="fda4e-120">-Defines</span></span>
<span data-ttu-id="fda4e-121">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="fda4e-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda4e-122">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="fda4e-122">-File</span></span>
<span data-ttu-id="fda4e-123">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fda4e-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="fda4e-124">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="fda4e-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="fda4e-125">-Files</span><span class="sxs-lookup"><span data-stu-id="fda4e-125">-Files</span></span>
<span data-ttu-id="fda4e-126">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="fda4e-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="fda4e-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="fda4e-127">-JobName</span></span>
<span data-ttu-id="fda4e-128">Określa nazwę zadania usługi Hive do zdefiniowania.</span><span class="sxs-lookup"><span data-stu-id="fda4e-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="fda4e-129">Jeśli nie podano tego parametru, używana jest nazwa domyślna: "gałąź: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="fda4e-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda4e-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="fda4e-130">-Profile</span></span>
<span data-ttu-id="fda4e-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda4e-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fda4e-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fda4e-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fda4e-133">-Query</span><span class="sxs-lookup"><span data-stu-id="fda4e-133">-Query</span></span>
<span data-ttu-id="fda4e-134">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="fda4e-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="fda4e-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="fda4e-135">-RunAsFileJob</span></span>
<span data-ttu-id="fda4e-136">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="fda4e-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="fda4e-137">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="fda4e-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="fda4e-138">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="fda4e-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda4e-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="fda4e-139">-StatusFolder</span></span>
<span data-ttu-id="fda4e-140">Określa lokalizację folderu zawierającego wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="fda4e-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="fda4e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda4e-141">CommonParameters</span></span>
<span data-ttu-id="fda4e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda4e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda4e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda4e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda4e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fda4e-144">INPUTS</span></span>

## <span data-ttu-id="fda4e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fda4e-145">OUTPUTS</span></span>

## <span data-ttu-id="fda4e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fda4e-146">NOTES</span></span>

## <span data-ttu-id="fda4e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fda4e-147">RELATED LINKS</span></span>

[<span data-ttu-id="fda4e-148">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fda4e-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="fda4e-149">Nowe — AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fda4e-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="fda4e-150">Nowe — AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fda4e-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="fda4e-151">Nowe — AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fda4e-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


