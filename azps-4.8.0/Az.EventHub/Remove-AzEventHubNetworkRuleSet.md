---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223928"
---
# <span data-ttu-id="7104b-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7104b-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="7104b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7104b-102">SYNOPSIS</span></span>
<span data-ttu-id="7104b-103">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7104b-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="7104b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7104b-104">SYNTAX</span></span>

### <span data-ttu-id="7104b-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7104b-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7104b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7104b-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7104b-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7104b-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7104b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7104b-108">DESCRIPTION</span></span>
<span data-ttu-id="7104b-109">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7104b-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="7104b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7104b-110">EXAMPLES</span></span>

### <span data-ttu-id="7104b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7104b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="7104b-112">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="7104b-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="7104b-113">Usuwa NetworkRuleSet dla danej przestrzeni nazw "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="7104b-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="7104b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7104b-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="7104b-115">Usuwa NetworkRuleSet za pomocą funkcji Inputobject</span><span class="sxs-lookup"><span data-stu-id="7104b-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="7104b-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7104b-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="7104b-117">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="7104b-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="7104b-118">Usuwa NetworkRuleSet za pomocą ResourceId obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7104b-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="7104b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7104b-119">PARAMETERS</span></span>

### <span data-ttu-id="7104b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7104b-120">-AsJob</span></span>
<span data-ttu-id="7104b-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7104b-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7104b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7104b-122">-DefaultProfile</span></span>
<span data-ttu-id="7104b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7104b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7104b-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7104b-124">-InputObject</span></span>
<span data-ttu-id="7104b-125">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="7104b-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7104b-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7104b-126">-Name</span></span>
<span data-ttu-id="7104b-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7104b-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7104b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7104b-128">-PassThru</span></span>
<span data-ttu-id="7104b-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7104b-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7104b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7104b-130">-ResourceGroupName</span></span>
<span data-ttu-id="7104b-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7104b-131">Resource Group Name</span></span>

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

### <span data-ttu-id="7104b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7104b-132">-ResourceId</span></span>
<span data-ttu-id="7104b-133">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7104b-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="7104b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7104b-134">-Confirm</span></span>
<span data-ttu-id="7104b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7104b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7104b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7104b-136">-WhatIf</span></span>
<span data-ttu-id="7104b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7104b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7104b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7104b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7104b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7104b-139">CommonParameters</span></span>
<span data-ttu-id="7104b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7104b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7104b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7104b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7104b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7104b-142">INPUTS</span></span>

### <span data-ttu-id="7104b-143">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7104b-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="7104b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7104b-144">System.String</span></span>

## <span data-ttu-id="7104b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7104b-145">OUTPUTS</span></span>

### <span data-ttu-id="7104b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7104b-146">System.Boolean</span></span>

## <span data-ttu-id="7104b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7104b-147">NOTES</span></span>

## <span data-ttu-id="7104b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7104b-148">RELATED LINKS</span></span>