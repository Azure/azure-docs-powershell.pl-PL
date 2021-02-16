---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4cf45d237d5611d5d9fb0fb1eb178d2c85807354
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200258"
---
# <span data-ttu-id="5a504-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5a504-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="5a504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a504-102">SYNOPSIS</span></span>
<span data-ttu-id="5a504-103">Tworzy obiekt zadania Gałąź.</span><span class="sxs-lookup"><span data-stu-id="5a504-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="5a504-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a504-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a504-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a504-105">DESCRIPTION</span></span>
<span data-ttu-id="5a504-106">Polecenie **cmdlet New-AzHDInsightHiveJobDefinition** definiuje obiekt zadania Gałąź do użytku z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5a504-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5a504-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a504-107">EXAMPLES</span></span>

### <span data-ttu-id="5a504-108">Przykład 1. Tworzenie definicji stanowiska</span><span class="sxs-lookup"><span data-stu-id="5a504-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="5a504-109">To polecenie tworzy definicję stanowiska Gałąź.</span><span class="sxs-lookup"><span data-stu-id="5a504-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="5a504-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a504-110">PARAMETERS</span></span>

### <span data-ttu-id="5a504-111">— Argumenty</span><span class="sxs-lookup"><span data-stu-id="5a504-111">-Arguments</span></span>
<span data-ttu-id="5a504-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="5a504-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="5a504-113">Argumenty są przekazywane jako argumenty wiersza polecenia do każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="5a504-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="5a504-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a504-114">-DefaultProfile</span></span>
<span data-ttu-id="5a504-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5a504-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a504-116">— definiuje</span><span class="sxs-lookup"><span data-stu-id="5a504-116">-Defines</span></span>
<span data-ttu-id="5a504-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas pracy zadania.</span><span class="sxs-lookup"><span data-stu-id="5a504-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="5a504-118">— Plik</span><span class="sxs-lookup"><span data-stu-id="5a504-118">-File</span></span>
<span data-ttu-id="5a504-119">Określa ścieżkę do pliku zawierającego zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="5a504-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="5a504-120">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="5a504-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="5a504-121">Możesz użyć tego parametru zamiast *parametru Query.*</span><span class="sxs-lookup"><span data-stu-id="5a504-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="5a504-122">— Pliki</span><span class="sxs-lookup"><span data-stu-id="5a504-122">-Files</span></span>
<span data-ttu-id="5a504-123">Określa zbiór plików skojarzonych z zadaniem Gałąź.</span><span class="sxs-lookup"><span data-stu-id="5a504-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="5a504-124">— JobName</span><span class="sxs-lookup"><span data-stu-id="5a504-124">-JobName</span></span>
<span data-ttu-id="5a504-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="5a504-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="5a504-126">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="5a504-126">-Query</span></span>
<span data-ttu-id="5a504-127">Określa zapytanie Ułana.</span><span class="sxs-lookup"><span data-stu-id="5a504-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="5a504-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="5a504-128">-RunAsFileJob</span></span>
<span data-ttu-id="5a504-129">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie magazynu platformy Azure, na którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="5a504-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="5a504-130">To polecenie cmdlet przesyła zadanie, które odwołuje się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="5a504-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="5a504-131">Ta funkcja umożliwia obsługę znaków specjalnych, takich jak znak procentu (%) oznaczałoby niepowodzenie przesłania zadania za pośrednictwem Templetona, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="5a504-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="5a504-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="5a504-132">-StatusFolder</span></span>
<span data-ttu-id="5a504-133">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="5a504-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="5a504-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a504-134">CommonParameters</span></span>
<span data-ttu-id="5a504-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a504-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a504-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a504-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a504-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a504-137">INPUTS</span></span>

### <span data-ttu-id="5a504-138">Brak</span><span class="sxs-lookup"><span data-stu-id="5a504-138">None</span></span>

## <span data-ttu-id="5a504-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a504-139">OUTPUTS</span></span>

### <span data-ttu-id="5a504-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5a504-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="5a504-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a504-141">NOTES</span></span>

## <span data-ttu-id="5a504-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a504-142">RELATED LINKS</span></span>

[<span data-ttu-id="5a504-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5a504-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


