---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179570"
---
# <span data-ttu-id="e0e01-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="e0e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e01-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e01-103">Tworzy połączenie IPSec łączące bramę VpnGateway ze zdalną gałąź klienta reprezentowaną w Uściślanych klientach jako lokację vpn.</span><span class="sxs-lookup"><span data-stu-id="e0e01-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="e0e01-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0e01-104">SYNTAX</span></span>

### <span data-ttu-id="e0e01-105">ByVpnGatewayNameByVpnSiteObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e0e01-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e01-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e01-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e01-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="e0e01-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e01-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e01-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e01-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="e0e01-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e01-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e01-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e01-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0e01-111">DESCRIPTION</span></span>
<span data-ttu-id="e0e01-112">Tworzy połączenie IPSec łączące bramę VpnGateway ze zdalną gałęzią klienta reprezentowaną w Uściślanych klientach jako lokację VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e0e01-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="e0e01-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0e01-113">EXAMPLES</span></span>

### <span data-ttu-id="e0e01-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0e01-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="e0e01-115">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e01-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e0e01-116">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="e0e01-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e0e01-117">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="e0e01-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="e0e01-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0e01-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="e0e01-119">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite z 1 łączami VpnSiteLink w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e01-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="e0e01-120">Brama VPN zostanie utworzona w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="e0e01-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="e0e01-121">Po utworzeniu brama jest podłączona do strony vpnsite za pomocą polecenia New-AzVpnConnection z 1 vpnSiteLinkConnections do vpnSiteLink tej lokacji.</span><span class="sxs-lookup"><span data-stu-id="e0e01-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="e0e01-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0e01-122">PARAMETERS</span></span>

### <span data-ttu-id="e0e01-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e0e01-123">-AsJob</span></span>
<span data-ttu-id="e0e01-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e0e01-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="e0e01-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="e0e01-126">Przepustowość, która musi zostać obsługina przez to połączenie w mb/s.</span><span class="sxs-lookup"><span data-stu-id="e0e01-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e01-127">-DefaultProfile</span></span>
<span data-ttu-id="e0e01-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e01-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e0e01-129">-EnableBgp</span></span>
<span data-ttu-id="e0e01-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="e0e01-130">Enable BGP for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e0e01-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="e0e01-132">Włącz zabezpieczenia internetowe dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="e0e01-132">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="e0e01-133">-IpSecPolicy</span></span>
<span data-ttu-id="e0e01-134">Przepustowość, która musi zostać obsługina przez to połączenie w mb/s.</span><span class="sxs-lookup"><span data-stu-id="e0e01-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0e01-135">-Name</span></span>
<span data-ttu-id="e0e01-136">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0e01-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-137">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0e01-137">-ParentObject</span></span>
<span data-ttu-id="e0e01-138">Nadrzędna aplikacja VpnGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="e0e01-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e01-139">-ParentResourceId</span></span>
<span data-ttu-id="e0e01-140">Identyfikator zasobu nadrzędnej aplikacji VpnGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="e0e01-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e0e01-141">-ParentResourceName</span></span>
<span data-ttu-id="e0e01-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0e01-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e01-143">-ResourceGroupName</span></span>
<span data-ttu-id="e0e01-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0e01-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0e01-145">-RoutingConfiguration</span></span>
<span data-ttu-id="e0e01-146">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="e0e01-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e0e01-147">-SharedKey</span></span>
<span data-ttu-id="e0e01-148">Klucz udostępniony wymagany do skonfigurowania tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="e0e01-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0e01-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="e0e01-150">Użyj lokalnego adresu IP platformy Azure jako adresu źródłowego podczas inicjowania połączenia.</span><span class="sxs-lookup"><span data-stu-id="e0e01-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e0e01-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e0e01-152">Dla tego połączenia użyj selektorów ruchu opartych na zasadach.</span><span class="sxs-lookup"><span data-stu-id="e0e01-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="e0e01-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="e0e01-154">Protokół połączenia bramy:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="e0e01-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-155">- VpnSite</span><span class="sxs-lookup"><span data-stu-id="e0e01-155">-VpnSite</span></span>
<span data-ttu-id="e0e01-156">Zdalna witryna vpn, z którą jest połączone połączenie z wirtualną siecią w centrum.</span><span class="sxs-lookup"><span data-stu-id="e0e01-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="e0e01-157">-VpnSiteId</span></span>
<span data-ttu-id="e0e01-158">Zdalna witryna vpn, z którą jest połączone połączenie z wirtualną siecią w centrum.</span><span class="sxs-lookup"><span data-stu-id="e0e01-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="e0e01-160">Lista połączeń VpnSiteLinkConnections posiadana przez tę usługę VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="e0e01-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0e01-161">-Confirm</span></span>
<span data-ttu-id="e0e01-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0e01-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e01-163">-WhatIf</span></span>
<span data-ttu-id="e0e01-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e01-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e01-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0e01-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e01-166">CommonParameters</span></span>
<span data-ttu-id="e0e01-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e01-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e01-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0e01-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e01-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e01-169">INPUTS</span></span>

### <span data-ttu-id="e0e01-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e0e01-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e0e01-171">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e01-171">System.String</span></span>

## <span data-ttu-id="e0e01-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e01-172">OUTPUTS</span></span>

### <span data-ttu-id="e0e01-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="e0e01-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0e01-174">NOTES</span></span>

## <span data-ttu-id="e0e01-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0e01-175">RELATED LINKS</span></span>

[<span data-ttu-id="e0e01-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="e0e01-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="e0e01-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e0e01-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="e0e01-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0e01-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
