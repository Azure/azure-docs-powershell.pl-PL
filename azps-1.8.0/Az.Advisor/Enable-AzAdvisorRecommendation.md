---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 05d74b254645a970389aae859d60583c53c07670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704728"
---
# <span data-ttu-id="b763b-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="b763b-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="b763b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b763b-102">SYNOPSIS</span></span>
<span data-ttu-id="b763b-103">Włącza zalecenia usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="b763b-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="b763b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b763b-104">SYNTAX</span></span>

### <span data-ttu-id="b763b-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b763b-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b763b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b763b-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b763b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b763b-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b763b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b763b-108">DESCRIPTION</span></span>
<span data-ttu-id="b763b-109">To polecenie cmdlet włącza uprzednio pominięte rekomendacje.</span><span class="sxs-lookup"><span data-stu-id="b763b-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="b763b-110">Możesz również usunąć wszystkie tłumienie związane z zaleceniem.</span><span class="sxs-lookup"><span data-stu-id="b763b-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="b763b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b763b-111">EXAMPLES</span></span>

### <span data-ttu-id="b763b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b763b-112">Example 1</span></span>
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

<span data-ttu-id="b763b-113">Usuwa wszystkie pomijane dane zalecenie o nazwie "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="b763b-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="b763b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b763b-114">Example 2</span></span>
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

<span data-ttu-id="b763b-115">Usuwa wszystkie elementy pomijania dla podanych rekomendacji przekazanych z potoku.</span><span class="sxs-lookup"><span data-stu-id="b763b-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="b763b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b763b-116">PARAMETERS</span></span>

### <span data-ttu-id="b763b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b763b-117">-Confirm</span></span>
<span data-ttu-id="b763b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b763b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b763b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b763b-119">-DefaultProfile</span></span>
<span data-ttu-id="b763b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b763b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b763b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b763b-121">-InputObject</span></span>
<span data-ttu-id="b763b-122">Typ obiektu programu PowerShell PsAzureAdvisorResourceRecommendationBase zwrócony przez połączenie Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="b763b-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="b763b-123">-Rekomendacja</span><span class="sxs-lookup"><span data-stu-id="b763b-123">-RecommendationName</span></span>
<span data-ttu-id="b763b-124">ResourceName zalecenia.</span><span class="sxs-lookup"><span data-stu-id="b763b-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="b763b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b763b-125">-ResourceId</span></span>
<span data-ttu-id="b763b-126">Identyfikator zalecenia, które ma zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="b763b-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="b763b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b763b-127">-WhatIf</span></span>
<span data-ttu-id="b763b-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b763b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b763b-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b763b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b763b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b763b-130">CommonParameters</span></span>
<span data-ttu-id="b763b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b763b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b763b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b763b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b763b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b763b-133">INPUTS</span></span>

### <span data-ttu-id="b763b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b763b-134">System.String</span></span>

### <span data-ttu-id="b763b-135">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="b763b-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b763b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b763b-136">OUTPUTS</span></span>

### <span data-ttu-id="b763b-137">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="b763b-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b763b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b763b-138">NOTES</span></span>

## <span data-ttu-id="b763b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b763b-139">RELATED LINKS</span></span>
