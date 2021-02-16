---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: d5f78bf034c46d3b07a97d642032ef0cfe6b339e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191803"
---
# <span data-ttu-id="a9800-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a9800-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="a9800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9800-102">SYNOPSIS</span></span>
<span data-ttu-id="a9800-103">Tworzy obiekt Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="a9800-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="a9800-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9800-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9800-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9800-105">DESCRIPTION</span></span>
<span data-ttu-id="a9800-106">Tworzy obiekt Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="a9800-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="a9800-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9800-107">EXAMPLES</span></span>

### <span data-ttu-id="a9800-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9800-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="a9800-109">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite z 1 łączami VpnSiteLink w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a9800-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="a9800-110">Brama VPN zostanie utworzona w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="a9800-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="a9800-111">Po utworzeniu brama jest podłączona do strony vpnsite za pomocą polecenia New-AzVpnConnection z 1 vpnSiteLinkConnections do vpnSiteLink tej lokacji.</span><span class="sxs-lookup"><span data-stu-id="a9800-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="a9800-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9800-112">PARAMETERS</span></span>

### <span data-ttu-id="a9800-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="a9800-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="a9800-114">Przepustowość, która musi zostać obsługina przez to połączenie linku w mb/s.</span><span class="sxs-lookup"><span data-stu-id="a9800-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9800-115">-DefaultProfile</span></span>
<span data-ttu-id="a9800-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9800-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9800-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="a9800-117">-EgressNatRule</span></span>
<span data-ttu-id="a9800-118">Lista reguł NAT ruchu wychodzącego skojarzonych z tym połączeniem linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a9800-119">-EnableBgp</span></span>
<span data-ttu-id="a9800-120">Włącz BGP dla tego połączenia linku</span><span class="sxs-lookup"><span data-stu-id="a9800-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="a9800-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="a9800-121">-IngressNatRule</span></span>
<span data-ttu-id="a9800-122">Lista reguł nat ruchu wychodzącego, które są skojarzone z tym połączeniem linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="a9800-123">-IpSecPolicy</span></span>
<span data-ttu-id="a9800-124">Zasady IpSec, które należy uwzględnić dla tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-124">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9800-125">-Name</span></span>
<span data-ttu-id="a9800-126">Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9800-126">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-127">- RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a9800-127">-RoutingWeight</span></span>
<span data-ttu-id="a9800-128">Routing Weight</span><span class="sxs-lookup"><span data-stu-id="a9800-128">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a9800-129">-SharedKey</span></span>
<span data-ttu-id="a9800-130">Klucz udostępniony wymagany do skonfigurowania tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-130">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9800-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="a9800-132">Użyj lokalnego adresu IP platformy Azure jako źródłowego adresu IP dla tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="a9800-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a9800-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a9800-134">Użyj selektorów ruchu opartych na zasadach dla tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="a9800-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="a9800-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="a9800-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="a9800-136">Protokół połączenia bramy:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="a9800-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a9800-137">-VpnSiteLink</span></span>
<span data-ttu-id="a9800-138">Obiekt linku witryny vpn, z który ma nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="a9800-138">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9800-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9800-139">CommonParameters</span></span>
<span data-ttu-id="a9800-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9800-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9800-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9800-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9800-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9800-142">INPUTS</span></span>

### <span data-ttu-id="a9800-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a9800-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="a9800-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9800-144">OUTPUTS</span></span>

### <span data-ttu-id="a9800-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a9800-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="a9800-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9800-146">NOTES</span></span>

## <span data-ttu-id="a9800-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9800-147">RELATED LINKS</span></span>

[<span data-ttu-id="a9800-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a9800-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)