---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958097"
---
# <span data-ttu-id="a742d-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a742d-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a742d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a742d-102">SYNOPSIS</span></span>
<span data-ttu-id="a742d-103">Zwraca wszystkie zapisane wyszukiwania w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a742d-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="a742d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a742d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a742d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a742d-105">DESCRIPTION</span></span>
<span data-ttu-id="a742d-106">Polecenie **cmdlet Get-AzOperationalInsightsSavedSearch** zwraca wszystkie zapisane wyszukiwania określonego obszaru roboczego w grupie zasobów, jeśli nie zostanie określony zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a742d-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="a742d-107">Jeśli określisz zapisany identyfikator wyszukiwania, zostanie zwrócone zapisane wyszukiwanie odpowiadające temu identyfikatorowi.</span><span class="sxs-lookup"><span data-stu-id="a742d-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="a742d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a742d-108">EXAMPLES</span></span>

### <span data-ttu-id="a742d-109">Przykład 1. Uzyskiwanie wszystkich zapisanych wyszukiwań w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="a742d-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="a742d-110">To polecenie pobiera wszystkie zapisane zasoby skojarzone z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="a742d-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="a742d-111">Przykład 2. Uzyskiwanie określonego zapisanego wyszukiwania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="a742d-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="a742d-112">To polecenie pobiera określone zapisane wyszukiwanie według jego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a742d-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="a742d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a742d-113">PARAMETERS</span></span>

### <span data-ttu-id="a742d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a742d-114">-DefaultProfile</span></span>
<span data-ttu-id="a742d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a742d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a742d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a742d-116">-ResourceGroupName</span></span>
<span data-ttu-id="a742d-117">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="a742d-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="a742d-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a742d-118">-SavedSearchId</span></span>
<span data-ttu-id="a742d-119">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a742d-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a742d-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a742d-120">-WorkspaceName</span></span>
<span data-ttu-id="a742d-121">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a742d-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="a742d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a742d-122">CommonParameters</span></span>
<span data-ttu-id="a742d-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a742d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a742d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a742d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a742d-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a742d-125">INPUTS</span></span>

### <span data-ttu-id="a742d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a742d-126">System.String</span></span>

## <span data-ttu-id="a742d-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a742d-127">OUTPUTS</span></span>

### <span data-ttu-id="a742d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="a742d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="a742d-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="a742d-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="a742d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a742d-130">NOTES</span></span>

## <span data-ttu-id="a742d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a742d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a742d-132">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="a742d-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


