---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196899"
---
# <span data-ttu-id="240d2-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="240d2-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="240d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240d2-102">SYNOPSIS</span></span>
<span data-ttu-id="240d2-103">Utwórz regułę sieciową.</span><span class="sxs-lookup"><span data-stu-id="240d2-103">Create a network rule.</span></span>

## <span data-ttu-id="240d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="240d2-104">SYNTAX</span></span>

### <span data-ttu-id="240d2-105">ByVirtualNetworkRule (domyślne)</span><span class="sxs-lookup"><span data-stu-id="240d2-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="240d2-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="240d2-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="240d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="240d2-107">DESCRIPTION</span></span>
<span data-ttu-id="240d2-108">Tworzenie obiektu reguły sieciowej w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="240d2-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="240d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="240d2-109">EXAMPLES</span></span>

### <span data-ttu-id="240d2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="240d2-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="240d2-111">Tworzenie zestawu reguł w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="240d2-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="240d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="240d2-112">PARAMETERS</span></span>

### <span data-ttu-id="240d2-113">— Akcja</span><span class="sxs-lookup"><span data-stu-id="240d2-113">-Action</span></span>
<span data-ttu-id="240d2-114">Działanie reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="240d2-114">The action of network rule.</span></span>

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

### <span data-ttu-id="240d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240d2-115">-DefaultProfile</span></span>
<span data-ttu-id="240d2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="240d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240d2-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="240d2-117">-IPAddressOrRange</span></span>
<span data-ttu-id="240d2-118">Określa zakres adresów IP lub IP w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="240d2-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="240d2-119">Dozwolony jest tylko adres IPV4.</span><span class="sxs-lookup"><span data-stu-id="240d2-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="240d2-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="240d2-120">-IPRule</span></span>
<span data-ttu-id="240d2-121">Wskaż, aby utworzyć adres IPRule.</span><span class="sxs-lookup"><span data-stu-id="240d2-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="240d2-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="240d2-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="240d2-123">Identyfikator zasobu podsieci, na przykład: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="240d2-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="240d2-124">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="240d2-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="240d2-125">Wskaż, aby utworzyć virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="240d2-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="240d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240d2-126">CommonParameters</span></span>
<span data-ttu-id="240d2-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240d2-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="240d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240d2-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="240d2-129">INPUTS</span></span>

### <span data-ttu-id="240d2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="240d2-130">System.String</span></span>

## <span data-ttu-id="240d2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="240d2-131">OUTPUTS</span></span>

### <span data-ttu-id="240d2-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="240d2-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="240d2-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="240d2-133">NOTES</span></span>

## <span data-ttu-id="240d2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="240d2-134">RELATED LINKS</span></span>
