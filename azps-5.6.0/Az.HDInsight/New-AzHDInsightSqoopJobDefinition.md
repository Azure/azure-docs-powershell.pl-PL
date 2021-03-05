---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 3217673c01e4d77fe2643765df55ff58747b3133
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971969"
---
# <span data-ttu-id="b6ead-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b6ead-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b6ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ead-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ead-103">Tworzy obiekt zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b6ead-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="b6ead-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6ead-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ead-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6ead-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ead-106">Polecenie cmdlet **New-AzHDInsightSqoopJobDefinition** definiuje obiekt zadania Sqoop do użytku z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b6ead-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b6ead-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6ead-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ead-108">Przykład 1. Tworzenie definicji stanowiska sqoop</span><span class="sxs-lookup"><span data-stu-id="b6ead-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b6ead-109">To polecenie tworzy definicję zadania sqoop.</span><span class="sxs-lookup"><span data-stu-id="b6ead-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="b6ead-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6ead-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ead-111">- Command</span><span class="sxs-lookup"><span data-stu-id="b6ead-111">-Command</span></span>
<span data-ttu-id="b6ead-112">Określa polecenie Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b6ead-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="b6ead-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ead-113">-DefaultProfile</span></span>
<span data-ttu-id="b6ead-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b6ead-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6ead-115">— Plik</span><span class="sxs-lookup"><span data-stu-id="b6ead-115">-File</span></span>
<span data-ttu-id="b6ead-116">Określa ścieżkę do pliku zawierającego zapytanie do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="b6ead-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b6ead-117">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="b6ead-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="b6ead-118">Możesz użyć tego parametru zamiast *parametru Query.*</span><span class="sxs-lookup"><span data-stu-id="b6ead-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b6ead-119">— Pliki</span><span class="sxs-lookup"><span data-stu-id="b6ead-119">-Files</span></span>
<span data-ttu-id="b6ead-120">Określa zbiór plików skojarzonych z zadaniem Gałąź.</span><span class="sxs-lookup"><span data-stu-id="b6ead-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b6ead-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="b6ead-121">-LibDir</span></span>
<span data-ttu-id="b6ead-122">Określa katalog biblioteki dla zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b6ead-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="b6ead-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b6ead-123">-StatusFolder</span></span>
<span data-ttu-id="b6ead-124">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="b6ead-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b6ead-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ead-125">CommonParameters</span></span>
<span data-ttu-id="b6ead-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ead-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ead-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6ead-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ead-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6ead-128">INPUTS</span></span>

### <span data-ttu-id="b6ead-129">Brak</span><span class="sxs-lookup"><span data-stu-id="b6ead-129">None</span></span>

## <span data-ttu-id="b6ead-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6ead-130">OUTPUTS</span></span>

### <span data-ttu-id="b6ead-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b6ead-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b6ead-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6ead-132">NOTES</span></span>

## <span data-ttu-id="b6ead-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6ead-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6ead-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b6ead-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


