---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868403"
---
# <span data-ttu-id="05460-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="05460-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="05460-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05460-102">SYNOPSIS</span></span>
<span data-ttu-id="05460-103">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="05460-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="05460-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05460-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05460-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05460-105">DESCRIPTION</span></span>
<span data-ttu-id="05460-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="05460-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="05460-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05460-107">EXAMPLES</span></span>

### <span data-ttu-id="05460-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05460-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="05460-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="05460-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="05460-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05460-110">PARAMETERS</span></span>

### <span data-ttu-id="05460-111">-Action</span><span class="sxs-lookup"><span data-stu-id="05460-111">-Action</span></span>
<span data-ttu-id="05460-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="05460-112">Type of Actions.</span></span>
<span data-ttu-id="05460-113">Możliwe wartości obejmują: "dozwolone", "Zablokuj", "log".</span><span class="sxs-lookup"><span data-stu-id="05460-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="05460-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05460-114">-DefaultProfile</span></span>
<span data-ttu-id="05460-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05460-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05460-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="05460-116">-MatchCondition</span></span>
<span data-ttu-id="05460-117">Lista warunków zgodności.</span><span class="sxs-lookup"><span data-stu-id="05460-117">List of match conditions.</span></span>

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

### <span data-ttu-id="05460-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05460-118">-Name</span></span>
<span data-ttu-id="05460-119">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="05460-119">Name of the rule</span></span>

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

### <span data-ttu-id="05460-120">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="05460-120">-Priority</span></span>
<span data-ttu-id="05460-121">Opisuje priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="05460-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="05460-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="05460-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="05460-123">Limit szybkości.</span><span class="sxs-lookup"><span data-stu-id="05460-123">Rate limit duration.</span></span> <span data-ttu-id="05460-124">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="05460-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="05460-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="05460-125">-RateLimitThreshold</span></span>
<span data-ttu-id="05460-126">Limit szybkości thresold</span><span class="sxs-lookup"><span data-stu-id="05460-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="05460-127">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="05460-127">-RuleType</span></span>
<span data-ttu-id="05460-128">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="05460-128">Type of the rule.</span></span>
<span data-ttu-id="05460-129">Możliwe wartości obejmują: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="05460-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="05460-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05460-130">CommonParameters</span></span>
<span data-ttu-id="05460-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05460-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05460-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05460-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05460-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05460-133">INPUTS</span></span>

### <span data-ttu-id="05460-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="05460-134">None</span></span>

## <span data-ttu-id="05460-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05460-135">OUTPUTS</span></span>

### <span data-ttu-id="05460-136">Microsoft. Azure. Commands. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="05460-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="05460-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05460-137">NOTES</span></span>

## <span data-ttu-id="05460-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05460-138">RELATED LINKS</span></span>

<span data-ttu-id="05460-139">[Nowe — AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="05460-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
