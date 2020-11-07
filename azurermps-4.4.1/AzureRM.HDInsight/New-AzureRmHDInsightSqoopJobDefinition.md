---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719031"
---
# <span data-ttu-id="62fb3-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="62fb3-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="62fb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="62fb3-103">Tworzy obiekt zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="62fb3-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62fb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62fb3-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62fb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="62fb3-106">Polecenie cmdlet **New-AzureRmHDInsightSqoopJobDefinition** definiuje obiekt zadania Sqoop do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="62fb3-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="62fb3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="62fb3-108">Przykład 1: Tworzenie definicji zadania programu Sqoop</span><span class="sxs-lookup"><span data-stu-id="62fb3-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="62fb3-109">To polecenie tworzy definicję zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="62fb3-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="62fb3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="62fb3-111">-Command</span><span class="sxs-lookup"><span data-stu-id="62fb3-111">-Command</span></span>
<span data-ttu-id="62fb3-112">Określa polecenie Sqoop.</span><span class="sxs-lookup"><span data-stu-id="62fb3-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="62fb3-113">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="62fb3-113">-File</span></span>
<span data-ttu-id="62fb3-114">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62fb3-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="62fb3-115">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="62fb3-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="62fb3-116">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="62fb3-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="62fb3-117">-Files</span><span class="sxs-lookup"><span data-stu-id="62fb3-117">-Files</span></span>
<span data-ttu-id="62fb3-118">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="62fb3-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="62fb3-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="62fb3-119">-LibDir</span></span>
<span data-ttu-id="62fb3-120">Określa katalog biblioteki zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="62fb3-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="62fb3-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="62fb3-121">-StatusFolder</span></span>
<span data-ttu-id="62fb3-122">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="62fb3-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="62fb3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fb3-123">-DefaultProfile</span></span>
<span data-ttu-id="62fb3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62fb3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62fb3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fb3-125">CommonParameters</span></span>
<span data-ttu-id="62fb3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fb3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fb3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fb3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fb3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62fb3-128">INPUTS</span></span>

## <span data-ttu-id="62fb3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62fb3-129">OUTPUTS</span></span>

### <span data-ttu-id="62fb3-130">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="62fb3-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="62fb3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62fb3-131">NOTES</span></span>

## <span data-ttu-id="62fb3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62fb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="62fb3-133">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="62fb3-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


