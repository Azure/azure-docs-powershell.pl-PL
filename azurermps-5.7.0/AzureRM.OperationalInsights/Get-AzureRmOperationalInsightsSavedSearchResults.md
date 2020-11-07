---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716833"
---
# <span data-ttu-id="14034-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="14034-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="14034-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14034-102">SYNOPSIS</span></span>
<span data-ttu-id="14034-103">Zwraca wyniki zapytania.</span><span class="sxs-lookup"><span data-stu-id="14034-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14034-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14034-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14034-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14034-105">DESCRIPTION</span></span>
<span data-ttu-id="14034-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsSavedSearchResults** zwraca wyniki z zapytania określonego przez identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="14034-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="14034-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14034-107">EXAMPLES</span></span>

### <span data-ttu-id="14034-108">Przykład 1: uzyskiwanie wszystkich wyników wyszukiwania dla zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="14034-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="14034-109">To polecenie pobiera wszystkie wyniki wyszukiwania w poszukiwaniu zapisanego wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="14034-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="14034-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14034-110">PARAMETERS</span></span>

### <span data-ttu-id="14034-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14034-111">-DefaultProfile</span></span>
<span data-ttu-id="14034-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14034-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14034-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14034-113">-ResourceGroupName</span></span>
<span data-ttu-id="14034-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="14034-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14034-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="14034-115">-SavedSearchId</span></span>
<span data-ttu-id="14034-116">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="14034-116">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14034-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="14034-117">-WorkspaceName</span></span>
<span data-ttu-id="14034-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="14034-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14034-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14034-119">CommonParameters</span></span>
<span data-ttu-id="14034-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14034-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14034-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14034-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14034-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14034-122">INPUTS</span></span>

### <span data-ttu-id="14034-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="14034-123">None</span></span>
<span data-ttu-id="14034-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="14034-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14034-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14034-125">OUTPUTS</span></span>

### <span data-ttu-id="14034-126">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="14034-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="14034-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14034-127">NOTES</span></span>

## <span data-ttu-id="14034-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14034-128">RELATED LINKS</span></span>

[<span data-ttu-id="14034-129">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="14034-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


