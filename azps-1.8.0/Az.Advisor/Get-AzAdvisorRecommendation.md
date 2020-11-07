---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 894fc2b3f3e722c7924e05e6c700ae03f741562f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704725"
---
# <span data-ttu-id="f66ed-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="f66ed-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="f66ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f66ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f66ed-103">Pobiera listę zaleceń dotyczących usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="f66ed-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="f66ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f66ed-104">SYNTAX</span></span>

### <span data-ttu-id="f66ed-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f66ed-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f66ed-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f66ed-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f66ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f66ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f66ed-108">Otrzymuje listę zaleceń dotyczących usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="f66ed-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="f66ed-109">Można filtrować według kategorii, identyfikatora zasobu, nazwy itd.</span><span class="sxs-lookup"><span data-stu-id="f66ed-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="f66ed-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f66ed-110">EXAMPLES</span></span>

### <span data-ttu-id="f66ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f66ed-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="f66ed-112">Pobiera listę wszystkich zaleceń.</span><span class="sxs-lookup"><span data-stu-id="f66ed-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="f66ed-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f66ed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="f66ed-114">Pobiera listę wszystkich rekomendacji filtrowanych według wydajności kategorii.</span><span class="sxs-lookup"><span data-stu-id="f66ed-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="f66ed-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f66ed-115">PARAMETERS</span></span>

### <span data-ttu-id="f66ed-116">-Category</span><span class="sxs-lookup"><span data-stu-id="f66ed-116">-Category</span></span>
<span data-ttu-id="f66ed-117">Kategoria rekomendacji</span><span class="sxs-lookup"><span data-stu-id="f66ed-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66ed-118">-DefaultProfile</span></span>
<span data-ttu-id="f66ed-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f66ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f66ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="f66ed-121">Nazwa tego zalecenia</span><span class="sxs-lookup"><span data-stu-id="f66ed-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66ed-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f66ed-122">-ResourceId</span></span>
<span data-ttu-id="f66ed-123">Identyfikator ResourceId zalecenia</span><span class="sxs-lookup"><span data-stu-id="f66ed-123">ResourceId of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f66ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66ed-124">CommonParameters</span></span>
<span data-ttu-id="f66ed-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f66ed-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f66ed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66ed-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66ed-127">INPUTS</span></span>

### <span data-ttu-id="f66ed-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f66ed-128">System.String</span></span>

## <span data-ttu-id="f66ed-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f66ed-129">OUTPUTS</span></span>

### <span data-ttu-id="f66ed-130">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="f66ed-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="f66ed-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f66ed-131">NOTES</span></span>

## <span data-ttu-id="f66ed-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f66ed-132">RELATED LINKS</span></span>