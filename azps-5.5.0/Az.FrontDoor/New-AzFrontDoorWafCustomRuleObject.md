---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180651"
---
# <span data-ttu-id="0e344-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e344-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="0e344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e344-102">SYNOPSIS</span></span>
<span data-ttu-id="0e344-103">Tworzenie obiektu CustomRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="0e344-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="0e344-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e344-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e344-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e344-105">DESCRIPTION</span></span>
<span data-ttu-id="0e344-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="0e344-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="0e344-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e344-107">EXAMPLES</span></span>

### <span data-ttu-id="0e344-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e344-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="0e344-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="0e344-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="0e344-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e344-110">PARAMETERS</span></span>

### <span data-ttu-id="0e344-111">— Akcja</span><span class="sxs-lookup"><span data-stu-id="0e344-111">-Action</span></span>
<span data-ttu-id="0e344-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="0e344-112">Type of Actions.</span></span>
<span data-ttu-id="0e344-113">Możliwe wartości: "Zezwalaj", "Blok", "Dziennik"</span><span class="sxs-lookup"><span data-stu-id="0e344-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="0e344-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e344-114">-DefaultProfile</span></span>
<span data-ttu-id="0e344-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e344-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e344-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0e344-116">-EnabledState</span></span>
<span data-ttu-id="0e344-117">Stan włączony.</span><span class="sxs-lookup"><span data-stu-id="0e344-117">Enabled State.</span></span> <span data-ttu-id="0e344-118">Możliwe wartości to: "Włączone", "Wyłączone".</span><span class="sxs-lookup"><span data-stu-id="0e344-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="0e344-119">- MatchCondition</span><span class="sxs-lookup"><span data-stu-id="0e344-119">-MatchCondition</span></span>
<span data-ttu-id="0e344-120">Lista warunków dopasowania.</span><span class="sxs-lookup"><span data-stu-id="0e344-120">List of match conditions.</span></span>

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

### <span data-ttu-id="0e344-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e344-121">-Name</span></span>
<span data-ttu-id="0e344-122">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="0e344-122">Name of the rule</span></span>

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

### <span data-ttu-id="0e344-123">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="0e344-123">-Priority</span></span>
<span data-ttu-id="0e344-124">W tym artykule opisano priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="0e344-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="0e344-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="0e344-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="0e344-126">Czas trwania limitu stawek.</span><span class="sxs-lookup"><span data-stu-id="0e344-126">Rate limit duration.</span></span> <span data-ttu-id="0e344-127">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="0e344-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="0e344-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="0e344-128">-RateLimitThreshold</span></span>
<span data-ttu-id="0e344-129">Próg limitu stawek</span><span class="sxs-lookup"><span data-stu-id="0e344-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="0e344-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0e344-130">-RuleType</span></span>
<span data-ttu-id="0e344-131">Wpisz regułę.</span><span class="sxs-lookup"><span data-stu-id="0e344-131">Type of the rule.</span></span>
<span data-ttu-id="0e344-132">Możliwe wartości to: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="0e344-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="0e344-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e344-133">CommonParameters</span></span>
<span data-ttu-id="0e344-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e344-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e344-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e344-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e344-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e344-136">INPUTS</span></span>

### <span data-ttu-id="0e344-137">Brak</span><span class="sxs-lookup"><span data-stu-id="0e344-137">None</span></span>

## <span data-ttu-id="0e344-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e344-138">OUTPUTS</span></span>

### <span data-ttu-id="0e344-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="0e344-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="0e344-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e344-140">NOTES</span></span>

## <span data-ttu-id="0e344-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e344-141">RELATED LINKS</span></span>

<span data-ttu-id="0e344-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="0e344-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
