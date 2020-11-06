---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 27f2e9d6dbc823f7148db6a299f9e999131c75d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554092"
---
# <span data-ttu-id="31385-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="31385-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="31385-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31385-102">SYNOPSIS</span></span>
<span data-ttu-id="31385-103">Tworzy obiekt zadania świni.</span><span class="sxs-lookup"><span data-stu-id="31385-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31385-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31385-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31385-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31385-105">DESCRIPTION</span></span>
<span data-ttu-id="31385-106">Polecenie cmdlet **New-AzureRmHDInsightPigJobDefinition** definiuje obiekt zadania wieprzowego, który ma być używany w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31385-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="31385-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31385-107">EXAMPLES</span></span>

### <span data-ttu-id="31385-108">Przykład 1. Tworzenie definicji zadania w ramach trzody chlewnej</span><span class="sxs-lookup"><span data-stu-id="31385-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="31385-109">To polecenie umożliwia utworzenie definicji zadania w ramach trzody chlewnej.</span><span class="sxs-lookup"><span data-stu-id="31385-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="31385-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31385-110">PARAMETERS</span></span>

### <span data-ttu-id="31385-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="31385-111">-Arguments</span></span>
<span data-ttu-id="31385-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="31385-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="31385-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="31385-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="31385-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31385-114">-DefaultProfile</span></span>
<span data-ttu-id="31385-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="31385-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31385-116">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="31385-116">-File</span></span>
<span data-ttu-id="31385-117">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="31385-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="31385-118">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="31385-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="31385-119">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="31385-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="31385-120">-Files</span><span class="sxs-lookup"><span data-stu-id="31385-120">-Files</span></span>
<span data-ttu-id="31385-121">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="31385-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="31385-122">-Query</span><span class="sxs-lookup"><span data-stu-id="31385-122">-Query</span></span>
<span data-ttu-id="31385-123">Umożliwia określenie zapytania wieprzowego.</span><span class="sxs-lookup"><span data-stu-id="31385-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="31385-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="31385-124">-StatusFolder</span></span>
<span data-ttu-id="31385-125">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="31385-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="31385-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31385-126">CommonParameters</span></span>
<span data-ttu-id="31385-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31385-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31385-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31385-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31385-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31385-129">INPUTS</span></span>

### <span data-ttu-id="31385-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="31385-130">None</span></span>

## <span data-ttu-id="31385-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31385-131">OUTPUTS</span></span>

### <span data-ttu-id="31385-132">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="31385-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="31385-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31385-133">NOTES</span></span>

## <span data-ttu-id="31385-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31385-134">RELATED LINKS</span></span>

[<span data-ttu-id="31385-135">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="31385-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


