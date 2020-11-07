---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705377"
---
# <span data-ttu-id="30719-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="30719-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="30719-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30719-102">SYNOPSIS</span></span>
<span data-ttu-id="30719-103">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="30719-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="30719-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30719-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30719-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30719-105">DESCRIPTION</span></span>
<span data-ttu-id="30719-106">Tworzenie obiektu ManagedRule do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="30719-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="30719-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30719-107">EXAMPLES</span></span>

### <span data-ttu-id="30719-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30719-108">Example 1</span></span>
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

<span data-ttu-id="30719-109">Tworzenie obiektu ManagedRule</span><span class="sxs-lookup"><span data-stu-id="30719-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="30719-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30719-110">PARAMETERS</span></span>

### <span data-ttu-id="30719-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30719-111">-DefaultProfile</span></span>
<span data-ttu-id="30719-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30719-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30719-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="30719-113">-RuleGroupOverride</span></span>
<span data-ttu-id="30719-114">Lista zastępowania konfiguracji zarządzanego dostawcy usługi Azure</span><span class="sxs-lookup"><span data-stu-id="30719-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="30719-115">-Type</span><span class="sxs-lookup"><span data-stu-id="30719-115">-Type</span></span>
<span data-ttu-id="30719-116">Typ zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="30719-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="30719-117">-Version</span><span class="sxs-lookup"><span data-stu-id="30719-117">-Version</span></span>
<span data-ttu-id="30719-118">Wersja zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="30719-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="30719-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30719-119">CommonParameters</span></span>
<span data-ttu-id="30719-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30719-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30719-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30719-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30719-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30719-122">INPUTS</span></span>

### <span data-ttu-id="30719-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30719-123">None</span></span>

## <span data-ttu-id="30719-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30719-124">OUTPUTS</span></span>

### <span data-ttu-id="30719-125">Microsoft. Azure. Commands. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="30719-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="30719-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30719-126">NOTES</span></span>

## <span data-ttu-id="30719-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30719-127">RELATED LINKS</span></span>

<span data-ttu-id="30719-128">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Nowe — AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="30719-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
