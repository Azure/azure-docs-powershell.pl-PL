---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 4a21a8fdacdb53df7e513744cae31da4a7a61ca7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241387"
---
# <span data-ttu-id="10f73-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10f73-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="10f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f73-102">SYNOPSIS</span></span>
<span data-ttu-id="10f73-103">Tworzy obiekt zadania Świnka.</span><span class="sxs-lookup"><span data-stu-id="10f73-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="10f73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10f73-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10f73-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="10f73-105">DESCRIPTION</span></span>
<span data-ttu-id="10f73-106">Polecenie **cmdlet New-AzHDInsightPigJobDefinition** definiuje obiekt zadania Świnka do użytku z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="10f73-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="10f73-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10f73-107">EXAMPLES</span></span>

### <span data-ttu-id="10f73-108">Przykład 1. Tworzenie definicji zadania Świnka</span><span class="sxs-lookup"><span data-stu-id="10f73-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="10f73-109">To polecenie tworzy definicję zadania świnki.</span><span class="sxs-lookup"><span data-stu-id="10f73-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="10f73-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f73-110">PARAMETERS</span></span>

### <span data-ttu-id="10f73-111">— Argumenty</span><span class="sxs-lookup"><span data-stu-id="10f73-111">-Arguments</span></span>
<span data-ttu-id="10f73-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="10f73-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="10f73-113">Argumenty są przekazywane jako argumenty wiersza polecenia do każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="10f73-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="10f73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f73-114">-DefaultProfile</span></span>
<span data-ttu-id="10f73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="10f73-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f73-116">— Plik</span><span class="sxs-lookup"><span data-stu-id="10f73-116">-File</span></span>
<span data-ttu-id="10f73-117">Określa ścieżkę do pliku zawierającego zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="10f73-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="10f73-118">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="10f73-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="10f73-119">Możesz użyć tego parametru zamiast *parametru Query.*</span><span class="sxs-lookup"><span data-stu-id="10f73-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="10f73-120">— Pliki</span><span class="sxs-lookup"><span data-stu-id="10f73-120">-Files</span></span>
<span data-ttu-id="10f73-121">Określa zbiór plików skojarzonych z zadaniem Gałąź.</span><span class="sxs-lookup"><span data-stu-id="10f73-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="10f73-122">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="10f73-122">-Query</span></span>
<span data-ttu-id="10f73-123">Określa zapytanie Świnka.</span><span class="sxs-lookup"><span data-stu-id="10f73-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="10f73-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="10f73-124">-StatusFolder</span></span>
<span data-ttu-id="10f73-125">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="10f73-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="10f73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f73-126">CommonParameters</span></span>
<span data-ttu-id="10f73-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f73-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f73-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f73-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f73-129">INPUTS</span></span>

### <span data-ttu-id="10f73-130">Brak</span><span class="sxs-lookup"><span data-stu-id="10f73-130">None</span></span>

## <span data-ttu-id="10f73-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f73-131">OUTPUTS</span></span>

### <span data-ttu-id="10f73-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10f73-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="10f73-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10f73-133">NOTES</span></span>

## <span data-ttu-id="10f73-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f73-134">RELATED LINKS</span></span>

[<span data-ttu-id="10f73-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10f73-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


