---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 8606cc96cde6271fd3d986eb0047475cbe709aee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546756"
---
# <span data-ttu-id="50d12-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="50d12-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="50d12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50d12-102">SYNOPSIS</span></span>
<span data-ttu-id="50d12-103">Tworzy obiekt zadania świni.</span><span class="sxs-lookup"><span data-stu-id="50d12-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50d12-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50d12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50d12-105">DESCRIPTION</span></span>
<span data-ttu-id="50d12-106">Polecenie cmdlet **New-AzureRmHDInsightPigJobDefinition** definiuje obiekt zadania wieprzowego, który ma być używany w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50d12-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="50d12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50d12-107">EXAMPLES</span></span>

### <span data-ttu-id="50d12-108">Przykład 1. Tworzenie definicji zadania w ramach trzody chlewnej</span><span class="sxs-lookup"><span data-stu-id="50d12-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="50d12-109">To polecenie umożliwia utworzenie definicji zadania w ramach trzody chlewnej.</span><span class="sxs-lookup"><span data-stu-id="50d12-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="50d12-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50d12-110">PARAMETERS</span></span>

### <span data-ttu-id="50d12-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="50d12-111">-Arguments</span></span>
<span data-ttu-id="50d12-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="50d12-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="50d12-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="50d12-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d12-114">-DefaultProfile</span></span>
<span data-ttu-id="50d12-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="50d12-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-116">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="50d12-116">-File</span></span>
<span data-ttu-id="50d12-117">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50d12-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="50d12-118">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="50d12-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="50d12-119">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="50d12-119">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-120">-Files</span><span class="sxs-lookup"><span data-stu-id="50d12-120">-Files</span></span>
<span data-ttu-id="50d12-121">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="50d12-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-122">-Query</span><span class="sxs-lookup"><span data-stu-id="50d12-122">-Query</span></span>
<span data-ttu-id="50d12-123">Umożliwia określenie zapytania wieprzowego.</span><span class="sxs-lookup"><span data-stu-id="50d12-123">Specifies the Pig query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="50d12-124">-StatusFolder</span></span>
<span data-ttu-id="50d12-125">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="50d12-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d12-126">CommonParameters</span></span>
<span data-ttu-id="50d12-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d12-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d12-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d12-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50d12-129">INPUTS</span></span>

### <span data-ttu-id="50d12-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="50d12-130">None</span></span>
<span data-ttu-id="50d12-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="50d12-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50d12-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50d12-132">OUTPUTS</span></span>

### <span data-ttu-id="50d12-133">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="50d12-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="50d12-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50d12-134">NOTES</span></span>

## <span data-ttu-id="50d12-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50d12-135">RELATED LINKS</span></span>

[<span data-ttu-id="50d12-136">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="50d12-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


