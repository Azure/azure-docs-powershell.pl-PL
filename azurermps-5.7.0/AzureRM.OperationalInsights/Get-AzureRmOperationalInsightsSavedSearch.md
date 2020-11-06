---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542455"
---
# <span data-ttu-id="c9d9b-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c9d9b-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c9d9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d9b-103">Zwraca wszystkie zapisane wyszukiwania dla określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9d9b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d9b-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsSavedSearch** zwraca wszystkie zapisane wyszukiwania dla określonego obszaru roboczego w określonej grupie zasobów, jeśli nie określisz zapisanego identyfikatora wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="c9d9b-107">Jeśli określisz zapisany identyfikator wyszukiwania, zostanie zwrócona wartość zapisanego wyszukiwania odpowiadająca temu IDENTYFIKATORowi.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="c9d9b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9d9b-108">EXAMPLES</span></span>

### <span data-ttu-id="c9d9b-109">Przykład 1. pobieranie wszystkich zapisanych wyszukiwań w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="c9d9b-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c9d9b-110">To polecenie umożliwia pobieranie wszystkich zapisanych zasobów skojarzonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="c9d9b-111">Przykład 2: uzyskiwanie określonego zapisanego wyszukiwania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c9d9b-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="c9d9b-112">To polecenie pobiera określone zapisane wyszukiwanie według jego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="c9d9b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9d9b-113">PARAMETERS</span></span>

### <span data-ttu-id="c9d9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d9b-114">-DefaultProfile</span></span>
<span data-ttu-id="c9d9b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9d9b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9d9b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d9b-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9d9b-117">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c9d9b-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c9d9b-118">-SavedSearchId</span></span>
<span data-ttu-id="c9d9b-119">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9b-120">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c9d9b-120">-WorkspaceName</span></span>
<span data-ttu-id="c9d9b-121">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c9d9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d9b-122">CommonParameters</span></span>
<span data-ttu-id="c9d9b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d9b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d9b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9d9b-125">INPUTS</span></span>

### <span data-ttu-id="c9d9b-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c9d9b-126">None</span></span>
<span data-ttu-id="c9d9b-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c9d9b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9d9b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9d9b-128">OUTPUTS</span></span>

### <span data-ttu-id="c9d9b-129">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9d9b-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="c9d9b-130">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9d9b-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="c9d9b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9d9b-131">NOTES</span></span>

## <span data-ttu-id="c9d9b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9d9b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9d9b-133">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="c9d9b-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


