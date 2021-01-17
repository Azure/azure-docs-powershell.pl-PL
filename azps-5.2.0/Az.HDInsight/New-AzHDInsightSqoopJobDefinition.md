---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322943"
---
# <span data-ttu-id="32148-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32148-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="32148-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32148-102">SYNOPSIS</span></span>
<span data-ttu-id="32148-103">Tworzy obiekt zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="32148-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="32148-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32148-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32148-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32148-105">DESCRIPTION</span></span>
<span data-ttu-id="32148-106">Polecenie cmdlet **New-AzHDInsightSqoopJobDefinition** definiuje obiekt zadania Sqoop do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="32148-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="32148-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32148-107">EXAMPLES</span></span>

### <span data-ttu-id="32148-108">Przykład 1: Tworzenie definicji zadania programu Sqoop</span><span class="sxs-lookup"><span data-stu-id="32148-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="32148-109">To polecenie tworzy definicję zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="32148-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="32148-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32148-110">PARAMETERS</span></span>

### <span data-ttu-id="32148-111">-Command</span><span class="sxs-lookup"><span data-stu-id="32148-111">-Command</span></span>
<span data-ttu-id="32148-112">Określa polecenie Sqoop.</span><span class="sxs-lookup"><span data-stu-id="32148-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="32148-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32148-113">-DefaultProfile</span></span>
<span data-ttu-id="32148-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="32148-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32148-115">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="32148-115">-File</span></span>
<span data-ttu-id="32148-116">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="32148-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="32148-117">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="32148-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="32148-118">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="32148-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="32148-119">-Files</span><span class="sxs-lookup"><span data-stu-id="32148-119">-Files</span></span>
<span data-ttu-id="32148-120">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="32148-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="32148-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="32148-121">-LibDir</span></span>
<span data-ttu-id="32148-122">Określa katalog biblioteki zadania programu Sqoop.</span><span class="sxs-lookup"><span data-stu-id="32148-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="32148-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="32148-123">-StatusFolder</span></span>
<span data-ttu-id="32148-124">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="32148-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="32148-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32148-125">CommonParameters</span></span>
<span data-ttu-id="32148-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32148-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32148-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32148-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32148-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32148-128">INPUTS</span></span>

### <span data-ttu-id="32148-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="32148-129">None</span></span>

## <span data-ttu-id="32148-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32148-130">OUTPUTS</span></span>

### <span data-ttu-id="32148-131">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="32148-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="32148-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32148-132">NOTES</span></span>

## <span data-ttu-id="32148-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32148-133">RELATED LINKS</span></span>

[<span data-ttu-id="32148-134">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="32148-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


