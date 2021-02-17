---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 737ccdbd742b3c4cc12518262423e846678cf599
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188347"
---
# <span data-ttu-id="db6a5-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="db6a5-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="db6a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="db6a5-103">Przesyła zapytanie Do klastra HDInsight i pobiera wyniki zapytania w jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="db6a5-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="db6a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db6a5-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6a5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="db6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="db6a5-106">Polecenie cmdlet **Invoke-AzHDInsightHiveJob** przesyła zapytanie w usłudze Azure HDInsight i pobiera wyniki zapytania w ramach jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="db6a5-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="db6a5-107">Użyj Use-AzHDInsightCluster cmdlet przed wywołaniem **invoke-AzHDInsightHiveJob,** aby określić klaster, który będzie używany dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="db6a5-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="db6a5-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db6a5-108">EXAMPLES</span></span>

### <span data-ttu-id="db6a5-109">Przykład 1. Przesyłanie zapytania w usłudze Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="db6a5-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
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
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="db6a5-110">To polecenie przesyła zapytanie SHOW TABLES do klastra o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="db6a5-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="db6a5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6a5-111">PARAMETERS</span></span>

### <span data-ttu-id="db6a5-112">— Argumenty</span><span class="sxs-lookup"><span data-stu-id="db6a5-112">-Arguments</span></span>
<span data-ttu-id="db6a5-113">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="db6a5-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="db6a5-114">Argumenty są przekazywane jako argumenty wiersza polecenia do każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="db6a5-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="db6a5-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="db6a5-115">-DefaultContainer</span></span>
<span data-ttu-id="db6a5-116">Określa nazwę domyślnego kontenera na domyślnym koncie magazynu platformy Azure używanym przez klaster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db6a5-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="db6a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6a5-117">-DefaultProfile</span></span>
<span data-ttu-id="db6a5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="db6a5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db6a5-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="db6a5-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="db6a5-120">Określa klucz konta dla domyślnego konta magazynu używanego przez klaster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db6a5-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="db6a5-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db6a5-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="db6a5-122">Określa nazwę domyślnego konta magazynu używanego przez klaster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db6a5-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="db6a5-123">— definiuje</span><span class="sxs-lookup"><span data-stu-id="db6a5-123">-Defines</span></span>
<span data-ttu-id="db6a5-124">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas pracy zadania.</span><span class="sxs-lookup"><span data-stu-id="db6a5-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="db6a5-125">— Plik</span><span class="sxs-lookup"><span data-stu-id="db6a5-125">-File</span></span>
<span data-ttu-id="db6a5-126">Określa ścieżkę do pliku w magazynie platformy Azure zawierającego zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="db6a5-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="db6a5-127">Możesz użyć tego parametru zamiast *parametru Query.*</span><span class="sxs-lookup"><span data-stu-id="db6a5-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="db6a5-128">— Pliki</span><span class="sxs-lookup"><span data-stu-id="db6a5-128">-Files</span></span>
<span data-ttu-id="db6a5-129">Określa zbiór plików wymaganych dla zadania Gałąź.</span><span class="sxs-lookup"><span data-stu-id="db6a5-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="db6a5-130">— JobName</span><span class="sxs-lookup"><span data-stu-id="db6a5-130">-JobName</span></span>
<span data-ttu-id="db6a5-131">Określa nazwę zadania Gałąź.</span><span class="sxs-lookup"><span data-stu-id="db6a5-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="db6a5-132">Jeśli nie określisz tego parametru, to polecenie cmdlet użyje wartości domyślnej: "Gałąź: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="db6a5-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="db6a5-133">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="db6a5-133">-Query</span></span>
<span data-ttu-id="db6a5-134">Określa zapytanie Ułana.</span><span class="sxs-lookup"><span data-stu-id="db6a5-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="db6a5-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="db6a5-135">-RunAsFileJob</span></span>
<span data-ttu-id="db6a5-136">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie magazynu platformy Azure, na którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="db6a5-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="db6a5-137">To polecenie cmdlet przesyła zadanie, które odwołuje się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="db6a5-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="db6a5-138">Ta funkcja umożliwia obsługę znaków specjalnych, takich jak znak procentu (%) oznaczałoby niepowodzenie przesłania zadania za pośrednictwem Templetona, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="db6a5-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="db6a5-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="db6a5-139">-StatusFolder</span></span>
<span data-ttu-id="db6a5-140">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="db6a5-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="db6a5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6a5-141">CommonParameters</span></span>
<span data-ttu-id="db6a5-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6a5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6a5-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db6a5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6a5-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db6a5-144">INPUTS</span></span>

### <span data-ttu-id="db6a5-145">Brak</span><span class="sxs-lookup"><span data-stu-id="db6a5-145">None</span></span>

## <span data-ttu-id="db6a5-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db6a5-146">OUTPUTS</span></span>

### <span data-ttu-id="db6a5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="db6a5-147">System.String</span></span>

## <span data-ttu-id="db6a5-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db6a5-148">NOTES</span></span>

## <span data-ttu-id="db6a5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db6a5-149">RELATED LINKS</span></span>

[<span data-ttu-id="db6a5-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="db6a5-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


