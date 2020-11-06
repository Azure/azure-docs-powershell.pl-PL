---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: fd933d157748de424aa425179701897772d93569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553883"
---
# <span data-ttu-id="76ff4-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="76ff4-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="76ff4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="76ff4-103">Tworzy obiekt zadania w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="76ff4-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76ff4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76ff4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ff4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="76ff4-106">Polecenie cmdlet **New-AzureRmHDInsightHiveJobDefinition** definiuje obiekt zadania Hive do użytku w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76ff4-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="76ff4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="76ff4-108">Przykład 1: Tworzenie definicji zadania w gałęzi</span><span class="sxs-lookup"><span data-stu-id="76ff4-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="76ff4-109">To polecenie tworzy definicję zadania w gałęzi.</span><span class="sxs-lookup"><span data-stu-id="76ff4-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="76ff4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76ff4-110">PARAMETERS</span></span>

### <span data-ttu-id="76ff4-111">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="76ff4-111">-Arguments</span></span>
<span data-ttu-id="76ff4-112">Określa tablicę argumentów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="76ff4-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="76ff4-113">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="76ff4-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="76ff4-114">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="76ff4-114">-Defines</span></span>
<span data-ttu-id="76ff4-115">Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="76ff4-115">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="76ff4-116">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="76ff4-116">-File</span></span>
<span data-ttu-id="76ff4-117">Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76ff4-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="76ff4-118">Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.</span><span class="sxs-lookup"><span data-stu-id="76ff4-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="76ff4-119">Tego parametru można użyć zamiast parametru *zapytania* .</span><span class="sxs-lookup"><span data-stu-id="76ff4-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="76ff4-120">-Files</span><span class="sxs-lookup"><span data-stu-id="76ff4-120">-Files</span></span>
<span data-ttu-id="76ff4-121">Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.</span><span class="sxs-lookup"><span data-stu-id="76ff4-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="76ff4-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="76ff4-122">-JobName</span></span>
<span data-ttu-id="76ff4-123">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="76ff4-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="76ff4-124">-Query</span><span class="sxs-lookup"><span data-stu-id="76ff4-124">-Query</span></span>
<span data-ttu-id="76ff4-125">Określa zapytanie dotyczące gałęzi.</span><span class="sxs-lookup"><span data-stu-id="76ff4-125">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="76ff4-126">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="76ff4-126">-RunAsFileJob</span></span>
<span data-ttu-id="76ff4-127">Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="76ff4-127">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="76ff4-128">To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="76ff4-128">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="76ff4-129">Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.</span><span class="sxs-lookup"><span data-stu-id="76ff4-129">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="76ff4-130">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="76ff4-130">-StatusFolder</span></span>
<span data-ttu-id="76ff4-131">Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.</span><span class="sxs-lookup"><span data-stu-id="76ff4-131">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="76ff4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ff4-132">-DefaultProfile</span></span>
<span data-ttu-id="76ff4-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76ff4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ff4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ff4-134">CommonParameters</span></span>
<span data-ttu-id="76ff4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ff4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ff4-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ff4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ff4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76ff4-137">INPUTS</span></span>

## <span data-ttu-id="76ff4-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76ff4-138">OUTPUTS</span></span>

### <span data-ttu-id="76ff4-139">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="76ff4-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="76ff4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76ff4-140">NOTES</span></span>

## <span data-ttu-id="76ff4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76ff4-141">RELATED LINKS</span></span>

[<span data-ttu-id="76ff4-142">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="76ff4-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


