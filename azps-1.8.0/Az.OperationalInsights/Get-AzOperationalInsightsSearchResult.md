---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708825"
---
# <span data-ttu-id="596ce-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="596ce-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="596ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="596ce-102">SYNOPSIS</span></span>
<span data-ttu-id="596ce-103">Zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="596ce-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="596ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="596ce-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="596ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="596ce-105">DESCRIPTION</span></span>
<span data-ttu-id="596ce-106">Polecenie cmdlet **Get-AzOperationalInsightsSearchResult** zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="596ce-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="596ce-107">Możesz uzyskać dostęp do stanu wyszukiwania we właściwości Metadata zwracanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="596ce-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="596ce-108">Jeśli stan jest oczekujący, wyszukiwanie nie zostało wykonane, a wyniki będą pochodzić z archiwum.</span><span class="sxs-lookup"><span data-stu-id="596ce-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="596ce-109">Wyniki wyszukiwania można pobrać z właściwości Value zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="596ce-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="596ce-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="596ce-110">EXAMPLES</span></span>

### <span data-ttu-id="596ce-111">Przykład 1: uzyskiwanie wyników wyszukiwania za pomocą kwerendy</span><span class="sxs-lookup"><span data-stu-id="596ce-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="596ce-112">To polecenie pobiera wszystkie wyniki wyszukiwania przy użyciu kwerendy.</span><span class="sxs-lookup"><span data-stu-id="596ce-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="596ce-113">Przykład 2: uzyskiwanie wyników wyszukiwania przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="596ce-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="596ce-114">To polecenie pobiera wyniki wyszukiwania przy użyciu identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="596ce-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="596ce-115">Przykład 3: oczekiwanie na ukończenie wyszukiwania przed wyświetleniem wyników</span><span class="sxs-lookup"><span data-stu-id="596ce-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="596ce-116">Ten skrypt rozpoczyna wyszukiwanie i czeka na zakończenie przed wyświetleniem wyników.</span><span class="sxs-lookup"><span data-stu-id="596ce-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="596ce-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="596ce-117">PARAMETERS</span></span>

### <span data-ttu-id="596ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596ce-118">-DefaultProfile</span></span>
<span data-ttu-id="596ce-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="596ce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="596ce-120">-Koniec</span><span class="sxs-lookup"><span data-stu-id="596ce-120">-End</span></span>
<span data-ttu-id="596ce-121">Koniec przeszukiwanego zakresu czasu.</span><span class="sxs-lookup"><span data-stu-id="596ce-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-122">-ID</span><span class="sxs-lookup"><span data-stu-id="596ce-122">-Id</span></span>
<span data-ttu-id="596ce-123">Jeśli zostanie podany identyfikator, wyniki wyszukiwania dla tego identyfikatora zostaną pobrane przy użyciu oryginalnych parametrów zapytania.</span><span class="sxs-lookup"><span data-stu-id="596ce-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="596ce-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-125">-Wyróżnianie</span><span class="sxs-lookup"><span data-stu-id="596ce-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-126">-Query</span><span class="sxs-lookup"><span data-stu-id="596ce-126">-Query</span></span>
<span data-ttu-id="596ce-127">Kwerenda wyszukiwania, która zostanie wykonana.</span><span class="sxs-lookup"><span data-stu-id="596ce-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="596ce-129">Nazwa grupy zasobów zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="596ce-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-130">-Start</span><span class="sxs-lookup"><span data-stu-id="596ce-130">-Start</span></span>
<span data-ttu-id="596ce-131">Początek poszukiwanego zakresu czasu.</span><span class="sxs-lookup"><span data-stu-id="596ce-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-132">-Początek</span><span class="sxs-lookup"><span data-stu-id="596ce-132">-Top</span></span>
<span data-ttu-id="596ce-133">Maksymalna liczba zwracanych wyników, ograniczona do 5000.</span><span class="sxs-lookup"><span data-stu-id="596ce-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-134">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="596ce-134">-WorkspaceName</span></span>
<span data-ttu-id="596ce-135">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="596ce-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596ce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596ce-136">CommonParameters</span></span>
<span data-ttu-id="596ce-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596ce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596ce-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596ce-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596ce-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="596ce-139">INPUTS</span></span>

### <span data-ttu-id="596ce-140">System. String</span><span class="sxs-lookup"><span data-stu-id="596ce-140">System.String</span></span>

### <span data-ttu-id="596ce-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="596ce-141">System.Int64</span></span>

### <span data-ttu-id="596ce-142">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="596ce-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="596ce-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="596ce-143">OUTPUTS</span></span>

### <span data-ttu-id="596ce-144">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="596ce-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="596ce-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="596ce-145">NOTES</span></span>

## <span data-ttu-id="596ce-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="596ce-146">RELATED LINKS</span></span>

[<span data-ttu-id="596ce-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="596ce-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


