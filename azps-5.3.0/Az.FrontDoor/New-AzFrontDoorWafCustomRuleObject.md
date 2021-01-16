---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501037"
---
# <span data-ttu-id="e0035-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e0035-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="e0035-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0035-102">SYNOPSIS</span></span>
<span data-ttu-id="e0035-103">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="e0035-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e0035-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0035-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0035-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0035-105">DESCRIPTION</span></span>
<span data-ttu-id="e0035-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="e0035-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e0035-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0035-107">EXAMPLES</span></span>

### <span data-ttu-id="e0035-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0035-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="e0035-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="e0035-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="e0035-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0035-110">PARAMETERS</span></span>

### <span data-ttu-id="e0035-111">-Action</span><span class="sxs-lookup"><span data-stu-id="e0035-111">-Action</span></span>
<span data-ttu-id="e0035-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="e0035-112">Type of Actions.</span></span>
<span data-ttu-id="e0035-113">Możliwe wartości obejmują: "dozwolone", "Zablokuj", "log".</span><span class="sxs-lookup"><span data-stu-id="e0035-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="e0035-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0035-114">-DefaultProfile</span></span>
<span data-ttu-id="e0035-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0035-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0035-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e0035-116">-EnabledState</span></span>
<span data-ttu-id="e0035-117">Stan włączenia.</span><span class="sxs-lookup"><span data-stu-id="e0035-117">Enabled State.</span></span> <span data-ttu-id="e0035-118">Możliwe wartości to: "włączone", "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="e0035-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="e0035-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e0035-119">-MatchCondition</span></span>
<span data-ttu-id="e0035-120">Lista warunków zgodności.</span><span class="sxs-lookup"><span data-stu-id="e0035-120">List of match conditions.</span></span>

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

### <span data-ttu-id="e0035-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0035-121">-Name</span></span>
<span data-ttu-id="e0035-122">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="e0035-122">Name of the rule</span></span>

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

### <span data-ttu-id="e0035-123">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="e0035-123">-Priority</span></span>
<span data-ttu-id="e0035-124">Opisuje priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="e0035-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="e0035-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e0035-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="e0035-126">Limit szybkości.</span><span class="sxs-lookup"><span data-stu-id="e0035-126">Rate limit duration.</span></span> <span data-ttu-id="e0035-127">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="e0035-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="e0035-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="e0035-128">-RateLimitThreshold</span></span>
<span data-ttu-id="e0035-129">Próg limitu szybkości</span><span class="sxs-lookup"><span data-stu-id="e0035-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="e0035-130">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="e0035-130">-RuleType</span></span>
<span data-ttu-id="e0035-131">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="e0035-131">Type of the rule.</span></span>
<span data-ttu-id="e0035-132">Możliwe wartości obejmują: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="e0035-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="e0035-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0035-133">CommonParameters</span></span>
<span data-ttu-id="e0035-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0035-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0035-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0035-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0035-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0035-136">INPUTS</span></span>

### <span data-ttu-id="e0035-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e0035-137">None</span></span>

## <span data-ttu-id="e0035-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0035-138">OUTPUTS</span></span>

### <span data-ttu-id="e0035-139">Microsoft. Azure. Commands. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="e0035-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="e0035-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0035-140">NOTES</span></span>

## <span data-ttu-id="e0035-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0035-141">RELATED LINKS</span></span>

<span data-ttu-id="e0035-142">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e0035-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
