---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186810"
---
# <span data-ttu-id="f0ea5-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="f0ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ea5-103">Aktualizuje połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="f0ea5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0ea5-104">SYNTAX</span></span>

### <span data-ttu-id="f0ea5-105">ByVpnConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f0ea5-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ea5-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f0ea5-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0ea5-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f0ea5-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ea5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0ea5-108">DESCRIPTION</span></span>
<span data-ttu-id="f0ea5-109">Polecenie **cmdlet Update-AzVpnConnection** aktualizuje połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="f0ea5-110">Połączenie VPN tworzy połączenie IPsec, które łączy bramę VPN z zdalną gałąź klienta reprezentowaną na platformie Azure jako witryna VPN.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="f0ea5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0ea5-111">EXAMPLES</span></span>

### <span data-ttu-id="f0ea5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0ea5-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="f0ea5-113">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f0ea5-114">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f0ea5-115">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="f0ea5-116">Połączenie zostanie zaktualizowane, aby przy użyciu polecenia Set-AzVpnConnection IpSecPolicy Set-AzVpnConnection nowe.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="f0ea5-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f0ea5-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="f0ea5-118">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f0ea5-119">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f0ea5-120">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="f0ea5-121">Połączenie zostanie zaktualizowane w celu utworzenia nowego klucza udostępnionego przy użyciu konstrukcji bezpiecznego ciągu.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="f0ea5-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0ea5-122">PARAMETERS</span></span>

### <span data-ttu-id="f0ea5-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f0ea5-123">-AsJob</span></span>
<span data-ttu-id="f0ea5-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f0ea5-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0ea5-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="f0ea5-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="f0ea5-126">Przepustowość, która musi zostać obsługina przez to połączenie w mb/s.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="f0ea5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ea5-127">-DefaultProfile</span></span>
<span data-ttu-id="f0ea5-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ea5-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f0ea5-129">-EnableBgp</span></span>
<span data-ttu-id="f0ea5-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="f0ea5-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f0ea5-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="f0ea5-132">Włącz zabezpieczenia internetowe dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="f0ea5-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ea5-133">-InputObject</span></span>
<span data-ttu-id="f0ea5-134">Obiekt VpnConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="f0ea5-135">-IpSecPolicy</span></span>
<span data-ttu-id="f0ea5-136">Przepustowość, która musi zostać obsługina przez to połączenie w mb/s.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="f0ea5-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f0ea5-137">-Name</span></span>
<span data-ttu-id="f0ea5-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f0ea5-139">-ParentResourceName</span></span>
<span data-ttu-id="f0ea5-140">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ea5-141">-ResourceGroupName</span></span>
<span data-ttu-id="f0ea5-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0ea5-143">-ResourceId</span></span>
<span data-ttu-id="f0ea5-144">Identyfikator zasobu obiektu VpnConnection do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ea5-145">-RoutingConfiguration</span></span>
<span data-ttu-id="f0ea5-146">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="f0ea5-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="f0ea5-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f0ea5-147">-SharedKey</span></span>
<span data-ttu-id="f0ea5-148">Klucz udostępniony wymagany do skonfigurowania tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="f0ea5-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0ea5-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="f0ea5-150">Użyj lokalnego adresu IP platformy Azure jako adresu źródłowego podczas inicjowania połączenia.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f0ea5-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f0ea5-152">Dla tego połączenia użyj selektorów ruchu opartych na zasadach.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea5-153">- VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="f0ea5-154">Lista połączeń VpnSiteLinkConnections, które musi mieć ta usługa VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="f0ea5-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0ea5-155">-Confirm</span></span>
<span data-ttu-id="f0ea5-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ea5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ea5-157">-WhatIf</span></span>
<span data-ttu-id="f0ea5-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ea5-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ea5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ea5-160">CommonParameters</span></span>
<span data-ttu-id="f0ea5-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ea5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ea5-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0ea5-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ea5-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0ea5-163">INPUTS</span></span>

### <span data-ttu-id="f0ea5-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f0ea5-164">System.String</span></span>

### <span data-ttu-id="f0ea5-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="f0ea5-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0ea5-166">OUTPUTS</span></span>

### <span data-ttu-id="f0ea5-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="f0ea5-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0ea5-168">NOTES</span></span>

## <span data-ttu-id="f0ea5-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0ea5-169">RELATED LINKS</span></span>

[<span data-ttu-id="f0ea5-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="f0ea5-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="f0ea5-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f0ea5-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="f0ea5-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ea5-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
