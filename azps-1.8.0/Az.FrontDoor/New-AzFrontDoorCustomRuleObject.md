---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400675"
---
# <span data-ttu-id="22c2d-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="22c2d-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="22c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="22c2d-103">Tworzenie obiektu CustomRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="22c2d-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="22c2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22c2d-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22c2d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="22c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="22c2d-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="22c2d-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="22c2d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="22c2d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22c2d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="22c2d-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="22c2d-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="22c2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22c2d-110">PARAMETERS</span></span>

### <span data-ttu-id="22c2d-111">— akcja</span><span class="sxs-lookup"><span data-stu-id="22c2d-111">-Action</span></span>
<span data-ttu-id="22c2d-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="22c2d-112">Type of Actions.</span></span>
<span data-ttu-id="22c2d-113">Możliwe wartości: "Zezwalaj", "Blokowy", "Dziennik"</span><span class="sxs-lookup"><span data-stu-id="22c2d-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c2d-114">-DefaultProfile</span></span>
<span data-ttu-id="22c2d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22c2d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c2d-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="22c2d-116">-MatchCondition</span></span>
<span data-ttu-id="22c2d-117">Lista warunków dopasowania.</span><span class="sxs-lookup"><span data-stu-id="22c2d-117">List of match conditions.</span></span>

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

### <span data-ttu-id="22c2d-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22c2d-118">-Name</span></span>
<span data-ttu-id="22c2d-119">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="22c2d-119">Name of the rule</span></span>

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

### <span data-ttu-id="22c2d-120">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="22c2d-120">-Priority</span></span>
<span data-ttu-id="22c2d-121">W tym artykule opisano priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="22c2d-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="22c2d-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="22c2d-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="22c2d-123">Czas trwania limitu stawek.</span><span class="sxs-lookup"><span data-stu-id="22c2d-123">Rate limit duration.</span></span> <span data-ttu-id="22c2d-124">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="22c2d-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="22c2d-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="22c2d-125">-RateLimitThreshold</span></span>
<span data-ttu-id="22c2d-126">Przerzucanie limitu stawek</span><span class="sxs-lookup"><span data-stu-id="22c2d-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="22c2d-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="22c2d-127">-RuleType</span></span>
<span data-ttu-id="22c2d-128">Wpisz regułę.</span><span class="sxs-lookup"><span data-stu-id="22c2d-128">Type of the rule.</span></span>
<span data-ttu-id="22c2d-129">Możliwe wartości to: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="22c2d-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c2d-130">CommonParameters</span></span>
<span data-ttu-id="22c2d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c2d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22c2d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c2d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22c2d-133">INPUTS</span></span>

### <span data-ttu-id="22c2d-134">Brak</span><span class="sxs-lookup"><span data-stu-id="22c2d-134">None</span></span>

## <span data-ttu-id="22c2d-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22c2d-135">OUTPUTS</span></span>

### <span data-ttu-id="22c2d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="22c2d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="22c2d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22c2d-137">NOTES</span></span>

## <span data-ttu-id="22c2d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22c2d-138">RELATED LINKS</span></span>

<span data-ttu-id="22c2d-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="22c2d-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
