---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201698"
---
# <span data-ttu-id="5ab6d-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="5ab6d-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="5ab6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab6d-103">Dodawanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5ab6d-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="5ab6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ab6d-104">SYNTAX</span></span>

### <span data-ttu-id="5ab6d-105">IPRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5ab6d-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab6d-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ab6d-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab6d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ab6d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ab6d-108">Dodawanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5ab6d-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="5ab6d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ab6d-109">EXAMPLES</span></span>

### <span data-ttu-id="5ab6d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ab6d-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="5ab6d-111">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="5ab6d-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="5ab6d-112">dodaj adres IPRule z adresem IpMask "11.22.33.44", a akcja Zezwalaj nie zezwolić na dostęp do danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="5ab6d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ab6d-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="5ab6d-114">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="5ab6d-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="5ab6d-115">dodaj adres IPRule z adresem IpMask "11.22.33.44", a akcja Zezwalaj nie zezwolić na dostęp do danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="5ab6d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ab6d-116">PARAMETERS</span></span>

### <span data-ttu-id="5ab6d-117">— Akcja</span><span class="sxs-lookup"><span data-stu-id="5ab6d-117">-Action</span></span>
<span data-ttu-id="5ab6d-118">Akcja filtrowania adresów IP</span><span class="sxs-lookup"><span data-stu-id="5ab6d-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="5ab6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab6d-119">-DefaultProfile</span></span>
<span data-ttu-id="5ab6d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab6d-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="5ab6d-121">-IpMask</span></span>
<span data-ttu-id="5ab6d-122">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="5ab6d-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="5ab6d-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5ab6d-123">-IpRuleObject</span></span>
<span data-ttu-id="5ab6d-124">Obiekt konfiguracji protokołu IPRule do dodania</span><span class="sxs-lookup"><span data-stu-id="5ab6d-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab6d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ab6d-125">-Name</span></span>
<span data-ttu-id="5ab6d-126">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5ab6d-126">Namespace Name</span></span>

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

### <span data-ttu-id="5ab6d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab6d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ab6d-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5ab6d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5ab6d-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ab6d-129">-Confirm</span></span>
<span data-ttu-id="5ab6d-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab6d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab6d-131">-WhatIf</span></span>
<span data-ttu-id="5ab6d-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab6d-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab6d-134">CommonParameters</span></span>
<span data-ttu-id="5ab6d-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ab6d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab6d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab6d-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ab6d-137">INPUTS</span></span>

### <span data-ttu-id="5ab6d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5ab6d-138">System.String</span></span>

### <span data-ttu-id="5ab6d-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5ab6d-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="5ab6d-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ab6d-140">OUTPUTS</span></span>

### <span data-ttu-id="5ab6d-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5ab6d-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5ab6d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ab6d-142">NOTES</span></span>

## <span data-ttu-id="5ab6d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ab6d-143">RELATED LINKS</span></span>