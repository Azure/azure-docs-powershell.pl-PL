---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049286"
---
# <span data-ttu-id="4503f-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4503f-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="4503f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4503f-102">SYNOPSIS</span></span>
<span data-ttu-id="4503f-103">Dodaj IpRules lub VirtualNetworkRules do właściwości NetworkRule na koncie usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="4503f-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4503f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4503f-104">SYNTAX</span></span>

### <span data-ttu-id="4503f-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4503f-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4503f-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="4503f-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4503f-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="4503f-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4503f-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="4503f-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4503f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4503f-109">DESCRIPTION</span></span>
<span data-ttu-id="4503f-110">Polecenie cmdlet **Add-AzCognitiveServicesAccountNetworkRule** umożliwia dodanie IpRules lub VirtualNetworkRules do właściwości NetworkRule konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="4503f-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4503f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4503f-111">EXAMPLES</span></span>

### <span data-ttu-id="4503f-112">Przykład 1. Dodaj kilka IpRules za pomocą IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4503f-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="4503f-113">To polecenie umożliwia dodanie kilku IpRules z IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="4503f-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="4503f-114">Przykład 2: Dodawanie VirtualNetworkRule za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="4503f-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="4503f-115">To polecenie umożliwia dodanie VirtualNetworkRule z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="4503f-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="4503f-116">Przykład 3: Dodawanie VirtualNetworkRules za pomocą obiektów VirtualNetworkRule z innego konta</span><span class="sxs-lookup"><span data-stu-id="4503f-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="4503f-117">To polecenie umożliwia dodanie VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="4503f-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="4503f-118">Przykład 4: Dodawanie kilku IpRule za pomocą obiektów IpRule, wprowadzanie za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="4503f-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="4503f-119">To polecenie umożliwia dodanie kilku IpRule z obiektami IpRule, które są wprowadzane za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="4503f-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="4503f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4503f-120">PARAMETERS</span></span>

### <span data-ttu-id="4503f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4503f-121">-DefaultProfile</span></span>
<span data-ttu-id="4503f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4503f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4503f-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4503f-123">-IpAddressOrRange</span></span>
<span data-ttu-id="4503f-124">Konto usług poznawczych NetworkRule IpRules IpAddressOrRange w ciągu.</span><span class="sxs-lookup"><span data-stu-id="4503f-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="4503f-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="4503f-125">-IpRule</span></span>
<span data-ttu-id="4503f-126">Konto usług poznawczych NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="4503f-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="4503f-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4503f-127">-Name</span></span>
<span data-ttu-id="4503f-128">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="4503f-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="4503f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4503f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4503f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4503f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="4503f-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4503f-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="4503f-132">Konto usług poznawczych NetworkRule VirtualNetworkRules VirtualNetworkResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="4503f-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="4503f-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4503f-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="4503f-134">Konto usług poznawczych NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="4503f-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="4503f-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4503f-135">-Confirm</span></span>
<span data-ttu-id="4503f-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4503f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4503f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4503f-137">-WhatIf</span></span>
<span data-ttu-id="4503f-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4503f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4503f-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4503f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4503f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4503f-140">CommonParameters</span></span>
<span data-ttu-id="4503f-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4503f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4503f-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4503f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4503f-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4503f-143">INPUTS</span></span>

### <span data-ttu-id="4503f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4503f-144">System.String</span></span>

### <span data-ttu-id="4503f-145">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="4503f-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="4503f-146">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="4503f-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="4503f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4503f-147">OUTPUTS</span></span>

### <span data-ttu-id="4503f-148">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4503f-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="4503f-149">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="4503f-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="4503f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4503f-150">NOTES</span></span>

## <span data-ttu-id="4503f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4503f-151">RELATED LINKS</span></span>
