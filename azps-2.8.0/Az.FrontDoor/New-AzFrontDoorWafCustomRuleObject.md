---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: c59e0f90ae8b6d7839c7bb845b56e31a42b2d033
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412796"
---
# <span data-ttu-id="f139d-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="f139d-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="f139d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f139d-102">SYNOPSIS</span></span>
<span data-ttu-id="f139d-103">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="f139d-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f139d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f139d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f139d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f139d-105">DESCRIPTION</span></span>
<span data-ttu-id="f139d-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="f139d-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f139d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f139d-107">EXAMPLES</span></span>

### <span data-ttu-id="f139d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f139d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="f139d-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="f139d-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="f139d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f139d-110">PARAMETERS</span></span>

### <span data-ttu-id="f139d-111">— akcja</span><span class="sxs-lookup"><span data-stu-id="f139d-111">-Action</span></span>
<span data-ttu-id="f139d-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="f139d-112">Type of Actions.</span></span>
<span data-ttu-id="f139d-113">Możliwe wartości: "Zezwalaj", "Blok", "Dziennik"</span><span class="sxs-lookup"><span data-stu-id="f139d-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f139d-114">-DefaultProfile</span></span>
<span data-ttu-id="f139d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f139d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f139d-116">- MatchCondition</span><span class="sxs-lookup"><span data-stu-id="f139d-116">-MatchCondition</span></span>
<span data-ttu-id="f139d-117">Lista warunków dopasowania.</span><span class="sxs-lookup"><span data-stu-id="f139d-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f139d-118">-Name</span></span>
<span data-ttu-id="f139d-119">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="f139d-119">Name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-120">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="f139d-120">-Priority</span></span>
<span data-ttu-id="f139d-121">W tym artykule opisano priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="f139d-121">Describes priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="f139d-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="f139d-123">Czas trwania limitu stawek.</span><span class="sxs-lookup"><span data-stu-id="f139d-123">Rate limit duration.</span></span> <span data-ttu-id="f139d-124">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="f139d-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="f139d-125">-RateLimitThreshold</span></span>
<span data-ttu-id="f139d-126">Próg limitu stawek</span><span class="sxs-lookup"><span data-stu-id="f139d-126">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f139d-127">-RuleType</span></span>
<span data-ttu-id="f139d-128">Wpisz regułę.</span><span class="sxs-lookup"><span data-stu-id="f139d-128">Type of the rule.</span></span>
<span data-ttu-id="f139d-129">Możliwe wartości to: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="f139d-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f139d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f139d-130">CommonParameters</span></span>
<span data-ttu-id="f139d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f139d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f139d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f139d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f139d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f139d-133">INPUTS</span></span>

### <span data-ttu-id="f139d-134">Brak</span><span class="sxs-lookup"><span data-stu-id="f139d-134">None</span></span>

## <span data-ttu-id="f139d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f139d-135">OUTPUTS</span></span>

### <span data-ttu-id="f139d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="f139d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="f139d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f139d-137">NOTES</span></span>

## <span data-ttu-id="f139d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f139d-138">RELATED LINKS</span></span>

<span data-ttu-id="f139d-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f139d-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
