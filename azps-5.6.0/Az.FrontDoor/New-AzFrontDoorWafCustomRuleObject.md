---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970929"
---
# <span data-ttu-id="433f7-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="433f7-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="433f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433f7-102">SYNOPSIS</span></span>
<span data-ttu-id="433f7-103">Tworzenie obiektu CustomRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="433f7-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="433f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="433f7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433f7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="433f7-105">DESCRIPTION</span></span>
<span data-ttu-id="433f7-106">Tworzenie obiektu CustomRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="433f7-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="433f7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="433f7-107">EXAMPLES</span></span>

### <span data-ttu-id="433f7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="433f7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="433f7-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="433f7-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="433f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433f7-110">PARAMETERS</span></span>

### <span data-ttu-id="433f7-111">— Akcja</span><span class="sxs-lookup"><span data-stu-id="433f7-111">-Action</span></span>
<span data-ttu-id="433f7-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="433f7-112">Type of Actions.</span></span>
<span data-ttu-id="433f7-113">Możliwe wartości: "Zezwalaj", "Blokowy", "Dziennik"</span><span class="sxs-lookup"><span data-stu-id="433f7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="433f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433f7-114">-DefaultProfile</span></span>
<span data-ttu-id="433f7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="433f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433f7-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="433f7-116">-EnabledState</span></span>
<span data-ttu-id="433f7-117">Stan włączony.</span><span class="sxs-lookup"><span data-stu-id="433f7-117">Enabled State.</span></span> <span data-ttu-id="433f7-118">Możliwe wartości to: "Włączone", "Wyłączone".</span><span class="sxs-lookup"><span data-stu-id="433f7-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433f7-119">- MatchCondition</span><span class="sxs-lookup"><span data-stu-id="433f7-119">-MatchCondition</span></span>
<span data-ttu-id="433f7-120">Lista warunków dopasowania.</span><span class="sxs-lookup"><span data-stu-id="433f7-120">List of match conditions.</span></span>

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

### <span data-ttu-id="433f7-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="433f7-121">-Name</span></span>
<span data-ttu-id="433f7-122">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="433f7-122">Name of the rule</span></span>

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

### <span data-ttu-id="433f7-123">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="433f7-123">-Priority</span></span>
<span data-ttu-id="433f7-124">W tym artykule opisano priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="433f7-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="433f7-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="433f7-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="433f7-126">Czas trwania limitu stawek.</span><span class="sxs-lookup"><span data-stu-id="433f7-126">Rate limit duration.</span></span> <span data-ttu-id="433f7-127">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="433f7-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="433f7-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="433f7-128">-RateLimitThreshold</span></span>
<span data-ttu-id="433f7-129">Próg limitu stawek</span><span class="sxs-lookup"><span data-stu-id="433f7-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="433f7-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="433f7-130">-RuleType</span></span>
<span data-ttu-id="433f7-131">Wpisz regułę.</span><span class="sxs-lookup"><span data-stu-id="433f7-131">Type of the rule.</span></span>
<span data-ttu-id="433f7-132">Możliwe wartości to: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="433f7-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="433f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433f7-133">CommonParameters</span></span>
<span data-ttu-id="433f7-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433f7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433f7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433f7-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="433f7-136">INPUTS</span></span>

### <span data-ttu-id="433f7-137">Brak</span><span class="sxs-lookup"><span data-stu-id="433f7-137">None</span></span>

## <span data-ttu-id="433f7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="433f7-138">OUTPUTS</span></span>

### <span data-ttu-id="433f7-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="433f7-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="433f7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="433f7-140">NOTES</span></span>

## <span data-ttu-id="433f7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="433f7-141">RELATED LINKS</span></span>

<span data-ttu-id="433f7-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="433f7-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
