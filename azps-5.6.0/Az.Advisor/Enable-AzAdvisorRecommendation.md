---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 6bf98fad2b1604f88293b81c55d49e9de3f0c33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967041"
---
# <span data-ttu-id="d1786-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1786-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="d1786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1786-102">SYNOPSIS</span></span>
<span data-ttu-id="d1786-103">Włącza zalecenia doradcy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1786-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="d1786-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1786-104">SYNTAX</span></span>

### <span data-ttu-id="d1786-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d1786-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1786-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1786-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1786-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1786-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1786-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1786-108">DESCRIPTION</span></span>
<span data-ttu-id="d1786-109">To polecenie cmdlet włącza poprzednio pominięte zalecenie.</span><span class="sxs-lookup"><span data-stu-id="d1786-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="d1786-110">Możesz również usunąć wszystkie wigorły skojarzone z zaleceniem.</span><span class="sxs-lookup"><span data-stu-id="d1786-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="d1786-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1786-111">EXAMPLES</span></span>

### <span data-ttu-id="d1786-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1786-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="d1786-113">Usuwa wszystkie akweduty dla danego zalecenia z nazwą "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="d1786-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="d1786-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d1786-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="d1786-115">Usuwa wszystkie amortyzy dla podanych zaleceń przekazanych z potoku.</span><span class="sxs-lookup"><span data-stu-id="d1786-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="d1786-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1786-116">PARAMETERS</span></span>

### <span data-ttu-id="d1786-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1786-117">-Confirm</span></span>
<span data-ttu-id="d1786-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1786-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1786-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1786-119">-DefaultProfile</span></span>
<span data-ttu-id="d1786-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1786-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1786-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1786-121">-InputObject</span></span>
<span data-ttu-id="d1786-122">Typ obiektu programu PowerShell PsAzureAdvisorResourceRecommendationBase zwrócony przez Get-AzAdvisorRecommendation połączenia.</span><span class="sxs-lookup"><span data-stu-id="d1786-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1786-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="d1786-123">-RecommendationName</span></span>
<span data-ttu-id="d1786-124">Nazwa_zasobu zalecenia.</span><span class="sxs-lookup"><span data-stu-id="d1786-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1786-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1786-125">-ResourceId</span></span>
<span data-ttu-id="d1786-126">Identyfikator zalecenia, które ma zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="d1786-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="d1786-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1786-127">-WhatIf</span></span>
<span data-ttu-id="d1786-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1786-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1786-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1786-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1786-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1786-130">CommonParameters</span></span>
<span data-ttu-id="d1786-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1786-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1786-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1786-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1786-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1786-133">INPUTS</span></span>

### <span data-ttu-id="d1786-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d1786-134">System.String</span></span>

### <span data-ttu-id="d1786-135">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="d1786-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="d1786-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1786-136">OUTPUTS</span></span>

### <span data-ttu-id="d1786-137">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="d1786-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="d1786-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1786-138">NOTES</span></span>

## <span data-ttu-id="d1786-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1786-139">RELATED LINKS</span></span>
