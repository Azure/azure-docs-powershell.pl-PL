---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708888"
---
# <span data-ttu-id="7ea9a-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="7ea9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea9a-103">Umożliwia zaktualizowanie połączenia VPN.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="7ea9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea9a-104">SYNTAX</span></span>

### <span data-ttu-id="7ea9a-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ea9a-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea9a-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea9a-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea9a-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7ea9a-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea9a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea9a-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea9a-109">Polecenie cmdlet **Update-AzVpnConnection** AKTUALIZUJE połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="7ea9a-110">Połączenie VPN tworzy połączenie IPsec, które łączy bramę VPN z zdalną gałęzią klienta reprezentowaną na platformie Azure jako witryną sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="7ea9a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea9a-111">EXAMPLES</span></span>

### <span data-ttu-id="7ea9a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ea9a-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="7ea9a-113">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7ea9a-114">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7ea9a-115">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7ea9a-116">Po zaktualizowaniu połączenie będzie miało nowe IpSecPolicy za pomocą polecenia Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="7ea9a-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7ea9a-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="7ea9a-118">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7ea9a-119">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7ea9a-120">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7ea9a-121">Następnie połączenie zostanie zaktualizowane w celu uzyskania nowego klucza współużytkowanego za pomocą bezpiecznego konstruowania ciągu.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="7ea9a-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea9a-122">PARAMETERS</span></span>

### <span data-ttu-id="7ea9a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ea9a-123">-AsJob</span></span>
<span data-ttu-id="7ea9a-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7ea9a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ea9a-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="7ea9a-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="7ea9a-126">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7ea9a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea9a-127">-DefaultProfile</span></span>
<span data-ttu-id="7ea9a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea9a-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7ea9a-129">-EnableBgp</span></span>
<span data-ttu-id="7ea9a-130">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="7ea9a-130">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ea9a-131">-InputObject</span></span>
<span data-ttu-id="7ea9a-132">Obiekt VpnConenction do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-132">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea9a-133">-IpSecPolicy</span></span>
<span data-ttu-id="7ea9a-134">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7ea9a-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ea9a-135">-Name</span></span>
<span data-ttu-id="7ea9a-136">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7ea9a-137">-ParentResourceName</span></span>
<span data-ttu-id="7ea9a-138">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea9a-139">-ResourceGroupName</span></span>
<span data-ttu-id="7ea9a-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea9a-141">-ResourceId</span></span>
<span data-ttu-id="7ea9a-142">Identyfikator zasobu obiektu VpnConenction, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-142">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7ea9a-143">-SharedKey</span></span>
<span data-ttu-id="7ea9a-144">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="7ea9a-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ea9a-145">-Confirm</span></span>
<span data-ttu-id="7ea9a-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea9a-147">-WhatIf</span></span>
<span data-ttu-id="7ea9a-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea9a-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea9a-150">CommonParameters</span></span>
<span data-ttu-id="7ea9a-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea9a-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea9a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea9a-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea9a-153">INPUTS</span></span>

### <span data-ttu-id="7ea9a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea9a-154">System.String</span></span>

### <span data-ttu-id="7ea9a-155">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7ea9a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea9a-156">OUTPUTS</span></span>

### <span data-ttu-id="7ea9a-157">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7ea9a-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea9a-158">NOTES</span></span>

## <span data-ttu-id="7ea9a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea9a-159">RELATED LINKS</span></span>

[<span data-ttu-id="7ea9a-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="7ea9a-161">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="7ea9a-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea9a-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
