---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055214"
---
# <span data-ttu-id="fb7af-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="fb7af-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="fb7af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb7af-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7af-103">Przesyła zapytania dotyczące gałęzi do klastra usługi HDInsight, pokazuje postęp wykonywania zapytań i pobiera wyniki zapytania w jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="fb7af-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="fb7af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb7af-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fb7af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb7af-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7af-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="fb7af-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="fb7af-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="fb7af-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="fb7af-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb7af-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="fb7af-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="fb7af-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="fb7af-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="fb7af-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="fb7af-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fb7af-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="fb7af-112">Polecenie cmdlet **Invoke-AzureHDInsightHiveJob** powoduje przesłanie zapytań dotyczących gałęzi do klastra usługi HDInsight, wyświetlenie postępu wykonywania zapytań i przyciąganie wyników zapytania w ramach jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="fb7af-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="fb7af-113">Przed uruchomieniem polecenia **Invoke-AzureHDInsightHiveJob** należy uruchomić polecenie cmdlet Use-AzureHDInsightCluster, aby określić klaster usługi HDInsight, do którego ma zostać przesłane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="fb7af-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="fb7af-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb7af-114">EXAMPLES</span></span>

### <span data-ttu-id="fb7af-115">Przykład 1: przesyłanie zapytania dotyczącego gałęzi</span><span class="sxs-lookup"><span data-stu-id="fb7af-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="fb7af-116">W pierwszym poleceniu użyto polecenia cmdlet **use-AzureHDInsightCluster** w celu określenia klastra w bieżącej subskrypcji, który będzie używany dla kwerendy w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="fb7af-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="fb7af-117">W drugim poleceniu zostanie użyte polecenie cmdlet **Invoke-AzureHDInsightHiveJob** w celu przesłania zapytania dotyczącego gałęzi.</span><span class="sxs-lookup"><span data-stu-id="fb7af-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="fb7af-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb7af-118">PARAMETERS</span></span>

### <span data-ttu-id="fb7af-119">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="fb7af-119">-Arguments</span></span>
<span data-ttu-id="fb7af-120">Określa tablicę argumentów dla zadania usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="fb7af-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="fb7af-121">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="fb7af-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="fb7af-122">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="fb7af-122">-Defines</span></span>
<span data-ttu-id="fb7af-123">Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="fb7af-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="fb7af-124">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="fb7af-124">-File</span></span>
<span data-ttu-id="fb7af-125">Określa ścieżkę obiektu BLOB (WASB) usługi Windows Azure do pliku w magazynie obiektów blob platformy Azure, który zawiera zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="fb7af-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="fb7af-126">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="fb7af-126">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="fb7af-127">-Files</span><span class="sxs-lookup"><span data-stu-id="fb7af-127">-Files</span></span>
<span data-ttu-id="fb7af-128">Określa zbiór plików wymaganych dla zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="fb7af-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="fb7af-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="fb7af-129">-JobName</span></span>
<span data-ttu-id="fb7af-130">Określa nazwę zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="fb7af-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="fb7af-131">Jeśli ten parametr nie jest określony, w tym poleceniu cmdlet jest używana wartość domyślna: "gałąź: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="fb7af-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="fb7af-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="fb7af-132">-Profile</span></span>
<span data-ttu-id="fb7af-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7af-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb7af-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fb7af-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb7af-135">-Query</span><span class="sxs-lookup"><span data-stu-id="fb7af-135">-Query</span></span>
<span data-ttu-id="fb7af-136">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="fb7af-136">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="fb7af-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="fb7af-137">-RunAsFileJob</span></span>
<span data-ttu-id="fb7af-138">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="fb7af-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="fb7af-139">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="fb7af-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="fb7af-140">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="fb7af-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="fb7af-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="fb7af-141">-StatusFolder</span></span>
<span data-ttu-id="fb7af-142">Określa lokalizację folderu zawierającego wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="fb7af-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="fb7af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7af-143">CommonParameters</span></span>
<span data-ttu-id="fb7af-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7af-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7af-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7af-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7af-146">INPUTS</span></span>

## <span data-ttu-id="fb7af-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb7af-147">OUTPUTS</span></span>

## <span data-ttu-id="fb7af-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb7af-148">NOTES</span></span>

## <span data-ttu-id="fb7af-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7af-149">RELATED LINKS</span></span>

[<span data-ttu-id="fb7af-150">Nowe — AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fb7af-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="fb7af-151">Użyj — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fb7af-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


