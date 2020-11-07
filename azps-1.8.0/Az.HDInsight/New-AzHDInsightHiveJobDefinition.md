---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4d8a35498462cae6e218fc41365de89a897bb555
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868244"
---
# <span data-ttu-id="d0e71-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d0e71-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d0e71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0e71-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e71-103">Tworzy obiekt zadania w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="d0e71-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="d0e71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0e71-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e71-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0e71-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e71-106">Polecenie cmdlet **New-AzHDInsightHiveJobDefinition** definiuje obiekt zadania Hive do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d0e71-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d0e71-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0e71-107">EXAMPLES</span></span>

### <span data-ttu-id="d0e71-108">Przykład 1: Tworzenie definicji zadania w gałęzi</span><span class="sxs-lookup"><span data-stu-id="d0e71-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="d0e71-109">To polecenie tworzy definicję zadania w gałęzi.</span><span class="sxs-lookup"><span data-stu-id="d0e71-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="d0e71-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0e71-110">PARAMETERS</span></span>

### <span data-ttu-id="d0e71-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="d0e71-111">-Arguments</span></span>
<span data-ttu-id="d0e71-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="d0e71-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d0e71-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="d0e71-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d0e71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e71-114">-DefaultProfile</span></span>
<span data-ttu-id="d0e71-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0e71-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e71-116">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="d0e71-116">-Defines</span></span>
<span data-ttu-id="d0e71-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="d0e71-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="d0e71-118">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="d0e71-118">-File</span></span>
<span data-ttu-id="d0e71-119">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0e71-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="d0e71-120">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="d0e71-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="d0e71-121">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="d0e71-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="d0e71-122">-Files</span><span class="sxs-lookup"><span data-stu-id="d0e71-122">-Files</span></span>
<span data-ttu-id="d0e71-123">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="d0e71-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d0e71-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d0e71-124">-JobName</span></span>
<span data-ttu-id="d0e71-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="d0e71-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="d0e71-126">-Query</span><span class="sxs-lookup"><span data-stu-id="d0e71-126">-Query</span></span>
<span data-ttu-id="d0e71-127">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="d0e71-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="d0e71-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="d0e71-128">-RunAsFileJob</span></span>
<span data-ttu-id="d0e71-129">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="d0e71-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="d0e71-130">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="d0e71-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="d0e71-131">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d0e71-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="d0e71-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d0e71-132">-StatusFolder</span></span>
<span data-ttu-id="d0e71-133">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="d0e71-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d0e71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e71-134">CommonParameters</span></span>
<span data-ttu-id="d0e71-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e71-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e71-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e71-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e71-137">INPUTS</span></span>

### <span data-ttu-id="d0e71-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0e71-138">None</span></span>

## <span data-ttu-id="d0e71-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0e71-139">OUTPUTS</span></span>

### <span data-ttu-id="d0e71-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d0e71-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d0e71-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0e71-141">NOTES</span></span>

## <span data-ttu-id="d0e71-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0e71-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0e71-143">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d0e71-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


