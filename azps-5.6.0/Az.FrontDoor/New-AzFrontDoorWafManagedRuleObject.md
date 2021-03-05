---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: f31b7c995c66e2b187038c45d9955a31f904764b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970874"
---
# <span data-ttu-id="f6e33-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f6e33-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="f6e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e33-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e33-103">Tworzenie obiektu ManagedRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="f6e33-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f6e33-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6e33-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e33-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6e33-105">DESCRIPTION</span></span>
<span data-ttu-id="f6e33-106">Tworzenie obiektu ManagedRule na celu utworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="f6e33-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f6e33-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6e33-107">EXAMPLES</span></span>

### <span data-ttu-id="f6e33-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6e33-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="f6e33-109">Tworzenie obiektu ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f6e33-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="f6e33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6e33-110">PARAMETERS</span></span>

### <span data-ttu-id="f6e33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e33-111">-DefaultProfile</span></span>
<span data-ttu-id="f6e33-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e33-113">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="f6e33-113">-Exclusion</span></span>
<span data-ttu-id="f6e33-114">Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="f6e33-114">Exclusion</span></span>

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

### <span data-ttu-id="f6e33-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f6e33-115">-RuleGroupOverride</span></span>
<span data-ttu-id="f6e33-116">Lista konfiguracji zastępowania dostawcy zarządzanego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f6e33-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="f6e33-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="f6e33-117">-Type</span></span>
<span data-ttu-id="f6e33-118">Typ reguły</span><span class="sxs-lookup"><span data-stu-id="f6e33-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="f6e33-119">— Wersja</span><span class="sxs-lookup"><span data-stu-id="f6e33-119">-Version</span></span>
<span data-ttu-id="f6e33-120">Wersja pakietu Ruleset</span><span class="sxs-lookup"><span data-stu-id="f6e33-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="f6e33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e33-121">CommonParameters</span></span>
<span data-ttu-id="f6e33-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e33-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6e33-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e33-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6e33-124">INPUTS</span></span>

### <span data-ttu-id="f6e33-125">Brak</span><span class="sxs-lookup"><span data-stu-id="f6e33-125">None</span></span>

## <span data-ttu-id="f6e33-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6e33-126">OUTPUTS</span></span>

### <span data-ttu-id="f6e33-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="f6e33-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="f6e33-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6e33-128">NOTES</span></span>

## <span data-ttu-id="f6e33-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6e33-129">RELATED LINKS</span></span>

<span data-ttu-id="f6e33-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="f6e33-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
