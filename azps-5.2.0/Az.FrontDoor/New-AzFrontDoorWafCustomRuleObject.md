---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352750"
---
# <span data-ttu-id="7f6ce-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="7f6ce-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="7f6ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6ce-103">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="7f6ce-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="7f6ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f6ce-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f6ce-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6ce-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="7f6ce-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="7f6ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f6ce-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6ce-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f6ce-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="7f6ce-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="7f6ce-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="7f6ce-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f6ce-110">PARAMETERS</span></span>

### <span data-ttu-id="7f6ce-111">-Action</span><span class="sxs-lookup"><span data-stu-id="7f6ce-111">-Action</span></span>
<span data-ttu-id="7f6ce-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-112">Type of Actions.</span></span>
<span data-ttu-id="7f6ce-113">Możliwe wartości obejmują: "dozwolone", "Zablokuj", "log".</span><span class="sxs-lookup"><span data-stu-id="7f6ce-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="7f6ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6ce-114">-DefaultProfile</span></span>
<span data-ttu-id="7f6ce-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6ce-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7f6ce-116">-EnabledState</span></span>
<span data-ttu-id="7f6ce-117">Stan włączenia.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-117">Enabled State.</span></span> <span data-ttu-id="7f6ce-118">Możliwe wartości to: "włączone", "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="7f6ce-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="7f6ce-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="7f6ce-119">-MatchCondition</span></span>
<span data-ttu-id="7f6ce-120">Lista warunków zgodności.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-120">List of match conditions.</span></span>

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

### <span data-ttu-id="7f6ce-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f6ce-121">-Name</span></span>
<span data-ttu-id="7f6ce-122">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="7f6ce-122">Name of the rule</span></span>

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

### <span data-ttu-id="7f6ce-123">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="7f6ce-123">-Priority</span></span>
<span data-ttu-id="7f6ce-124">Opisuje priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="7f6ce-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="7f6ce-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="7f6ce-126">Limit szybkości.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-126">Rate limit duration.</span></span> <span data-ttu-id="7f6ce-127">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="7f6ce-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="7f6ce-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="7f6ce-128">-RateLimitThreshold</span></span>
<span data-ttu-id="7f6ce-129">Próg limitu szybkości</span><span class="sxs-lookup"><span data-stu-id="7f6ce-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="7f6ce-130">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="7f6ce-130">-RuleType</span></span>
<span data-ttu-id="7f6ce-131">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-131">Type of the rule.</span></span>
<span data-ttu-id="7f6ce-132">Możliwe wartości obejmują: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="7f6ce-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="7f6ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6ce-133">CommonParameters</span></span>
<span data-ttu-id="7f6ce-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6ce-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f6ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6ce-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f6ce-136">INPUTS</span></span>

### <span data-ttu-id="7f6ce-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f6ce-137">None</span></span>

## <span data-ttu-id="7f6ce-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f6ce-138">OUTPUTS</span></span>

### <span data-ttu-id="7f6ce-139">Microsoft. Azure. Commands. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="7f6ce-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="7f6ce-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f6ce-140">NOTES</span></span>

## <span data-ttu-id="7f6ce-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f6ce-141">RELATED LINKS</span></span>

<span data-ttu-id="7f6ce-142">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="7f6ce-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
