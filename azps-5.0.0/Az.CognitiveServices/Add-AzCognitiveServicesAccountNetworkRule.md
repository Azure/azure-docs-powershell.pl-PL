---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233673"
---
# <span data-ttu-id="049e7-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="049e7-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="049e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="049e7-102">SYNOPSIS</span></span>
<span data-ttu-id="049e7-103">Dodaj IpRules lub VirtualNetworkRules do właściwości NetworkRule na koncie usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="049e7-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="049e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="049e7-104">SYNTAX</span></span>

### <span data-ttu-id="049e7-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="049e7-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="049e7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="049e7-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="049e7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="049e7-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="049e7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="049e7-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="049e7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="049e7-109">DESCRIPTION</span></span>
<span data-ttu-id="049e7-110">Polecenie cmdlet **Add-AzCognitiveServicesAccountNetworkRule** umożliwia dodanie IpRules lub VirtualNetworkRules do właściwości NetworkRule konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="049e7-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="049e7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="049e7-111">EXAMPLES</span></span>

### <span data-ttu-id="049e7-112">Przykład 1. Dodaj kilka IpRules za pomocą IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="049e7-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="049e7-113">To polecenie umożliwia dodanie kilku IpRules z IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="049e7-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="049e7-114">Przykład 2: Dodawanie VirtualNetworkRule za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="049e7-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="049e7-115">To polecenie umożliwia dodanie VirtualNetworkRule z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="049e7-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="049e7-116">Przykład 3: Dodawanie VirtualNetworkRules za pomocą obiektów VirtualNetworkRule z innego konta</span><span class="sxs-lookup"><span data-stu-id="049e7-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="049e7-117">To polecenie umożliwia dodanie VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="049e7-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="049e7-118">Przykład 4: Dodawanie kilku IpRule za pomocą obiektów IpRule, wprowadzanie za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="049e7-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="049e7-119">To polecenie umożliwia dodanie kilku IpRule z obiektami IpRule, które są wprowadzane za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="049e7-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="049e7-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="049e7-120">PARAMETERS</span></span>

### <span data-ttu-id="049e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049e7-121">-DefaultProfile</span></span>
<span data-ttu-id="049e7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="049e7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="049e7-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="049e7-123">-IpAddressOrRange</span></span>
<span data-ttu-id="049e7-124">Konto usług poznawczych NetworkRule IpRules IpAddressOrRange w ciągu.</span><span class="sxs-lookup"><span data-stu-id="049e7-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="049e7-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="049e7-125">-IpRule</span></span>
<span data-ttu-id="049e7-126">Konto usług poznawczych NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="049e7-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="049e7-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="049e7-127">-Name</span></span>
<span data-ttu-id="049e7-128">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="049e7-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="049e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="049e7-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="049e7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="049e7-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="049e7-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="049e7-132">Konto usług poznawczych NetworkRule VirtualNetworkRules VirtualNetworkResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="049e7-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="049e7-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="049e7-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="049e7-134">Konto usług poznawczych NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="049e7-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="049e7-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="049e7-135">-Confirm</span></span>
<span data-ttu-id="049e7-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="049e7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="049e7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="049e7-137">-WhatIf</span></span>
<span data-ttu-id="049e7-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="049e7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="049e7-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="049e7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="049e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049e7-140">CommonParameters</span></span>
<span data-ttu-id="049e7-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049e7-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="049e7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049e7-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="049e7-143">INPUTS</span></span>

### <span data-ttu-id="049e7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="049e7-144">System.String</span></span>

### <span data-ttu-id="049e7-145">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="049e7-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="049e7-146">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="049e7-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="049e7-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="049e7-147">OUTPUTS</span></span>

### <span data-ttu-id="049e7-148">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="049e7-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="049e7-149">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="049e7-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="049e7-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="049e7-150">NOTES</span></span>

## <span data-ttu-id="049e7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="049e7-151">RELATED LINKS</span></span>
