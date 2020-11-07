---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868364"
---
# <span data-ttu-id="1ffb1-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="1ffb1-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="1ffb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ffb1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffb1-103">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="1ffb1-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1ffb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ffb1-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ffb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ffb1-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffb1-106">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="1ffb1-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1ffb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ffb1-107">EXAMPLES</span></span>

### <span data-ttu-id="1ffb1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ffb1-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="1ffb1-109">Tworzenie obiektu RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1ffb1-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="1ffb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ffb1-110">PARAMETERS</span></span>

### <span data-ttu-id="1ffb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffb1-111">-DefaultProfile</span></span>
<span data-ttu-id="1ffb1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ffb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffb1-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1ffb1-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="1ffb1-114">Lista zastępowania reguł</span><span class="sxs-lookup"><span data-stu-id="1ffb1-114">Rule override list</span></span>

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

### <span data-ttu-id="1ffb1-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffb1-115">-RuleGroupName</span></span>
<span data-ttu-id="1ffb1-116">Nazwa grupy reguł, dla której obowiązują te zastąpienia</span><span class="sxs-lookup"><span data-stu-id="1ffb1-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="1ffb1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffb1-117">CommonParameters</span></span>
<span data-ttu-id="1ffb1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffb1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffb1-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ffb1-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffb1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ffb1-120">INPUTS</span></span>

### <span data-ttu-id="1ffb1-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ffb1-121">None</span></span>

## <span data-ttu-id="1ffb1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ffb1-122">OUTPUTS</span></span>

### <span data-ttu-id="1ffb1-123">Microsoft. Azure. Commands. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1ffb1-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="1ffb1-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ffb1-124">NOTES</span></span>

## <span data-ttu-id="1ffb1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ffb1-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ffb1-126">Nowe — AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1ffb1-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
