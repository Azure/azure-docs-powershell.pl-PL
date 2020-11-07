---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: f51545cc28a11984c55fa05b6760b71a055de7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705318"
---
# <span data-ttu-id="cddac-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="cddac-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="cddac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cddac-102">SYNOPSIS</span></span>
<span data-ttu-id="cddac-103">Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="cddac-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="cddac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cddac-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cddac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cddac-105">DESCRIPTION</span></span>
<span data-ttu-id="cddac-106">Polecenie cmdlet **Invoke-AzHDInsightHiveJob** przesyła zapytanie o aplikację Hive do klastra usługi Azure HDInsight i pobiera wyniki zapytania w jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="cddac-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="cddac-107">Przed wywołaniem funkcji **Invoke-AzHDInsightHiveJob** Użyj polecenia cmdlet Use-AzHDInsightCluster, aby określić klaster, który będzie używany dla kwerendy.</span><span class="sxs-lookup"><span data-stu-id="cddac-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="cddac-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cddac-108">EXAMPLES</span></span>

### <span data-ttu-id="cddac-109">Przykład 1: przesyłanie zapytania Hive do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="cddac-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="cddac-110">To polecenie przesyła kwerendy do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="cddac-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cddac-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cddac-111">PARAMETERS</span></span>

### <span data-ttu-id="cddac-112">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="cddac-112">-Arguments</span></span>
<span data-ttu-id="cddac-113">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cddac-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cddac-114">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="cddac-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="cddac-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="cddac-115">-DefaultContainer</span></span>
<span data-ttu-id="cddac-116">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure używanym przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cddac-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="cddac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddac-117">-DefaultProfile</span></span>
<span data-ttu-id="cddac-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cddac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cddac-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cddac-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="cddac-120">Określa klucz konta dla domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cddac-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="cddac-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cddac-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="cddac-122">Określa nazwę domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cddac-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="cddac-123">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="cddac-123">-Defines</span></span>
<span data-ttu-id="cddac-124">Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="cddac-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="cddac-125">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="cddac-125">-File</span></span>
<span data-ttu-id="cddac-126">Określa ścieżkę do pliku w usłudze Azure Storage, który zawiera zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="cddac-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="cddac-127">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="cddac-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="cddac-128">-Files</span><span class="sxs-lookup"><span data-stu-id="cddac-128">-Files</span></span>
<span data-ttu-id="cddac-129">Określa zbiór plików wymaganych dla zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="cddac-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="cddac-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="cddac-130">-JobName</span></span>
<span data-ttu-id="cddac-131">Określa nazwę zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="cddac-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="cddac-132">Jeśli ten parametr nie jest określony, w tym poleceniu cmdlet jest używana wartość domyślna: "gałąź: \< pierwsze 100 znaków zapytania \> ".</span><span class="sxs-lookup"><span data-stu-id="cddac-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="cddac-133">-Query</span><span class="sxs-lookup"><span data-stu-id="cddac-133">-Query</span></span>
<span data-ttu-id="cddac-134">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="cddac-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="cddac-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="cddac-135">-RunAsFileJob</span></span>
<span data-ttu-id="cddac-136">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="cddac-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="cddac-137">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="cddac-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="cddac-138">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="cddac-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddac-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cddac-139">-StatusFolder</span></span>
<span data-ttu-id="cddac-140">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cddac-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cddac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddac-141">CommonParameters</span></span>
<span data-ttu-id="cddac-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddac-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddac-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddac-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cddac-144">INPUTS</span></span>

### <span data-ttu-id="cddac-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cddac-145">None</span></span>

## <span data-ttu-id="cddac-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cddac-146">OUTPUTS</span></span>

### <span data-ttu-id="cddac-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cddac-147">System.String</span></span>

## <span data-ttu-id="cddac-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cddac-148">NOTES</span></span>

## <span data-ttu-id="cddac-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cddac-149">RELATED LINKS</span></span>

[<span data-ttu-id="cddac-150">Użyj — AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cddac-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


