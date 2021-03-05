---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: fe2f405e07bc20437b9c0b47b8e551039b90b500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965050"
---
# <span data-ttu-id="0086d-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0086d-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="0086d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0086d-102">SYNOPSIS</span></span>
<span data-ttu-id="0086d-103">Dodawanie wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="0086d-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0086d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0086d-104">SYNTAX</span></span>

### <span data-ttu-id="0086d-105">NetWorkRuleString (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0086d-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0086d-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0086d-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0086d-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0086d-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0086d-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="0086d-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0086d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0086d-109">DESCRIPTION</span></span>
<span data-ttu-id="0086d-110">Polecenie **cmdlet Add-AzCognitiveServicesAccountNetworkRule** dodaje wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="0086d-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0086d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0086d-111">EXAMPLES</span></span>

### <span data-ttu-id="0086d-112">Przykład 1. Dodawanie kilku adresów IpRules za pomocą adresu IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0086d-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="0086d-113">To polecenie pozwala dodać kilka poleceń IpRules z adresem IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="0086d-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="0086d-114">Przykład 2. Dodawanie dodatku VirtualNetworkRule z virtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="0086d-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="0086d-115">To polecenie pozwala dodać pole VirtualNetworkRule z polem VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="0086d-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="0086d-116">Przykład 3. Dodawanie obiektów VirtualNetworkRules za pomocą funkcji VirtualNetworkRule Objects z innego konta</span><span class="sxs-lookup"><span data-stu-id="0086d-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="0086d-117">To polecenie pozwala dodać obiekty VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="0086d-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="0086d-118">Przykład 4. Dodawanie kilku adresów IpRule za pomocą obiektów IpRule, danych wejściowych za pomocą JSON</span><span class="sxs-lookup"><span data-stu-id="0086d-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="0086d-119">To polecenie pozwala dodać kilka obiektów IpRule z obiektami IpRule, dane wejściowe z wartością JSON.</span><span class="sxs-lookup"><span data-stu-id="0086d-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="0086d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0086d-120">PARAMETERS</span></span>

### <span data-ttu-id="0086d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0086d-121">-DefaultProfile</span></span>
<span data-ttu-id="0086d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0086d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0086d-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0086d-123">-IpAddressOrRange</span></span>
<span data-ttu-id="0086d-124">Konto usług Cognitive Services NetworkRule IpRules IpAddressOrRange w ciągu.</span><span class="sxs-lookup"><span data-stu-id="0086d-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="0086d-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="0086d-125">-IpRule</span></span>
<span data-ttu-id="0086d-126">Konto usług Cognitive Services NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="0086d-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="0086d-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0086d-127">-Name</span></span>
<span data-ttu-id="0086d-128">Nazwa konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="0086d-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="0086d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0086d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0086d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0086d-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="0086d-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0086d-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0086d-132">Konto usług Cognitive Services NetworkRule VirtualNetworkRules VirtualNetworkResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="0086d-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="0086d-133">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0086d-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="0086d-134">Konto usług Cognitive Services NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="0086d-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="0086d-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0086d-135">-Confirm</span></span>
<span data-ttu-id="0086d-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0086d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0086d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0086d-137">-WhatIf</span></span>
<span data-ttu-id="0086d-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0086d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0086d-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0086d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0086d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0086d-140">CommonParameters</span></span>
<span data-ttu-id="0086d-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0086d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0086d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0086d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0086d-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0086d-143">INPUTS</span></span>

### <span data-ttu-id="0086d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0086d-144">System.String</span></span>

### <span data-ttu-id="0086d-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="0086d-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="0086d-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="0086d-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0086d-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0086d-147">OUTPUTS</span></span>

### <span data-ttu-id="0086d-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0086d-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="0086d-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="0086d-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="0086d-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0086d-150">NOTES</span></span>

## <span data-ttu-id="0086d-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0086d-151">RELATED LINKS</span></span>
