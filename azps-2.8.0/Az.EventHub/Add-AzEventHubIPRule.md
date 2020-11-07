---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 824c1ea3462b2a15e74ca4c02eb69fe566f97d78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705468"
---
# <span data-ttu-id="77e5c-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="77e5c-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="77e5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="77e5c-103">Dodawanie jednej reguły IP do NetworkRuleSet w danym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="77e5c-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="77e5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77e5c-104">SYNTAX</span></span>

### <span data-ttu-id="77e5c-105">IPRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77e5c-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e5c-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e5c-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77e5c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77e5c-107">DESCRIPTION</span></span>
<span data-ttu-id="77e5c-108">Dodawanie jednej reguły IP do NetworkRuleSet w danym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="77e5c-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="77e5c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77e5c-109">EXAMPLES</span></span>

### <span data-ttu-id="77e5c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77e5c-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="77e5c-111">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="77e5c-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="77e5c-112">Dodaj IPRule z IpMask "11.22.33.44" i akcję Zezwól na pozwolenie na dany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="77e5c-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="77e5c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77e5c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="77e5c-114">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="77e5c-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="77e5c-115">Dodaj IPRule z IpMask "11.22.33.44" i akcję Zezwól na pozwolenie na dany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="77e5c-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="77e5c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77e5c-116">PARAMETERS</span></span>

### <span data-ttu-id="77e5c-117">-Action</span><span class="sxs-lookup"><span data-stu-id="77e5c-117">-Action</span></span>
<span data-ttu-id="77e5c-118">Akcja filtrowania IP</span><span class="sxs-lookup"><span data-stu-id="77e5c-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e5c-119">-DefaultProfile</span></span>
<span data-ttu-id="77e5c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77e5c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e5c-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="77e5c-121">-IpMask</span></span>
<span data-ttu-id="77e5c-122">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="77e5c-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="77e5c-123">-IpRuleObject</span></span>
<span data-ttu-id="77e5c-124">Obiekt konfiguracji IPRule, który ma zostać dodany</span><span class="sxs-lookup"><span data-stu-id="77e5c-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77e5c-125">-Name</span></span>
<span data-ttu-id="77e5c-126">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77e5c-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e5c-127">-ResourceGroupName</span></span>
<span data-ttu-id="77e5c-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="77e5c-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77e5c-129">-Confirm</span></span>
<span data-ttu-id="77e5c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e5c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e5c-131">-WhatIf</span></span>
<span data-ttu-id="77e5c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e5c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e5c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77e5c-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e5c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e5c-134">CommonParameters</span></span>
<span data-ttu-id="77e5c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e5c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77e5c-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e5c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e5c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77e5c-137">INPUTS</span></span>

### <span data-ttu-id="77e5c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="77e5c-138">System.String</span></span>

### <span data-ttu-id="77e5c-139">Microsoft. Azure. Commands. EventHub. modele. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="77e5c-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="77e5c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77e5c-140">OUTPUTS</span></span>

### <span data-ttu-id="77e5c-141">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="77e5c-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="77e5c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77e5c-142">NOTES</span></span>

## <span data-ttu-id="77e5c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77e5c-143">RELATED LINKS</span></span>