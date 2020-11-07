---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704729"
---
# <span data-ttu-id="325c7-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="325c7-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="325c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="325c7-102">SYNOPSIS</span></span>
<span data-ttu-id="325c7-103">Wyłącz zalecenia dotyczące usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="325c7-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="325c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="325c7-104">SYNTAX</span></span>

### <span data-ttu-id="325c7-105">IdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="325c7-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325c7-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="325c7-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325c7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="325c7-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325c7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="325c7-108">DESCRIPTION</span></span>
<span data-ttu-id="325c7-109">Tworzy pominięcie rekomendacji, to umożliwia odroczenie konkretnego rekomendacji na określony czas trwania lub bez zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="325c7-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="325c7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="325c7-110">EXAMPLES</span></span>

### <span data-ttu-id="325c7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="325c7-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="325c7-112">Utwórz tłumienie dla danej nazwy rekomendacji z domyślną wartością-SuppressionName i domyślną wartością dni na-1.</span><span class="sxs-lookup"><span data-stu-id="325c7-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="325c7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="325c7-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="325c7-114">Dla danego zalecenia-ID jest tworzone pomijanie.</span><span class="sxs-lookup"><span data-stu-id="325c7-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="325c7-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="325c7-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="325c7-116">Tworzenie tłumienia, przewody rurowe z Get-AzAdvisorRecommendation w celu wyłączenia-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="325c7-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="325c7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="325c7-117">PARAMETERS</span></span>

### <span data-ttu-id="325c7-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="325c7-118">-Confirm</span></span>
<span data-ttu-id="325c7-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="325c7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325c7-120">-Dni</span><span class="sxs-lookup"><span data-stu-id="325c7-120">-Days</span></span>
<span data-ttu-id="325c7-121">Dni do wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="325c7-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325c7-122">-DefaultProfile</span></span>
<span data-ttu-id="325c7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="325c7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325c7-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="325c7-124">-InputObject</span></span>
<span data-ttu-id="325c7-125">Typ obiektu programu PowerShell PsAzureAdvisorResourceRecommendationBase zwrócony przez połączenie Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="325c7-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="325c7-126">-Rekomendacja</span><span class="sxs-lookup"><span data-stu-id="325c7-126">-RecommendationName</span></span>
<span data-ttu-id="325c7-127">ResourceName zalecenia</span><span class="sxs-lookup"><span data-stu-id="325c7-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="325c7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="325c7-128">-ResourceId</span></span>
<span data-ttu-id="325c7-129">Identyfikator zalecenia, które ma zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="325c7-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325c7-130">-WhatIf</span></span>
<span data-ttu-id="325c7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="325c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="325c7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="325c7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325c7-133">CommonParameters</span></span>
<span data-ttu-id="325c7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="325c7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325c7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325c7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="325c7-136">INPUTS</span></span>

### <span data-ttu-id="325c7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="325c7-137">System.String</span></span>

### <span data-ttu-id="325c7-138">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="325c7-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="325c7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="325c7-139">OUTPUTS</span></span>

### <span data-ttu-id="325c7-140">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="325c7-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="325c7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="325c7-141">NOTES</span></span>

## <span data-ttu-id="325c7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="325c7-142">RELATED LINKS</span></span>