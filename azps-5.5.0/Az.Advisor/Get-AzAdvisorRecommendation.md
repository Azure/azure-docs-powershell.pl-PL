---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192658"
---
# <span data-ttu-id="c0704-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="c0704-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="c0704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0704-102">SYNOPSIS</span></span>
<span data-ttu-id="c0704-103">Otrzymuje listę zaleceń dotyczących usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="c0704-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="c0704-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0704-104">SYNTAX</span></span>

### <span data-ttu-id="c0704-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0704-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0704-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0704-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0704-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0704-107">DESCRIPTION</span></span>
<span data-ttu-id="c0704-108">Uzyskuje listę zaleceń dla doradcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0704-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="c0704-109">Można filtrować według kategorii, identyfikatora zasobu, nazwy itp.</span><span class="sxs-lookup"><span data-stu-id="c0704-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="c0704-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0704-110">EXAMPLES</span></span>

### <span data-ttu-id="c0704-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0704-111">Example 1</span></span>
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
<span data-ttu-id="c0704-112">Pobiera listę wszystkich zaleceń.</span><span class="sxs-lookup"><span data-stu-id="c0704-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="c0704-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c0704-113">Example 2</span></span>
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
<span data-ttu-id="c0704-114">Pobiera listę wszystkich zaleceń filtrowanych według kategorii Wydajność.</span><span class="sxs-lookup"><span data-stu-id="c0704-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="c0704-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0704-115">PARAMETERS</span></span>

### <span data-ttu-id="c0704-116">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="c0704-116">-Category</span></span>
<span data-ttu-id="c0704-117">Kategoria zalecenia</span><span class="sxs-lookup"><span data-stu-id="c0704-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0704-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0704-118">-DefaultProfile</span></span>
<span data-ttu-id="c0704-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0704-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0704-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0704-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0704-121">Nazwa grupy zasobów zalecenia</span><span class="sxs-lookup"><span data-stu-id="c0704-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="c0704-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0704-122">-ResourceId</span></span>
<span data-ttu-id="c0704-123">ResourceId zalecenia</span><span class="sxs-lookup"><span data-stu-id="c0704-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="c0704-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0704-124">CommonParameters</span></span>
<span data-ttu-id="c0704-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0704-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c0704-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0704-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0704-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0704-127">INPUTS</span></span>

### <span data-ttu-id="c0704-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c0704-128">System.String</span></span>

## <span data-ttu-id="c0704-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0704-129">OUTPUTS</span></span>

### <span data-ttu-id="c0704-130">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="c0704-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="c0704-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0704-131">NOTES</span></span>

## <span data-ttu-id="c0704-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0704-132">RELATED LINKS</span></span>
