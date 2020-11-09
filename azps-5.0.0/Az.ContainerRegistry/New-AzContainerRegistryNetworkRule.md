---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304129"
---
# <span data-ttu-id="3bf4e-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3bf4e-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="3bf4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bf4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf4e-103">Utwórz regułę sieci.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-103">Create a network rule.</span></span>

## <span data-ttu-id="3bf4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bf4e-104">SYNTAX</span></span>

### <span data-ttu-id="3bf4e-105">ByVirtualNetworkRule (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3bf4e-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bf4e-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="3bf4e-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bf4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3bf4e-107">DESCRIPTION</span></span>
<span data-ttu-id="3bf4e-108">Tworzenie obiektu reguły sieci w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="3bf4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bf4e-109">EXAMPLES</span></span>

### <span data-ttu-id="3bf4e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bf4e-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="3bf4e-111">Utwórz zestaw reguł virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="3bf4e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bf4e-112">PARAMETERS</span></span>

### <span data-ttu-id="3bf4e-113">-Action</span><span class="sxs-lookup"><span data-stu-id="3bf4e-113">-Action</span></span>
<span data-ttu-id="3bf4e-114">Akcja reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf4e-115">-DefaultProfile</span></span>
<span data-ttu-id="3bf4e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bf4e-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3bf4e-117">-IPAddressOrRange</span></span>
<span data-ttu-id="3bf4e-118">Określa zakres adresów IP lub IP w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="3bf4e-119">Dozwolony jest tylko adres IPV4.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf4e-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3bf4e-120">-IPRule</span></span>
<span data-ttu-id="3bf4e-121">Wskaż, aby utworzyć IPRule.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf4e-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf4e-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3bf4e-123">Identyfikator zasobu podsieci, na przykład:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf4e-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3bf4e-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="3bf4e-125">Wskaż, aby utworzyć VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf4e-126">CommonParameters</span></span>
<span data-ttu-id="3bf4e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf4e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bf4e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf4e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bf4e-129">INPUTS</span></span>

### <span data-ttu-id="3bf4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3bf4e-130">System.String</span></span>

## <span data-ttu-id="3bf4e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bf4e-131">OUTPUTS</span></span>

### <span data-ttu-id="3bf4e-132">Microsoft. Azure. Commands. ContainerRegistry. models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3bf4e-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="3bf4e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bf4e-133">NOTES</span></span>

## <span data-ttu-id="3bf4e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bf4e-134">RELATED LINKS</span></span>
