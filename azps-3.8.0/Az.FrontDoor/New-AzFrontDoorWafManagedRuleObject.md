---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 6e56ff9b174ec13d0844a1ac860d34043f8b73cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052802"
---
# <span data-ttu-id="dea77-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dea77-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="dea77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dea77-102">SYNOPSIS</span></span>
<span data-ttu-id="dea77-103">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="dea77-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dea77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dea77-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dea77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dea77-105">DESCRIPTION</span></span>
<span data-ttu-id="dea77-106">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="dea77-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dea77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dea77-107">EXAMPLES</span></span>

### <span data-ttu-id="dea77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dea77-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="dea77-109">Tworzenie obiektu ManagedRule</span><span class="sxs-lookup"><span data-stu-id="dea77-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="dea77-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dea77-110">PARAMETERS</span></span>

### <span data-ttu-id="dea77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea77-111">-DefaultProfile</span></span>
<span data-ttu-id="dea77-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dea77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea77-113">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="dea77-113">-Exclusion</span></span>
<span data-ttu-id="dea77-114">Wyjątki</span><span class="sxs-lookup"><span data-stu-id="dea77-114">Exclusion</span></span>

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

### <span data-ttu-id="dea77-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="dea77-115">-RuleGroupOverride</span></span>
<span data-ttu-id="dea77-116">Lista zastępowania konfiguracji zarządzanego dostawcy usługi Azure</span><span class="sxs-lookup"><span data-stu-id="dea77-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea77-117">-Type</span><span class="sxs-lookup"><span data-stu-id="dea77-117">-Type</span></span>
<span data-ttu-id="dea77-118">Typ zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="dea77-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="dea77-119">-Version</span><span class="sxs-lookup"><span data-stu-id="dea77-119">-Version</span></span>
<span data-ttu-id="dea77-120">Wersja zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="dea77-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="dea77-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea77-121">CommonParameters</span></span>
<span data-ttu-id="dea77-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea77-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea77-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dea77-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea77-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dea77-124">INPUTS</span></span>

### <span data-ttu-id="dea77-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dea77-125">None</span></span>

## <span data-ttu-id="dea77-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dea77-126">OUTPUTS</span></span>

### <span data-ttu-id="dea77-127">Microsoft. Azure. Commands. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="dea77-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="dea77-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dea77-128">NOTES</span></span>

## <span data-ttu-id="dea77-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dea77-129">RELATED LINKS</span></span>

<span data-ttu-id="dea77-130">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Nowe — AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="dea77-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
