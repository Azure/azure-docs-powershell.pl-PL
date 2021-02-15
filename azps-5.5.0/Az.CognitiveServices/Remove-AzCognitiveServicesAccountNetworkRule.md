---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239019"
---
# <span data-ttu-id="93689-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93689-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="93689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93689-102">SYNOPSIS</span></span>
<span data-ttu-id="93689-103">Usuwanie wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="93689-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="93689-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93689-104">SYNTAX</span></span>

### <span data-ttu-id="93689-105">NetWorkRuleString (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="93689-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93689-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="93689-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93689-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="93689-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93689-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="93689-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93689-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="93689-109">DESCRIPTION</span></span>
<span data-ttu-id="93689-110">Polecenie cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** usuwa wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="93689-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="93689-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93689-111">EXAMPLES</span></span>

### <span data-ttu-id="93689-112">Przykład 1. Usuwanie kilku adresów IpRules za pomocą adresu IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="93689-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="93689-113">To polecenie usuwa kilka adresów IpRules z adresem IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="93689-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="93689-114">Przykład 2. Usuwanie ciągu VirtualNetworkRule za pomocą danych wejściowych obiektu VirtualNetworkRule z JSON</span><span class="sxs-lookup"><span data-stu-id="93689-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="93689-115">To polecenie usuwa polecenie VirtualNetworkRule z wprowadzeniem obiektu VirtualNetworkRule z JSON.</span><span class="sxs-lookup"><span data-stu-id="93689-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="93689-116">Przykład 3. Usuwanie pierwszego ciągu IpRule z potokiem</span><span class="sxs-lookup"><span data-stu-id="93689-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="93689-117">To polecenie umożliwia usunięcie pierwszego polecenia IpRule z potokiem.</span><span class="sxs-lookup"><span data-stu-id="93689-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="93689-118">Przykład 4. Usuwanie kilku przycisków VirtualNetworkRules za pomocą funkcji VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="93689-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="93689-119">To polecenie usuwa kilka poleceń VirtualNetworkRules za pomocą funkcji VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="93689-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="93689-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93689-120">PARAMETERS</span></span>

### <span data-ttu-id="93689-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93689-121">-DefaultProfile</span></span>
<span data-ttu-id="93689-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93689-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93689-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="93689-123">-IpAddressOrRange</span></span>
<span data-ttu-id="93689-124">Konto usług Cognitive Services NetworkRule IpRules IpAddressOrRange w ciągu.</span><span class="sxs-lookup"><span data-stu-id="93689-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="93689-125">-IpRule</span></span>
<span data-ttu-id="93689-126">Konto usług Cognitive Services NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="93689-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93689-127">-Name</span></span>
<span data-ttu-id="93689-128">Nazwa konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="93689-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93689-129">-ResourceGroupName</span></span>
<span data-ttu-id="93689-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93689-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="93689-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="93689-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="93689-132">Konto usług Cognitive Services NetworkRule VirtualNetworkRules VirtualNetworkResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="93689-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-133">- VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93689-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="93689-134">Konto usług Cognitive Services NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="93689-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93689-135">-Confirm</span></span>
<span data-ttu-id="93689-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93689-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93689-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93689-137">-WhatIf</span></span>
<span data-ttu-id="93689-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93689-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93689-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93689-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93689-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93689-140">CommonParameters</span></span>
<span data-ttu-id="93689-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93689-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93689-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93689-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93689-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93689-143">INPUTS</span></span>

### <span data-ttu-id="93689-144">System.String</span><span class="sxs-lookup"><span data-stu-id="93689-144">System.String</span></span>

### <span data-ttu-id="93689-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="93689-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="93689-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="93689-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="93689-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93689-147">OUTPUTS</span></span>

### <span data-ttu-id="93689-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93689-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="93689-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="93689-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="93689-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93689-150">NOTES</span></span>

## <span data-ttu-id="93689-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93689-151">RELATED LINKS</span></span>
