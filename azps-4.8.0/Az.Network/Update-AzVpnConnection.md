---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223017"
---
# <span data-ttu-id="4bf88-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="4bf88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bf88-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf88-103">Umożliwia zaktualizowanie połączenia VPN.</span><span class="sxs-lookup"><span data-stu-id="4bf88-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="4bf88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bf88-104">SYNTAX</span></span>

### <span data-ttu-id="4bf88-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bf88-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf88-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf88-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bf88-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4bf88-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf88-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4bf88-108">DESCRIPTION</span></span>
<span data-ttu-id="4bf88-109">Polecenie cmdlet **Update-AzVpnConnection** AKTUALIZUJE połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="4bf88-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="4bf88-110">Połączenie VPN tworzy połączenie IPsec, które łączy bramę VPN z zdalną gałęzią klienta reprezentowaną na platformie Azure jako witryną sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="4bf88-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="4bf88-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bf88-111">EXAMPLES</span></span>

### <span data-ttu-id="4bf88-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bf88-112">Example 1</span></span>

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

<span data-ttu-id="4bf88-113">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bf88-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4bf88-114">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="4bf88-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4bf88-115">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4bf88-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="4bf88-116">Po zaktualizowaniu połączenie będzie miało nowe IpSecPolicy za pomocą polecenia Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4bf88-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="4bf88-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4bf88-117">Example 2</span></span>

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

<span data-ttu-id="4bf88-118">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bf88-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4bf88-119">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="4bf88-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4bf88-120">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4bf88-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="4bf88-121">Następnie połączenie zostanie zaktualizowane w celu uzyskania nowego klucza współużytkowanego za pomocą bezpiecznego konstruowania ciągu.</span><span class="sxs-lookup"><span data-stu-id="4bf88-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="4bf88-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bf88-122">PARAMETERS</span></span>

### <span data-ttu-id="4bf88-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bf88-123">-AsJob</span></span>
<span data-ttu-id="4bf88-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4bf88-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bf88-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4bf88-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="4bf88-126">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="4bf88-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="4bf88-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf88-127">-DefaultProfile</span></span>
<span data-ttu-id="4bf88-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bf88-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf88-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4bf88-129">-EnableBgp</span></span>
<span data-ttu-id="4bf88-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4bf88-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="4bf88-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="4bf88-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="4bf88-132">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4bf88-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="4bf88-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4bf88-133">-InputObject</span></span>
<span data-ttu-id="4bf88-134">Obiekt VpnConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4bf88-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="4bf88-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="4bf88-135">-IpSecPolicy</span></span>
<span data-ttu-id="4bf88-136">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="4bf88-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="4bf88-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4bf88-137">-Name</span></span>
<span data-ttu-id="4bf88-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4bf88-138">The resource name.</span></span>

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

### <span data-ttu-id="4bf88-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4bf88-139">-ParentResourceName</span></span>
<span data-ttu-id="4bf88-140">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4bf88-140">The parent resource name.</span></span>

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

### <span data-ttu-id="4bf88-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf88-141">-ResourceGroupName</span></span>
<span data-ttu-id="4bf88-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4bf88-142">The resource group name.</span></span>

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

### <span data-ttu-id="4bf88-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf88-143">-ResourceId</span></span>
<span data-ttu-id="4bf88-144">Identyfikator zasobu obiektu VpnConnection, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4bf88-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="4bf88-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bf88-145">-RoutingConfiguration</span></span>
<span data-ttu-id="4bf88-146">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4bf88-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="4bf88-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4bf88-147">-SharedKey</span></span>
<span data-ttu-id="4bf88-148">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="4bf88-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="4bf88-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bf88-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="4bf88-150">Gdy jest inicjowane połączenie, Użyj lokalnego adresu IP platformy Azure jako adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="4bf88-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="4bf88-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="4bf88-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="4bf88-152">Użyj selektorów ruchu opartego na zasadach dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="4bf88-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="4bf88-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="4bf88-154">Lista VpnSiteLinkConnections, które ta VpnConnection musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="4bf88-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="4bf88-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bf88-155">-Confirm</span></span>
<span data-ttu-id="4bf88-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bf88-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf88-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf88-157">-WhatIf</span></span>
<span data-ttu-id="4bf88-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bf88-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf88-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4bf88-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf88-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf88-160">CommonParameters</span></span>
<span data-ttu-id="4bf88-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf88-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf88-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bf88-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf88-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bf88-163">INPUTS</span></span>

### <span data-ttu-id="4bf88-164">System. String</span><span class="sxs-lookup"><span data-stu-id="4bf88-164">System.String</span></span>

### <span data-ttu-id="4bf88-165">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="4bf88-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bf88-166">OUTPUTS</span></span>

### <span data-ttu-id="4bf88-167">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="4bf88-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bf88-168">NOTES</span></span>

## <span data-ttu-id="4bf88-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bf88-169">RELATED LINKS</span></span>

[<span data-ttu-id="4bf88-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="4bf88-171">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="4bf88-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bf88-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="4bf88-173">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bf88-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
