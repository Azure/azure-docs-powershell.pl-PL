---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705382"
---
# <span data-ttu-id="5ee73-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="5ee73-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="5ee73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ee73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee73-103">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5ee73-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="5ee73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ee73-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ee73-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee73-106">Tworzenie obiektu CustomRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5ee73-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="5ee73-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ee73-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee73-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ee73-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="5ee73-109">Tworzenie obiektu CustomRule</span><span class="sxs-lookup"><span data-stu-id="5ee73-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="5ee73-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ee73-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee73-111">-Action</span><span class="sxs-lookup"><span data-stu-id="5ee73-111">-Action</span></span>
<span data-ttu-id="5ee73-112">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="5ee73-112">Type of Actions.</span></span>
<span data-ttu-id="5ee73-113">Możliwe wartości obejmują: "dozwolone", "Zablokuj", "log".</span><span class="sxs-lookup"><span data-stu-id="5ee73-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="5ee73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee73-114">-DefaultProfile</span></span>
<span data-ttu-id="5ee73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee73-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="5ee73-116">-MatchCondition</span></span>
<span data-ttu-id="5ee73-117">Lista warunków zgodności.</span><span class="sxs-lookup"><span data-stu-id="5ee73-117">List of match conditions.</span></span>

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

### <span data-ttu-id="5ee73-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ee73-118">-Name</span></span>
<span data-ttu-id="5ee73-119">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="5ee73-119">Name of the rule</span></span>

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

### <span data-ttu-id="5ee73-120">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="5ee73-120">-Priority</span></span>
<span data-ttu-id="5ee73-121">Opisuje priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="5ee73-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="5ee73-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="5ee73-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="5ee73-123">Limit szybkości.</span><span class="sxs-lookup"><span data-stu-id="5ee73-123">Rate limit duration.</span></span> <span data-ttu-id="5ee73-124">Domyślne — 1 minuta</span><span class="sxs-lookup"><span data-stu-id="5ee73-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="5ee73-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="5ee73-125">-RateLimitThreshold</span></span>
<span data-ttu-id="5ee73-126">Próg limitu szybkości</span><span class="sxs-lookup"><span data-stu-id="5ee73-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="5ee73-127">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="5ee73-127">-RuleType</span></span>
<span data-ttu-id="5ee73-128">Typ reguły.</span><span class="sxs-lookup"><span data-stu-id="5ee73-128">Type of the rule.</span></span>
<span data-ttu-id="5ee73-129">Możliwe wartości obejmują: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="5ee73-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="5ee73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee73-130">CommonParameters</span></span>
<span data-ttu-id="5ee73-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee73-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ee73-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee73-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ee73-133">INPUTS</span></span>

### <span data-ttu-id="5ee73-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5ee73-134">None</span></span>

## <span data-ttu-id="5ee73-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ee73-135">OUTPUTS</span></span>

### <span data-ttu-id="5ee73-136">Microsoft. Azure. Commands. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="5ee73-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="5ee73-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ee73-137">NOTES</span></span>

## <span data-ttu-id="5ee73-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ee73-138">RELATED LINKS</span></span>

<span data-ttu-id="5ee73-139">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="5ee73-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
