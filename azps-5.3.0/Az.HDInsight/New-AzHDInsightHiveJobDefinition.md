---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4cf45d237d5611d5d9fb0fb1eb178d2c85807354
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489602"
---
# <span data-ttu-id="9a864-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9a864-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="9a864-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a864-102">SYNOPSIS</span></span>
<span data-ttu-id="9a864-103">Tworzy obiekt zadania w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="9a864-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="9a864-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a864-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a864-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a864-105">DESCRIPTION</span></span>
<span data-ttu-id="9a864-106">Polecenie cmdlet **New-AzHDInsightHiveJobDefinition** definiuje obiekt zadania Hive do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9a864-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9a864-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a864-107">EXAMPLES</span></span>

### <span data-ttu-id="9a864-108">Przykład 1: Tworzenie definicji zadania w gałęzi</span><span class="sxs-lookup"><span data-stu-id="9a864-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="9a864-109">To polecenie tworzy definicję zadania w gałęzi.</span><span class="sxs-lookup"><span data-stu-id="9a864-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="9a864-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a864-110">PARAMETERS</span></span>

### <span data-ttu-id="9a864-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="9a864-111">-Arguments</span></span>
<span data-ttu-id="9a864-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="9a864-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="9a864-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="9a864-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="9a864-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a864-114">-DefaultProfile</span></span>
<span data-ttu-id="9a864-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9a864-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a864-116">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="9a864-116">-Defines</span></span>
<span data-ttu-id="9a864-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="9a864-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="9a864-118">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="9a864-118">-File</span></span>
<span data-ttu-id="9a864-119">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a864-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="9a864-120">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="9a864-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="9a864-121">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="9a864-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="9a864-122">-Files</span><span class="sxs-lookup"><span data-stu-id="9a864-122">-Files</span></span>
<span data-ttu-id="9a864-123">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="9a864-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="9a864-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="9a864-124">-JobName</span></span>
<span data-ttu-id="9a864-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="9a864-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="9a864-126">-Query</span><span class="sxs-lookup"><span data-stu-id="9a864-126">-Query</span></span>
<span data-ttu-id="9a864-127">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="9a864-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="9a864-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="9a864-128">-RunAsFileJob</span></span>
<span data-ttu-id="9a864-129">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="9a864-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="9a864-130">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="9a864-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="9a864-131">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="9a864-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="9a864-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9a864-132">-StatusFolder</span></span>
<span data-ttu-id="9a864-133">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="9a864-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="9a864-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a864-134">CommonParameters</span></span>
<span data-ttu-id="9a864-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a864-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a864-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a864-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a864-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a864-137">INPUTS</span></span>

### <span data-ttu-id="9a864-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9a864-138">None</span></span>

## <span data-ttu-id="9a864-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a864-139">OUTPUTS</span></span>

### <span data-ttu-id="9a864-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9a864-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="9a864-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a864-141">NOTES</span></span>

## <span data-ttu-id="9a864-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a864-142">RELATED LINKS</span></span>

[<span data-ttu-id="9a864-143">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9a864-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


