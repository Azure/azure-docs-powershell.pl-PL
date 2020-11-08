---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062742"
---
# <span data-ttu-id="afa3f-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="afa3f-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="afa3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afa3f-102">SYNOPSIS</span></span>
<span data-ttu-id="afa3f-103">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="afa3f-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="afa3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afa3f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afa3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="afa3f-105">DESCRIPTION</span></span>
<span data-ttu-id="afa3f-106">Tworzenie obiektu RuleGroupOverride do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="afa3f-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="afa3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afa3f-107">EXAMPLES</span></span>

### <span data-ttu-id="afa3f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afa3f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="afa3f-109">Tworzenie obiektu RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="afa3f-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="afa3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afa3f-110">PARAMETERS</span></span>

### <span data-ttu-id="afa3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa3f-111">-DefaultProfile</span></span>
<span data-ttu-id="afa3f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afa3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa3f-113">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="afa3f-113">-Exclusion</span></span>
<span data-ttu-id="afa3f-114">Wyjątki</span><span class="sxs-lookup"><span data-stu-id="afa3f-114">Exclusion</span></span>

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

### <span data-ttu-id="afa3f-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="afa3f-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="afa3f-116">Lista zastępowania reguł</span><span class="sxs-lookup"><span data-stu-id="afa3f-116">Rule override list</span></span>

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

### <span data-ttu-id="afa3f-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="afa3f-117">-RuleGroupName</span></span>
<span data-ttu-id="afa3f-118">Nazwa grupy reguł, dla której obowiązują te zastąpienia</span><span class="sxs-lookup"><span data-stu-id="afa3f-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="afa3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa3f-119">CommonParameters</span></span>
<span data-ttu-id="afa3f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa3f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afa3f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa3f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afa3f-122">INPUTS</span></span>

### <span data-ttu-id="afa3f-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="afa3f-123">None</span></span>

## <span data-ttu-id="afa3f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afa3f-124">OUTPUTS</span></span>

### <span data-ttu-id="afa3f-125">Microsoft. Azure. Commands. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="afa3f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="afa3f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afa3f-126">NOTES</span></span>

## <span data-ttu-id="afa3f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afa3f-127">RELATED LINKS</span></span>

[<span data-ttu-id="afa3f-128">Nowe — AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="afa3f-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
