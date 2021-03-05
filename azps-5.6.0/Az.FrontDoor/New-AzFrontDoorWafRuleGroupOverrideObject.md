---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015281"
---
# <span data-ttu-id="b1a0c-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="b1a0c-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="b1a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a0c-103">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="b1a0c-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="b1a0c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b1a0c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a0c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b1a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a0c-106">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="b1a0c-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="b1a0c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b1a0c-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a0c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1a0c-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="b1a0c-109">Tworzenie obiektu RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b1a0c-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="b1a0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1a0c-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a0c-111">-DefaultProfile</span></span>
<span data-ttu-id="b1a0c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a0c-113">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="b1a0c-113">-Exclusion</span></span>
<span data-ttu-id="b1a0c-114">Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="b1a0c-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0c-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="b1a0c-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="b1a0c-116">Lista zastępowania reguł</span><span class="sxs-lookup"><span data-stu-id="b1a0c-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0c-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a0c-117">-RuleGroupName</span></span>
<span data-ttu-id="b1a0c-118">Nazwa grupy reguł, dla której mają zastosowanie te zastąpienia</span><span class="sxs-lookup"><span data-stu-id="b1a0c-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="b1a0c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a0c-119">CommonParameters</span></span>
<span data-ttu-id="b1a0c-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a0c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a0c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1a0c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a0c-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1a0c-122">INPUTS</span></span>

### <span data-ttu-id="b1a0c-123">Brak</span><span class="sxs-lookup"><span data-stu-id="b1a0c-123">None</span></span>

## <span data-ttu-id="b1a0c-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1a0c-124">OUTPUTS</span></span>

### <span data-ttu-id="b1a0c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b1a0c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="b1a0c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b1a0c-126">NOTES</span></span>

## <span data-ttu-id="b1a0c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1a0c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1a0c-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b1a0c-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
