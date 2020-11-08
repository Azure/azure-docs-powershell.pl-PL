---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 020a0684d6fe3a14b61b8582d8ad8427e68d8855
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061697"
---
# <span data-ttu-id="ed839-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="ed839-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="ed839-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed839-102">SYNOPSIS</span></span>
<span data-ttu-id="ed839-103">Zwraca wyniki zapytania.</span><span class="sxs-lookup"><span data-stu-id="ed839-103">Returns the results from a query.</span></span>

## <span data-ttu-id="ed839-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed839-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed839-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed839-105">DESCRIPTION</span></span>
<span data-ttu-id="ed839-106">Polecenie cmdlet **Get-AzOperationalInsightsSavedSearchResult** zwraca wyniki z zapytania określonego przez identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed839-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="ed839-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed839-107">EXAMPLES</span></span>

### <span data-ttu-id="ed839-108">Przykład 1: uzyskiwanie wszystkich wyników wyszukiwania dla zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="ed839-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="ed839-109">To polecenie pobiera wszystkie wyniki wyszukiwania w poszukiwaniu zapisanego wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed839-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="ed839-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed839-110">PARAMETERS</span></span>

### <span data-ttu-id="ed839-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed839-111">-DefaultProfile</span></span>
<span data-ttu-id="ed839-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ed839-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed839-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed839-113">-ResourceGroupName</span></span>
<span data-ttu-id="ed839-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="ed839-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ed839-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ed839-115">-SavedSearchId</span></span>
<span data-ttu-id="ed839-116">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed839-116">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed839-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="ed839-117">-WorkspaceName</span></span>
<span data-ttu-id="ed839-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ed839-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="ed839-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed839-119">CommonParameters</span></span>
<span data-ttu-id="ed839-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed839-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed839-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed839-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed839-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed839-122">INPUTS</span></span>

### <span data-ttu-id="ed839-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ed839-123">System.String</span></span>

## <span data-ttu-id="ed839-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed839-124">OUTPUTS</span></span>

### <span data-ttu-id="ed839-125">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="ed839-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="ed839-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed839-126">NOTES</span></span>

## <span data-ttu-id="ed839-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed839-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed839-128">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="ed839-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


