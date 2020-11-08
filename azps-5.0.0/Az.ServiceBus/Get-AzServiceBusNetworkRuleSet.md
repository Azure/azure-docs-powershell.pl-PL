---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225511"
---
# <span data-ttu-id="1e8a0-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e8a0-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="1e8a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8a0-103">Pobiera szczegóły NetworkruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1e8a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e8a0-104">SYNTAX</span></span>

### <span data-ttu-id="1e8a0-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e8a0-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e8a0-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1e8a0-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e8a0-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e8a0-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e8a0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e8a0-108">DESCRIPTION</span></span>
<span data-ttu-id="1e8a0-109">Pobiera szczegóły NetworkruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1e8a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e8a0-110">EXAMPLES</span></span>

### <span data-ttu-id="1e8a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e8a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="1e8a0-112">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="1e8a0-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1e8a0-113">Zapoznaj się z informacjami o NetworkruleSetych koncentratorów zdarzeń przy użyciu parametrów resourceName i Namespace.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="1e8a0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e8a0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="1e8a0-115">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="1e8a0-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1e8a0-116">Zapoznaj się z informacjami o NetworkruleSetych koncentratorów zdarzeń w obszarze nazw, które znajdują się w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="1e8a0-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1e8a0-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="1e8a0-118">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="1e8a0-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1e8a0-119">Uzyskiwanie szczegółowych informacji o NetworkruleSetych koncentratorów zdarzeń przy użyciu identyfikatora zasobu innej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1e8a0-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="1e8a0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e8a0-120">PARAMETERS</span></span>

### <span data-ttu-id="1e8a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8a0-121">-DefaultProfile</span></span>
<span data-ttu-id="1e8a0-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e8a0-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e8a0-123">-Namespace</span></span>
<span data-ttu-id="1e8a0-124">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="1e8a0-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="1e8a0-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1e8a0-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8a0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e8a0-127">-ResourceId</span></span>
<span data-ttu-id="1e8a0-128">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="1e8a0-128">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e8a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8a0-129">CommonParameters</span></span>
<span data-ttu-id="1e8a0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e8a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1e8a0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8a0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8a0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e8a0-132">INPUTS</span></span>

### <span data-ttu-id="1e8a0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1e8a0-133">System.String</span></span>

## <span data-ttu-id="1e8a0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e8a0-134">OUTPUTS</span></span>

### <span data-ttu-id="1e8a0-135">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1e8a0-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1e8a0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e8a0-136">NOTES</span></span>

## <span data-ttu-id="1e8a0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e8a0-137">RELATED LINKS</span></span>