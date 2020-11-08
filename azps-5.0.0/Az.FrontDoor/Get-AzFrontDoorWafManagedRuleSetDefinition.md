---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233526"
---
# <span data-ttu-id="1176c-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="1176c-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="1176c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1176c-102">SYNOPSIS</span></span>
<span data-ttu-id="1176c-103">Pobieranie definicji zestawu reguł zarządzanych WAF</span><span class="sxs-lookup"><span data-stu-id="1176c-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="1176c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1176c-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1176c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1176c-105">DESCRIPTION</span></span>
<span data-ttu-id="1176c-106">Pobiera listę definicji zestawu reguł zarządzanych WAF, które będą używane jako odwołania</span><span class="sxs-lookup"><span data-stu-id="1176c-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="1176c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1176c-107">EXAMPLES</span></span>

### <span data-ttu-id="1176c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1176c-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="1176c-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1176c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1176c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1176c-110">PARAMETERS</span></span>

### <span data-ttu-id="1176c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1176c-111">-DefaultProfile</span></span>
<span data-ttu-id="1176c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1176c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1176c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1176c-113">CommonParameters</span></span>
<span data-ttu-id="1176c-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1176c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1176c-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1176c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1176c-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1176c-116">INPUTS</span></span>

### <span data-ttu-id="1176c-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1176c-117">None</span></span>

## <span data-ttu-id="1176c-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1176c-118">OUTPUTS</span></span>

### <span data-ttu-id="1176c-119">Microsoft. Azure. Commands. FrontDoor. models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="1176c-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="1176c-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1176c-120">NOTES</span></span>

## <span data-ttu-id="1176c-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1176c-121">RELATED LINKS</span></span>

<span data-ttu-id="1176c-122">[Nowe — AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Nowe — AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Nowe — AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="1176c-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
