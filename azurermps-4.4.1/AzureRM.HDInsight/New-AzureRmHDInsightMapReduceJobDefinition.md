---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553880"
---
# <span data-ttu-id="46460-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="46460-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="46460-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46460-102">SYNOPSIS</span></span>
<span data-ttu-id="46460-103">Tworzy obiekt zadania programu MapReduce.</span><span class="sxs-lookup"><span data-stu-id="46460-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46460-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46460-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46460-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46460-105">DESCRIPTION</span></span>
<span data-ttu-id="46460-106">Polecenie cmdlet **New-AzureRmHDInsightMapReduceJobDefinition** definiuje nowe zadanie MapReduce, które ma być używane w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="46460-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="46460-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46460-107">EXAMPLES</span></span>

### <span data-ttu-id="46460-108">Przykład 1: Tworzenie definicji zadania programu MapReduce</span><span class="sxs-lookup"><span data-stu-id="46460-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="46460-109">To polecenie tworzy definicję zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="46460-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="46460-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46460-110">PARAMETERS</span></span>

### <span data-ttu-id="46460-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="46460-111">-Arguments</span></span>
<span data-ttu-id="46460-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="46460-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="46460-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="46460-114">-ClassName</span></span>
<span data-ttu-id="46460-115">Określa klasę zadania w pliku JAR.</span><span class="sxs-lookup"><span data-stu-id="46460-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="46460-116">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="46460-116">-Defines</span></span>
<span data-ttu-id="46460-117">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="46460-118">-Files</span><span class="sxs-lookup"><span data-stu-id="46460-118">-Files</span></span>
<span data-ttu-id="46460-119">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="46460-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="46460-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="46460-120">-JarFile</span></span>
<span data-ttu-id="46460-121">Określa plik JAR, który ma być używany jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="46460-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="46460-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="46460-122">-JobName</span></span>
<span data-ttu-id="46460-123">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="46460-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="46460-124">-LibJars</span></span>
<span data-ttu-id="46460-125">Określa słoiki biblioteki dla zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="46460-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="46460-126">-StatusFolder</span></span>
<span data-ttu-id="46460-127">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="46460-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="46460-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46460-128">-DefaultProfile</span></span>
<span data-ttu-id="46460-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46460-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46460-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46460-130">CommonParameters</span></span>
<span data-ttu-id="46460-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46460-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46460-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46460-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46460-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46460-133">INPUTS</span></span>

## <span data-ttu-id="46460-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46460-134">OUTPUTS</span></span>

### <span data-ttu-id="46460-135">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="46460-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="46460-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46460-136">NOTES</span></span>

## <span data-ttu-id="46460-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46460-137">RELATED LINKS</span></span>

[<span data-ttu-id="46460-138">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="46460-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


