---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 870caec4cad2bd4d64c00a2b0bf3423f080b98ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894573"
---
# <span data-ttu-id="6b3ed-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="6b3ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3ed-103">Tworzy połączenie IPSec łączące VpnGateway z odległym rozgałęzieniem klientów, reprezentowany w dodatku RM jako VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="6b3ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b3ed-104">SYNTAX</span></span>

### <span data-ttu-id="6b3ed-105">ByVpnGatewayNameByVpnSiteObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b3ed-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b3ed-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ed-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ed-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="6b3ed-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ed-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ed-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ed-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="6b3ed-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3ed-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ed-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3ed-111">Opis</span><span class="sxs-lookup"><span data-stu-id="6b3ed-111">DESCRIPTION</span></span>
<span data-ttu-id="6b3ed-112">Tworzy połączenie IPSec łączące VpnGateway z odległym rozgałęzieniem klientów, reprezentowany w dodatku RM jako VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="6b3ed-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b3ed-113">EXAMPLES</span></span>

### <span data-ttu-id="6b3ed-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b3ed-114">Example 1</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="6b3ed-115">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6b3ed-116">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6b3ed-117">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="6b3ed-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6b3ed-118">Example 2</span></span>
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

<span data-ttu-id="6b3ed-119">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite z 1 VpnSiteLinks na zachodnim terenie Stanów Zjednoczonych w obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="6b3ed-120">Brama sieci VPN zostanie utworzona później w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="6b3ed-121">Po utworzeniu bramy jest ona połączona z VpnSite za pomocą polecenia New-AzVpnConnection z 1 VpnSiteLinkConnections na VpnSiteLink VpnSite.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="6b3ed-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b3ed-122">PARAMETERS</span></span>

### <span data-ttu-id="6b3ed-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b3ed-123">-AsJob</span></span>
<span data-ttu-id="6b3ed-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b3ed-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b3ed-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6b3ed-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="6b3ed-126">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6b3ed-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3ed-127">-DefaultProfile</span></span>
<span data-ttu-id="6b3ed-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3ed-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6b3ed-129">-EnableBgp</span></span>
<span data-ttu-id="6b3ed-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="6b3ed-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="6b3ed-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6b3ed-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="6b3ed-132">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="6b3ed-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="6b3ed-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="6b3ed-133">-IpSecPolicy</span></span>
<span data-ttu-id="6b3ed-134">Przepustowość, która musi być obsługiwana przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6b3ed-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b3ed-135">-Name</span></span>
<span data-ttu-id="6b3ed-136">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-136">The resource name.</span></span>

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

### <span data-ttu-id="6b3ed-137">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6b3ed-137">-ParentObject</span></span>
<span data-ttu-id="6b3ed-138">VpnGateway nadrzędny dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-138">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="6b3ed-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3ed-139">-ParentResourceId</span></span>
<span data-ttu-id="6b3ed-140">Identyfikator zasobu dla VpnGateway nadrzędnego dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-140">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="6b3ed-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6b3ed-141">-ParentResourceName</span></span>
<span data-ttu-id="6b3ed-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-142">The resource group name.</span></span>

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

### <span data-ttu-id="6b3ed-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b3ed-143">-ResourceGroupName</span></span>
<span data-ttu-id="6b3ed-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-144">The resource group name.</span></span>

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

### <span data-ttu-id="6b3ed-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6b3ed-145">-SharedKey</span></span>
<span data-ttu-id="6b3ed-146">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="6b3ed-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b3ed-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6b3ed-148">Gdy jest inicjowane połączenie, Użyj lokalnego adresu IP platformy Azure jako adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="6b3ed-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6b3ed-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6b3ed-150">Użyj selektorów ruchu opartego na zasadach dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="6b3ed-151">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="6b3ed-151">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="6b3ed-152">Protokół połączeń z bramą: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="6b3ed-152">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="6b3ed-153">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6b3ed-153">-VpnSite</span></span>
<span data-ttu-id="6b3ed-154">Zdalna witryna sieci VPN, do której jest podłączone połączenie z siecią wirtualną tego centrum.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-154">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6b3ed-155">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="6b3ed-155">-VpnSiteId</span></span>
<span data-ttu-id="6b3ed-156">Zdalna witryna sieci VPN, do której jest podłączone połączenie z siecią wirtualną tego centrum.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6b3ed-157">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-157">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="6b3ed-158">Lista VpnSiteLinkConnections, które posiada ta VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-158">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

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

### <span data-ttu-id="6b3ed-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b3ed-159">-Confirm</span></span>
<span data-ttu-id="6b3ed-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3ed-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3ed-161">-WhatIf</span></span>
<span data-ttu-id="6b3ed-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3ed-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3ed-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3ed-164">CommonParameters</span></span>
<span data-ttu-id="6b3ed-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3ed-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3ed-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b3ed-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3ed-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b3ed-167">INPUTS</span></span>

### <span data-ttu-id="6b3ed-168">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6b3ed-168">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6b3ed-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6b3ed-169">System.String</span></span>

## <span data-ttu-id="6b3ed-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b3ed-170">OUTPUTS</span></span>

### <span data-ttu-id="6b3ed-171">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-171">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="6b3ed-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b3ed-172">NOTES</span></span>

## <span data-ttu-id="6b3ed-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b3ed-173">RELATED LINKS</span></span>

[<span data-ttu-id="6b3ed-174">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-174">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="6b3ed-175">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-175">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="6b3ed-176">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6b3ed-176">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
