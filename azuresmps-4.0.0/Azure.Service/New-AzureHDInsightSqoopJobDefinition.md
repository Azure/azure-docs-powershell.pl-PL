---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054881"
---
# <span data-ttu-id="92745-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="92745-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92745-102">SYNOPSIS</span></span>
<span data-ttu-id="92745-103">Definiuje nowe zadanie Sqoop.</span><span class="sxs-lookup"><span data-stu-id="92745-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="92745-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92745-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92745-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92745-105">DESCRIPTION</span></span>
<span data-ttu-id="92745-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="92745-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="92745-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="92745-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="92745-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="92745-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="92745-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="92745-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="92745-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="92745-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="92745-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="92745-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="92745-112">Polecenie cmdlet **New-AzureHDInsightSqoopJobDefinition** tworzy zadanie Sqoop, które ma zostać uruchomione w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="92745-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="92745-113">Sqoop to narzędzie do przesyłania danych między klastrami usługi Hadoop a relacyjnymi bazami danych.</span><span class="sxs-lookup"><span data-stu-id="92745-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="92745-114">Za pomocą Sqoop można zaimportować dane z bazy danych programu SQL Server do rozproszonego systemu plików HDFS (Hadoop File System), przekształcić dane za pomocą usługi Hadoop MapReduce, a następnie wyeksportować dane z pliku HDFS z powrotem do bazy danych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92745-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="92745-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92745-115">EXAMPLES</span></span>

### <span data-ttu-id="92745-116">Przykład 1. Importowanie danych</span><span class="sxs-lookup"><span data-stu-id="92745-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="92745-117">To polecenie definiuje zadanie Sqoop, które importuje wszystkie wiersze w tabeli z bazy danych serwera AzureSQL do klastra usługi HDInsight, a następnie zapisuje definicję zadania w zmiennej $SqoopJobDef.</span><span class="sxs-lookup"><span data-stu-id="92745-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="92745-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92745-118">PARAMETERS</span></span>

### <span data-ttu-id="92745-119">-Command</span><span class="sxs-lookup"><span data-stu-id="92745-119">-Command</span></span>
<span data-ttu-id="92745-120">Określa polecenie Sqoop i jego argumenty.</span><span class="sxs-lookup"><span data-stu-id="92745-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="92745-121">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="92745-121">-File</span></span>
<span data-ttu-id="92745-122">Określa ścieżkę do pliku skryptu, który zawiera polecenia do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="92745-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="92745-123">Plik skryptu musi znajdować się w witrynie WASB.</span><span class="sxs-lookup"><span data-stu-id="92745-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="92745-124">-Files</span><span class="sxs-lookup"><span data-stu-id="92745-124">-Files</span></span>
<span data-ttu-id="92745-125">Określa kolekcję plików WASB wymaganych dla zadania.</span><span class="sxs-lookup"><span data-stu-id="92745-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="92745-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="92745-126">-Profile</span></span>
<span data-ttu-id="92745-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92745-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92745-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="92745-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92745-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="92745-129">-StatusFolder</span></span>
<span data-ttu-id="92745-130">Określa lokalizację folderu zawierającego wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="92745-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="92745-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92745-131">CommonParameters</span></span>
<span data-ttu-id="92745-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92745-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92745-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92745-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92745-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92745-134">INPUTS</span></span>

## <span data-ttu-id="92745-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92745-135">OUTPUTS</span></span>

## <span data-ttu-id="92745-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92745-136">NOTES</span></span>

## <span data-ttu-id="92745-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92745-137">RELATED LINKS</span></span>

[<span data-ttu-id="92745-138">Nowe — AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="92745-139">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="92745-140">Nowe — AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="92745-141">Nowe — AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


