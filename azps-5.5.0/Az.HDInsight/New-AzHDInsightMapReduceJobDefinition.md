---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200226"
---
# <span data-ttu-id="b4f0e-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b4f0e-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="b4f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f0e-103">Tworzy obiekt zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="b4f0e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4f0e-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f0e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f0e-106">Polecenie cmdlet **New-AzHDInsightMapReduceJobDefinition** definiuje nowe zadanie MapReduce do używania z klastrem usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b4f0e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f0e-108">Przykład 1. Tworzenie definicji zadania MapReduce</span><span class="sxs-lookup"><span data-stu-id="b4f0e-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b4f0e-109">To polecenie tworzy definicję zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="b4f0e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4f0e-110">PARAMETERS</span></span>

### <span data-ttu-id="b4f0e-111">— Argumenty</span><span class="sxs-lookup"><span data-stu-id="b4f0e-111">-Arguments</span></span>
<span data-ttu-id="b4f0e-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b4f0e-113">Argumenty są przekazywane do każdego zadania jako argumenty wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b4f0e-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="b4f0e-114">-ClassName</span></span>
<span data-ttu-id="b4f0e-115">Określa klasę zadania w pliku JAR.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-115">Specifies the job class in the JAR file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f0e-116">-DefaultProfile</span></span>
<span data-ttu-id="b4f0e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b4f0e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4f0e-118">— definiuje</span><span class="sxs-lookup"><span data-stu-id="b4f0e-118">-Defines</span></span>
<span data-ttu-id="b4f0e-119">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas pracy zadania.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b4f0e-120">— Pliki</span><span class="sxs-lookup"><span data-stu-id="b4f0e-120">-Files</span></span>
<span data-ttu-id="b4f0e-121">Określa zbiór plików skojarzonych z zadaniem Gałąź.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b4f0e-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="b4f0e-122">-JarFile</span></span>
<span data-ttu-id="b4f0e-123">Określa plik JAR do użycia w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-123">Specifies the JAR file to use for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f0e-124">— JobName</span><span class="sxs-lookup"><span data-stu-id="b4f0e-124">-JobName</span></span>
<span data-ttu-id="b4f0e-125">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="b4f0e-126">- LibJars</span><span class="sxs-lookup"><span data-stu-id="b4f0e-126">-LibJars</span></span>
<span data-ttu-id="b4f0e-127">Określa bibliotekę JARS dla zadania.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="b4f0e-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b4f0e-128">-StatusFolder</span></span>
<span data-ttu-id="b4f0e-129">Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b4f0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f0e-130">CommonParameters</span></span>
<span data-ttu-id="b4f0e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f0e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4f0e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f0e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4f0e-133">INPUTS</span></span>

### <span data-ttu-id="b4f0e-134">Brak</span><span class="sxs-lookup"><span data-stu-id="b4f0e-134">None</span></span>

## <span data-ttu-id="b4f0e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4f0e-135">OUTPUTS</span></span>

### <span data-ttu-id="b4f0e-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b4f0e-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="b4f0e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4f0e-137">NOTES</span></span>

## <span data-ttu-id="b4f0e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4f0e-138">RELATED LINKS</span></span>

[<span data-ttu-id="b4f0e-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b4f0e-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


