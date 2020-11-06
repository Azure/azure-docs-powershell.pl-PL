---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545731"
---
# <span data-ttu-id="23f5f-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="23f5f-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="23f5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="23f5f-103">Tworzy obiekt zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="23f5f-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23f5f-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f5f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="23f5f-106">Polecenie cmdlet **New-AzureRmHDInsightSqoopJobDefinition** definiuje obiekt zadania Sqoop do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23f5f-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="23f5f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23f5f-107">EXAMPLES</span></span>

### <span data-ttu-id="23f5f-108">Przykład 1: Tworzenie definicji zadania programu Sqoop</span><span class="sxs-lookup"><span data-stu-id="23f5f-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="23f5f-109">To polecenie tworzy definicję zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="23f5f-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="23f5f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23f5f-110">PARAMETERS</span></span>

### <span data-ttu-id="23f5f-111">-Command</span><span class="sxs-lookup"><span data-stu-id="23f5f-111">-Command</span></span>
<span data-ttu-id="23f5f-112">Określa polecenie Sqoop.</span><span class="sxs-lookup"><span data-stu-id="23f5f-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="23f5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f5f-113">-DefaultProfile</span></span>
<span data-ttu-id="23f5f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="23f5f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23f5f-115">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="23f5f-115">-File</span></span>
<span data-ttu-id="23f5f-116">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="23f5f-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="23f5f-117">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="23f5f-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="23f5f-118">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="23f5f-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="23f5f-119">-Files</span><span class="sxs-lookup"><span data-stu-id="23f5f-119">-Files</span></span>
<span data-ttu-id="23f5f-120">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="23f5f-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="23f5f-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="23f5f-121">-LibDir</span></span>
<span data-ttu-id="23f5f-122">Określa katalog biblioteki zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="23f5f-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="23f5f-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="23f5f-123">-StatusFolder</span></span>
<span data-ttu-id="23f5f-124">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="23f5f-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="23f5f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f5f-125">CommonParameters</span></span>
<span data-ttu-id="23f5f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f5f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f5f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f5f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f5f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23f5f-128">INPUTS</span></span>

### <span data-ttu-id="23f5f-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="23f5f-129">None</span></span>
<span data-ttu-id="23f5f-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="23f5f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23f5f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23f5f-131">OUTPUTS</span></span>

### <span data-ttu-id="23f5f-132">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="23f5f-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="23f5f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23f5f-133">NOTES</span></span>

## <span data-ttu-id="23f5f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23f5f-134">RELATED LINKS</span></span>

[<span data-ttu-id="23f5f-135">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="23f5f-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


