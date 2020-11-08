---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053477"
---
# <span data-ttu-id="444e3-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="444e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="444e3-102">SYNOPSIS</span></span>
<span data-ttu-id="444e3-103">Umożliwia zaktualizowanie połączenia VPN.</span><span class="sxs-lookup"><span data-stu-id="444e3-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="444e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="444e3-104">SYNTAX</span></span>

### <span data-ttu-id="444e3-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="444e3-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444e3-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="444e3-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="444e3-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="444e3-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="444e3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="444e3-108">DESCRIPTION</span></span>
<span data-ttu-id="444e3-109">Polecenie cmdlet **Update-AzVpnConnection** AKTUALIZUJE połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="444e3-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="444e3-110">Połączenie VPN tworzy połączenie IPsec, które łączy bramę VPN z zdalną gałęzią klienta reprezentowaną na platformie Azure jako witryną sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="444e3-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="444e3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="444e3-111">EXAMPLES</span></span>

### <span data-ttu-id="444e3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="444e3-112">Example 1</span></span>

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
```

<span data-ttu-id="444e3-113">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="444e3-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="444e3-114">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="444e3-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="444e3-115">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="444e3-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="444e3-116">Po zaktualizowaniu połączenie będzie miało nowe IpSecPolicy za pomocą polecenia Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="444e3-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="444e3-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="444e3-117">Example 2</span></span>

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
```

<span data-ttu-id="444e3-118">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="444e3-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="444e3-119">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="444e3-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="444e3-120">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="444e3-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="444e3-121">Następnie połączenie zostanie zaktualizowane w celu uzyskania nowego klucza współużytkowanego za pomocą bezpiecznego konstruowania ciągu.</span><span class="sxs-lookup"><span data-stu-id="444e3-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="444e3-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="444e3-122">PARAMETERS</span></span>

### <span data-ttu-id="444e3-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="444e3-123">-AsJob</span></span>
<span data-ttu-id="444e3-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="444e3-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="444e3-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="444e3-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="444e3-126">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="444e3-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="444e3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444e3-127">-DefaultProfile</span></span>
<span data-ttu-id="444e3-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="444e3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444e3-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="444e3-129">-EnableBgp</span></span>
<span data-ttu-id="444e3-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="444e3-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="444e3-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="444e3-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="444e3-132">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="444e3-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="444e3-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="444e3-133">-InputObject</span></span>
<span data-ttu-id="444e3-134">Obiekt VpnConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="444e3-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="444e3-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="444e3-135">-IpSecPolicy</span></span>
<span data-ttu-id="444e3-136">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="444e3-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="444e3-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="444e3-137">-Name</span></span>
<span data-ttu-id="444e3-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="444e3-138">The resource name.</span></span>

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

### <span data-ttu-id="444e3-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="444e3-139">-ParentResourceName</span></span>
<span data-ttu-id="444e3-140">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="444e3-140">The parent resource name.</span></span>

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

### <span data-ttu-id="444e3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444e3-141">-ResourceGroupName</span></span>
<span data-ttu-id="444e3-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="444e3-142">The resource group name.</span></span>

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

### <span data-ttu-id="444e3-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="444e3-143">-ResourceId</span></span>
<span data-ttu-id="444e3-144">Identyfikator zasobu obiektu VpnConnection, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="444e3-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="444e3-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="444e3-145">-SharedKey</span></span>
<span data-ttu-id="444e3-146">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="444e3-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="444e3-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="444e3-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="444e3-148">Gdy jest inicjowane połączenie, Użyj lokalnego adresu IP platformy Azure jako adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="444e3-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="444e3-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="444e3-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="444e3-150">Użyj selektorów ruchu opartego na zasadach dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="444e3-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="444e3-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="444e3-152">Lista VpnSiteLinkConnections, które ta VpnConnection musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="444e3-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="444e3-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="444e3-153">-Confirm</span></span>
<span data-ttu-id="444e3-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="444e3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="444e3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="444e3-155">-WhatIf</span></span>
<span data-ttu-id="444e3-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="444e3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="444e3-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="444e3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="444e3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444e3-158">CommonParameters</span></span>
<span data-ttu-id="444e3-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444e3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444e3-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="444e3-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444e3-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="444e3-161">INPUTS</span></span>

### <span data-ttu-id="444e3-162">System. String</span><span class="sxs-lookup"><span data-stu-id="444e3-162">System.String</span></span>

### <span data-ttu-id="444e3-163">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="444e3-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="444e3-164">OUTPUTS</span></span>

### <span data-ttu-id="444e3-165">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="444e3-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="444e3-166">NOTES</span></span>

## <span data-ttu-id="444e3-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="444e3-167">RELATED LINKS</span></span>

[<span data-ttu-id="444e3-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="444e3-169">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="444e3-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="444e3-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
