---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176530"
---
# <span data-ttu-id="9e228-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="9e228-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="9e228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e228-102">SYNOPSIS</span></span>
<span data-ttu-id="9e228-103">Wyłącz zalecenie usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="9e228-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="9e228-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e228-104">SYNTAX</span></span>

### <span data-ttu-id="9e228-105">IdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9e228-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e228-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e228-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e228-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e228-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e228-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e228-108">DESCRIPTION</span></span>
<span data-ttu-id="9e228-109">Tworzy polecanie, co umożliwia odłożenie określonego zalecenia o określony czas trwania lub w nieskończoność.</span><span class="sxs-lookup"><span data-stu-id="9e228-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="9e228-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e228-110">EXAMPLES</span></span>

### <span data-ttu-id="9e228-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e228-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="9e228-112">Utwórz polecaną nazwę z wartością domyślną NazwaDomowy i domyślne dni na -1.</span><span class="sxs-lookup"><span data-stu-id="9e228-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="9e228-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9e228-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="9e228-114">Utworzono pochłoną to zalecenie.</span><span class="sxs-lookup"><span data-stu-id="9e228-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="9e228-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9e228-115">Example 3</span></span>
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

<span data-ttu-id="9e228-116">Tworzenie wytłaczyń z programu Get-AzAdvisorRecommendation do disable-azAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="9e228-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="9e228-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e228-117">PARAMETERS</span></span>

### <span data-ttu-id="9e228-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e228-118">-Confirm</span></span>
<span data-ttu-id="9e228-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e228-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e228-120">— Dni</span><span class="sxs-lookup"><span data-stu-id="9e228-120">-Days</span></span>
<span data-ttu-id="9e228-121">Dni na wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="9e228-121">Days to disable.</span></span>

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

### <span data-ttu-id="9e228-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e228-122">-DefaultProfile</span></span>
<span data-ttu-id="9e228-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e228-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e228-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e228-124">-InputObject</span></span>
<span data-ttu-id="9e228-125">Typ obiektu programu PowerShell PsAzureAdvisorResourceRecommendationBase zwrócony przez Get-AzAdvisorRecommendation połączenia.</span><span class="sxs-lookup"><span data-stu-id="9e228-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="9e228-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="9e228-126">-RecommendationName</span></span>
<span data-ttu-id="9e228-127">Nazwa Zasobu zalecenia</span><span class="sxs-lookup"><span data-stu-id="9e228-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="9e228-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e228-128">-ResourceId</span></span>
<span data-ttu-id="9e228-129">Identyfikator zalecenia, które ma zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="9e228-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="9e228-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e228-130">-WhatIf</span></span>
<span data-ttu-id="9e228-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e228-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e228-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9e228-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e228-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e228-133">CommonParameters</span></span>
<span data-ttu-id="9e228-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e228-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e228-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e228-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e228-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e228-136">INPUTS</span></span>

### <span data-ttu-id="9e228-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9e228-137">System.String</span></span>

### <span data-ttu-id="9e228-138">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="9e228-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="9e228-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e228-139">OUTPUTS</span></span>

### <span data-ttu-id="9e228-140">Microsoft.Azure.Commands.Advisor.Cmdlet.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="9e228-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="9e228-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e228-141">NOTES</span></span>

## <span data-ttu-id="9e228-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e228-142">RELATED LINKS</span></span>
