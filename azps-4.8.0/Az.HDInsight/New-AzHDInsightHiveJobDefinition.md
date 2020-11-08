---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063534"
---
# <span data-ttu-id="2331e-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2331e-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2331e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2331e-102">SYNOPSIS</span></span>
<span data-ttu-id="2331e-103">Tworzy obiekt zadania w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="2331e-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="2331e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2331e-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2331e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2331e-105">DESCRIPTION</span></span>
<span data-ttu-id="2331e-106">Polecenie cmdlet **New-AzHDInsightHiveJobDefinition** definiuje obiekt zadania Hive do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2331e-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2331e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2331e-107">EXAMPLES</span></span>

### <span data-ttu-id="2331e-108">Przykład 1: Tworzenie definicji zadania w gałęzi</span><span class="sxs-lookup"><span data-stu-id="2331e-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="2331e-109">To polecenie tworzy definicję zadania w gałęzi.</span><span class="sxs-lookup"><span data-stu-id="2331e-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="2331e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2331e-110">PARAMETERS</span></span>

### <span data-ttu-id="2331e-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="2331e-111">-Arguments</span></span>
<span data-ttu-id="2331e-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="2331e-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="2331e-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="2331e-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="2331e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2331e-114">-DefaultProfile</span></span>
<span data-ttu-id="2331e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2331e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2331e-116">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="2331e-116">-Defines</span></span>
<span data-ttu-id="2331e-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="2331e-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="2331e-118">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="2331e-118">-File</span></span>
<span data-ttu-id="2331e-119">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2331e-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="2331e-120">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="2331e-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="2331e-121">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="2331e-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2331e-122">-Files</span><span class="sxs-lookup"><span data-stu-id="2331e-122">-Files</span></span>
<span data-ttu-id="2331e-123">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="2331e-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="2331e-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="2331e-124">-JobName</span></span>
<span data-ttu-id="2331e-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="2331e-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="2331e-126">-Query</span><span class="sxs-lookup"><span data-stu-id="2331e-126">-Query</span></span>
<span data-ttu-id="2331e-127">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="2331e-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="2331e-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="2331e-128">-RunAsFileJob</span></span>
<span data-ttu-id="2331e-129">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="2331e-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="2331e-130">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="2331e-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="2331e-131">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="2331e-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="2331e-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2331e-132">-StatusFolder</span></span>
<span data-ttu-id="2331e-133">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="2331e-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2331e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2331e-134">CommonParameters</span></span>
<span data-ttu-id="2331e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2331e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2331e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2331e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2331e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2331e-137">INPUTS</span></span>

### <span data-ttu-id="2331e-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2331e-138">None</span></span>

## <span data-ttu-id="2331e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2331e-139">OUTPUTS</span></span>

### <span data-ttu-id="2331e-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2331e-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2331e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2331e-141">NOTES</span></span>

## <span data-ttu-id="2331e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2331e-142">RELATED LINKS</span></span>

[<span data-ttu-id="2331e-143">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2331e-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


