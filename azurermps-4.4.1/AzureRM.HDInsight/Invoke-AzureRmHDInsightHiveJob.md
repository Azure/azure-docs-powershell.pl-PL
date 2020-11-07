---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553886"
---
# <span data-ttu-id="23efb-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="23efb-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="23efb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23efb-102">SYNOPSIS</span></span>
<span data-ttu-id="23efb-103">Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="23efb-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23efb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23efb-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23efb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23efb-105">DESCRIPTION</span></span>
<span data-ttu-id="23efb-106">Polecenie cmdlet **Invoke-AzureRmHDInsightHiveJob** przesyła zapytanie o aplikację Hive do klastra usługi Azure HDInsight i pobiera wyniki zapytania w jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="23efb-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="23efb-107">Przed wywołaniem funkcji **Invoke-AzureRmHDInsightHiveJob** Użyj polecenia cmdlet Use-AzureRmHDInsightCluster, aby określić klaster, który będzie używany dla kwerendy.</span><span class="sxs-lookup"><span data-stu-id="23efb-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="23efb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23efb-108">EXAMPLES</span></span>

### <span data-ttu-id="23efb-109">Przykład 1: przesyłanie zapytania Hive do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="23efb-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="23efb-110">To polecenie przesyła kwerendy do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="23efb-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="23efb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23efb-111">PARAMETERS</span></span>

### <span data-ttu-id="23efb-112">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="23efb-112">-Arguments</span></span>
<span data-ttu-id="23efb-113">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="23efb-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="23efb-114">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="23efb-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="23efb-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="23efb-115">-DefaultContainer</span></span>
<span data-ttu-id="23efb-116">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure używanym przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23efb-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="23efb-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23efb-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="23efb-118">Określa klucz konta dla domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23efb-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="23efb-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23efb-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="23efb-120">Określa nazwę domyślnego konta magazynu używanego przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23efb-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="23efb-121">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="23efb-121">-Defines</span></span>
<span data-ttu-id="23efb-122">Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="23efb-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="23efb-123">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="23efb-123">-File</span></span>
<span data-ttu-id="23efb-124">Określa ścieżkę do pliku w usłudze Azure Storage, który zawiera zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="23efb-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="23efb-125">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="23efb-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="23efb-126">-Files</span><span class="sxs-lookup"><span data-stu-id="23efb-126">-Files</span></span>
<span data-ttu-id="23efb-127">Określa zbiór plików wymaganych dla zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="23efb-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="23efb-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="23efb-128">-JobName</span></span>
<span data-ttu-id="23efb-129">Określa nazwę zadania w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="23efb-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="23efb-130">Jeśli ten parametr nie jest określony, w tym poleceniu cmdlet jest używana wartość domyślna: "gałąź: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="23efb-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="23efb-131">-Query</span><span class="sxs-lookup"><span data-stu-id="23efb-131">-Query</span></span>
<span data-ttu-id="23efb-132">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="23efb-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="23efb-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="23efb-133">-RunAsFileJob</span></span>
<span data-ttu-id="23efb-134">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="23efb-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="23efb-135">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="23efb-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="23efb-136">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="23efb-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="23efb-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="23efb-137">-StatusFolder</span></span>
<span data-ttu-id="23efb-138">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="23efb-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="23efb-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23efb-139">-DefaultProfile</span></span>
<span data-ttu-id="23efb-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23efb-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23efb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23efb-141">CommonParameters</span></span>
<span data-ttu-id="23efb-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23efb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23efb-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23efb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23efb-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23efb-144">INPUTS</span></span>

## <span data-ttu-id="23efb-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23efb-145">OUTPUTS</span></span>

### <span data-ttu-id="23efb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="23efb-146">System.String</span></span>

## <span data-ttu-id="23efb-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23efb-147">NOTES</span></span>

## <span data-ttu-id="23efb-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23efb-148">RELATED LINKS</span></span>

[<span data-ttu-id="23efb-149">Użyj — AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="23efb-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)

