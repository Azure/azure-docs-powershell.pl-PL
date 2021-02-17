---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191594"
---
# <span data-ttu-id="61933-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="61933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61933-102">SYNOPSIS</span></span>
<span data-ttu-id="61933-103">Konfiguruje komunikacji równorzędne w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="61933-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="61933-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61933-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61933-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="61933-105">DESCRIPTION</span></span>
<span data-ttu-id="61933-106">Polecenie **cmdlet Set-AzVirtualNetworkPeering** konfiguruje wirtualną sieć równorzędną.</span><span class="sxs-lookup"><span data-stu-id="61933-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="61933-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61933-107">EXAMPLES</span></span>

### <span data-ttu-id="61933-108">Przykład 1. Zmienianie konfiguracji ruchu przekazywanego w komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="61933-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="61933-109">Przykład 2. Zmienianie dostępu do sieci wirtualnej w komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="61933-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="61933-110">Przykład 3. Zmienianie konfiguracji właściwości przesyłania bramy w komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="61933-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="61933-111">Przykład 4. Korzystanie z bram zdalnych w komunikacji równorzędnej w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="61933-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="61933-112">Zmieniając tę właściwość na $True, można używać bramy VNet firmy równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="61933-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="61933-113">Jednak w sieci VNet równorzędnej musi być skonfigurowana brama, a wartość właściwości **AllowGatewayTransit** musi $True.</span><span class="sxs-lookup"><span data-stu-id="61933-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="61933-114">Tej właściwości nie można używać, jeśli brama została już skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="61933-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="61933-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61933-115">PARAMETERS</span></span>

### <span data-ttu-id="61933-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="61933-116">-AsJob</span></span>
<span data-ttu-id="61933-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="61933-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61933-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61933-118">-DefaultProfile</span></span>
<span data-ttu-id="61933-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61933-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61933-120">— VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="61933-121">Określa sieć wirtualną komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="61933-121">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61933-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61933-122">CommonParameters</span></span>
<span data-ttu-id="61933-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61933-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61933-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61933-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61933-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61933-125">INPUTS</span></span>

### <span data-ttu-id="61933-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="61933-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61933-127">OUTPUTS</span></span>

### <span data-ttu-id="61933-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="61933-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61933-129">NOTES</span></span>

## <span data-ttu-id="61933-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61933-130">RELATED LINKS</span></span>

[<span data-ttu-id="61933-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="61933-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="61933-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="61933-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
