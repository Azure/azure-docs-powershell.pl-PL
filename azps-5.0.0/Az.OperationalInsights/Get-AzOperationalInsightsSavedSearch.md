---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225848"
---
# <span data-ttu-id="5628d-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="5628d-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="5628d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5628d-102">SYNOPSIS</span></span>
<span data-ttu-id="5628d-103">Zwraca wszystkie zapisane wyszukiwania dla określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5628d-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="5628d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5628d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5628d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5628d-105">DESCRIPTION</span></span>
<span data-ttu-id="5628d-106">Polecenie cmdlet **Get-AzOperationalInsightsSavedSearch** zwraca wszystkie zapisane wyszukiwania dla określonego obszaru roboczego w określonej grupie zasobów, jeśli nie określisz zapisanego identyfikatora wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="5628d-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="5628d-107">Jeśli określisz zapisany identyfikator wyszukiwania, zostanie zwrócona wartość zapisanego wyszukiwania odpowiadająca temu IDENTYFIKATORowi.</span><span class="sxs-lookup"><span data-stu-id="5628d-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="5628d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5628d-108">EXAMPLES</span></span>

### <span data-ttu-id="5628d-109">Przykład 1. pobieranie wszystkich zapisanych wyszukiwań w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="5628d-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="5628d-110">To polecenie umożliwia pobieranie wszystkich zapisanych zasobów skojarzonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="5628d-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="5628d-111">Przykład 2: uzyskiwanie określonego zapisanego wyszukiwania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5628d-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="5628d-112">To polecenie pobiera określone zapisane wyszukiwanie według jego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="5628d-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="5628d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5628d-113">PARAMETERS</span></span>

### <span data-ttu-id="5628d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5628d-114">-DefaultProfile</span></span>
<span data-ttu-id="5628d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5628d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5628d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5628d-116">-ResourceGroupName</span></span>
<span data-ttu-id="5628d-117">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="5628d-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="5628d-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5628d-118">-SavedSearchId</span></span>
<span data-ttu-id="5628d-119">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="5628d-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="5628d-120">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5628d-120">-WorkspaceName</span></span>
<span data-ttu-id="5628d-121">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5628d-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="5628d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5628d-122">CommonParameters</span></span>
<span data-ttu-id="5628d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5628d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5628d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5628d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5628d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5628d-125">INPUTS</span></span>

### <span data-ttu-id="5628d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5628d-126">System.String</span></span>

## <span data-ttu-id="5628d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5628d-127">OUTPUTS</span></span>

### <span data-ttu-id="5628d-128">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="5628d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="5628d-129">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="5628d-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="5628d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5628d-130">NOTES</span></span>

## <span data-ttu-id="5628d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5628d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5628d-132">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="5628d-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


