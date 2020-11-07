---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 3ad94696ea10d791ebe2930b6c054e00b9e69d18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705424"
---
# <span data-ttu-id="79940-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="79940-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="79940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79940-102">SYNOPSIS</span></span>
<span data-ttu-id="79940-103">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="79940-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="79940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79940-104">SYNTAX</span></span>

### <span data-ttu-id="79940-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79940-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79940-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79940-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79940-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79940-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79940-108">Opis</span><span class="sxs-lookup"><span data-stu-id="79940-108">DESCRIPTION</span></span>
<span data-ttu-id="79940-109">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="79940-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="79940-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79940-110">EXAMPLES</span></span>

### <span data-ttu-id="79940-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79940-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="79940-112">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="79940-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="79940-113">Usuwa NetworkRuleSet dla danej przestrzeni nazw "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="79940-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="79940-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79940-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="79940-115">Usuwa NetworkRuleSet za pomocą funkcji Inputobject</span><span class="sxs-lookup"><span data-stu-id="79940-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="79940-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="79940-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="79940-117">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="79940-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="79940-118">Usuwa NetworkRuleSet za pomocą ResourceId obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="79940-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="79940-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79940-119">PARAMETERS</span></span>

### <span data-ttu-id="79940-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79940-120">-AsJob</span></span>
<span data-ttu-id="79940-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79940-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79940-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79940-122">-DefaultProfile</span></span>
<span data-ttu-id="79940-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79940-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79940-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79940-124">-InputObject</span></span>
<span data-ttu-id="79940-125">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="79940-125">Namespace Object</span></span>

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

### <span data-ttu-id="79940-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79940-126">-Name</span></span>
<span data-ttu-id="79940-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="79940-127">Namespace Name</span></span>

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

### <span data-ttu-id="79940-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79940-128">-PassThru</span></span>
<span data-ttu-id="79940-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="79940-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="79940-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79940-130">-ResourceGroupName</span></span>
<span data-ttu-id="79940-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="79940-131">Resource Group Name</span></span>

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

### <span data-ttu-id="79940-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79940-132">-ResourceId</span></span>
<span data-ttu-id="79940-133">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="79940-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="79940-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79940-134">-Confirm</span></span>
<span data-ttu-id="79940-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79940-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79940-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79940-136">-WhatIf</span></span>
<span data-ttu-id="79940-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79940-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79940-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79940-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79940-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79940-139">CommonParameters</span></span>
<span data-ttu-id="79940-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79940-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="79940-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79940-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79940-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79940-142">INPUTS</span></span>

### <span data-ttu-id="79940-143">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="79940-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="79940-144">System. String</span><span class="sxs-lookup"><span data-stu-id="79940-144">System.String</span></span>

## <span data-ttu-id="79940-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79940-145">OUTPUTS</span></span>

### <span data-ttu-id="79940-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79940-146">System.Boolean</span></span>

## <span data-ttu-id="79940-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79940-147">NOTES</span></span>

## <span data-ttu-id="79940-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79940-148">RELATED LINKS</span></span>