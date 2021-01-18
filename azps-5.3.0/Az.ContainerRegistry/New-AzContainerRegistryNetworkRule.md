---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501794"
---
# <span data-ttu-id="ee67b-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ee67b-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="ee67b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee67b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee67b-103">Utwórz regułę sieci.</span><span class="sxs-lookup"><span data-stu-id="ee67b-103">Create a network rule.</span></span>

## <span data-ttu-id="ee67b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee67b-104">SYNTAX</span></span>

### <span data-ttu-id="ee67b-105">ByVirtualNetworkRule (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee67b-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee67b-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="ee67b-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee67b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee67b-107">DESCRIPTION</span></span>
<span data-ttu-id="ee67b-108">Tworzenie obiektu reguły sieci w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee67b-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="ee67b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee67b-109">EXAMPLES</span></span>

### <span data-ttu-id="ee67b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee67b-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="ee67b-111">Utwórz zestaw reguł virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="ee67b-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="ee67b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee67b-112">PARAMETERS</span></span>

### <span data-ttu-id="ee67b-113">-Action</span><span class="sxs-lookup"><span data-stu-id="ee67b-113">-Action</span></span>
<span data-ttu-id="ee67b-114">Akcja reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="ee67b-114">The action of network rule.</span></span>

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

### <span data-ttu-id="ee67b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee67b-115">-DefaultProfile</span></span>
<span data-ttu-id="ee67b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee67b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee67b-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ee67b-117">-IPAddressOrRange</span></span>
<span data-ttu-id="ee67b-118">Określa zakres adresów IP lub IP w formacie CIDR.</span><span class="sxs-lookup"><span data-stu-id="ee67b-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="ee67b-119">Dozwolony jest tylko adres IPV4.</span><span class="sxs-lookup"><span data-stu-id="ee67b-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="ee67b-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ee67b-120">-IPRule</span></span>
<span data-ttu-id="ee67b-121">Wskaż, aby utworzyć IPRule.</span><span class="sxs-lookup"><span data-stu-id="ee67b-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="ee67b-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ee67b-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ee67b-123">Identyfikator zasobu podsieci, na przykład:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="ee67b-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="ee67b-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ee67b-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="ee67b-125">Wskaż, aby utworzyć VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ee67b-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="ee67b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee67b-126">CommonParameters</span></span>
<span data-ttu-id="ee67b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee67b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee67b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee67b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee67b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee67b-129">INPUTS</span></span>

### <span data-ttu-id="ee67b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ee67b-130">System.String</span></span>

## <span data-ttu-id="ee67b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee67b-131">OUTPUTS</span></span>

### <span data-ttu-id="ee67b-132">Microsoft. Azure. Commands. ContainerRegistry. models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ee67b-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="ee67b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee67b-133">NOTES</span></span>

## <span data-ttu-id="ee67b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee67b-134">RELATED LINKS</span></span>
