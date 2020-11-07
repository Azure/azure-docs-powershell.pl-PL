---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705371"
---
# <span data-ttu-id="d5fe4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="d5fe4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="d5fe4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fe4-103">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="d5fe4-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="d5fe4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5fe4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5fe4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fe4-106">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="d5fe4-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="d5fe4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="d5fe4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5fe4-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="d5fe4-109">Tworzenie obiektu RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d5fe4-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="d5fe4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="d5fe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fe4-111">-DefaultProfile</span></span>
<span data-ttu-id="d5fe4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fe4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5fe4-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d5fe4-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="d5fe4-114">Lista zastępowania reguł</span><span class="sxs-lookup"><span data-stu-id="d5fe4-114">Rule override list</span></span>

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

### <span data-ttu-id="d5fe4-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fe4-115">-RuleGroupName</span></span>
<span data-ttu-id="d5fe4-116">Nazwa grupy reguł, dla której obowiązują te zastąpienia</span><span class="sxs-lookup"><span data-stu-id="d5fe4-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="d5fe4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fe4-117">CommonParameters</span></span>
<span data-ttu-id="d5fe4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fe4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fe4-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5fe4-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fe4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5fe4-120">INPUTS</span></span>

### <span data-ttu-id="d5fe4-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d5fe4-121">None</span></span>

## <span data-ttu-id="d5fe4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5fe4-122">OUTPUTS</span></span>

### <span data-ttu-id="d5fe4-123">Microsoft. Azure. Commands. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d5fe4-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="d5fe4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5fe4-124">NOTES</span></span>

## <span data-ttu-id="d5fe4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5fe4-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5fe4-126">Nowe — AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5fe4-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)