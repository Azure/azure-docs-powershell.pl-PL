---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242243"
---
# <span data-ttu-id="402b7-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="402b7-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="402b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="402b7-102">SYNOPSIS</span></span>
<span data-ttu-id="402b7-103">Pobiera szczegóły centrum zdarzeń NetworkruleSet przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="402b7-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="402b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="402b7-104">SYNTAX</span></span>

### <span data-ttu-id="402b7-105">NetworkRuleSetPropertiesSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="402b7-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="402b7-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="402b7-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="402b7-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="402b7-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="402b7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="402b7-108">DESCRIPTION</span></span>
<span data-ttu-id="402b7-109">Pobiera szczegóły centrum zdarzeń NetworkruleSet przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="402b7-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="402b7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="402b7-110">EXAMPLES</span></span>

### <span data-ttu-id="402b7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="402b7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="402b7-112">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="402b7-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="402b7-113">Uzyskaj szczegółowe informacje na temat zestawu networkruleset centrum zdarzeń przestrzeni nazw przy użyciu parametrów ResourceGroup i Przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="402b7-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="402b7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="402b7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="402b7-115">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="402b7-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="402b7-116">Uzyskaj szczegółowe informacje na temat zestawu networkruleset centrum zdarzeń przestrzeni nazw przy użyciu przestrzeni nazw, która znajduje się w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="402b7-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="402b7-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="402b7-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="402b7-118">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="402b7-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="402b7-119">Uzyskiwanie szczegółów dotyczących centrum zdarzeń NetworkruleSet przestrzeni nazw przy użyciu identyfikatora zasobu innej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="402b7-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="402b7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="402b7-120">PARAMETERS</span></span>

### <span data-ttu-id="402b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402b7-121">-DefaultProfile</span></span>
<span data-ttu-id="402b7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="402b7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="402b7-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="402b7-123">-Namespace</span></span>
<span data-ttu-id="402b7-124">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="402b7-124">Namespace Name</span></span>

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

### <span data-ttu-id="402b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="402b7-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="402b7-126">Resource Group Name</span></span>

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

### <span data-ttu-id="402b7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="402b7-127">-ResourceId</span></span>
<span data-ttu-id="402b7-128">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="402b7-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="402b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402b7-129">CommonParameters</span></span>
<span data-ttu-id="402b7-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="402b7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="402b7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402b7-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="402b7-132">INPUTS</span></span>

### <span data-ttu-id="402b7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="402b7-133">System.String</span></span>

## <span data-ttu-id="402b7-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="402b7-134">OUTPUTS</span></span>

### <span data-ttu-id="402b7-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="402b7-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="402b7-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="402b7-136">NOTES</span></span>

## <span data-ttu-id="402b7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="402b7-137">RELATED LINKS</span></span>