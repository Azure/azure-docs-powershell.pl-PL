---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545003"
---
# <span data-ttu-id="c8e57-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8e57-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="c8e57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8e57-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e57-103">Umożliwia zaktualizowanie obiektu VpnConnection do stanu celu.</span><span class="sxs-lookup"><span data-stu-id="c8e57-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8e57-104">SYNTAX</span></span>

### <span data-ttu-id="c8e57-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8e57-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8e57-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="c8e57-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e57-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c8e57-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e57-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c8e57-108">DESCRIPTION</span></span>
<span data-ttu-id="c8e57-109">Tworzy połączenie IPSec łączące VpnGateway z odległym rozgałęzieniem klientów, reprezentowany w dodatku RM jako VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c8e57-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="c8e57-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8e57-110">EXAMPLES</span></span>

### <span data-ttu-id="c8e57-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8e57-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="c8e57-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e57-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c8e57-113">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="c8e57-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c8e57-114">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c8e57-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="c8e57-115">Po zaktualizowaniu połączenie będzie miało nowe IpSecPolicy za pomocą polecenia Set-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c8e57-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="c8e57-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c8e57-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="c8e57-117">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e57-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c8e57-118">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="c8e57-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c8e57-119">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c8e57-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="c8e57-120">Następnie połączenie zostanie zaktualizowane w celu uzyskania nowego klucza współużytkowanego za pomocą bezpiecznego konstruowania ciągu.</span><span class="sxs-lookup"><span data-stu-id="c8e57-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="c8e57-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8e57-121">PARAMETERS</span></span>

### <span data-ttu-id="c8e57-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8e57-122">-AsJob</span></span>
<span data-ttu-id="c8e57-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c8e57-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8e57-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c8e57-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="c8e57-125">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="c8e57-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="c8e57-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e57-126">-DefaultProfile</span></span>
<span data-ttu-id="c8e57-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e57-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e57-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c8e57-128">-EnableBgp</span></span>
<span data-ttu-id="c8e57-129">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="c8e57-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="c8e57-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8e57-130">-InputObject</span></span>
<span data-ttu-id="c8e57-131">Obiekt VpnConenction do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c8e57-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="c8e57-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e57-132">-IpSecPolicy</span></span>
<span data-ttu-id="c8e57-133">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="c8e57-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="c8e57-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8e57-134">-Name</span></span>
<span data-ttu-id="c8e57-135">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c8e57-135">The resource name.</span></span>

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

### <span data-ttu-id="c8e57-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c8e57-136">-ParentResourceName</span></span>
<span data-ttu-id="c8e57-137">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="c8e57-137">The parent resource name.</span></span>

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

### <span data-ttu-id="c8e57-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e57-138">-ResourceGroupName</span></span>
<span data-ttu-id="c8e57-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8e57-139">The resource group name.</span></span>

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

### <span data-ttu-id="c8e57-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8e57-140">-ResourceId</span></span>
<span data-ttu-id="c8e57-141">Identyfikator zasobu obiektu VpnConenction, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c8e57-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="c8e57-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c8e57-142">-SharedKey</span></span>
<span data-ttu-id="c8e57-143">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="c8e57-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="c8e57-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8e57-144">-Confirm</span></span>
<span data-ttu-id="c8e57-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e57-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e57-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e57-146">-WhatIf</span></span>
<span data-ttu-id="c8e57-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e57-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e57-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8e57-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e57-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e57-149">CommonParameters</span></span>
<span data-ttu-id="c8e57-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e57-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e57-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e57-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e57-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8e57-152">INPUTS</span></span>

### <span data-ttu-id="c8e57-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e57-153">System.String</span></span>

### <span data-ttu-id="c8e57-154">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8e57-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c8e57-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8e57-155">OUTPUTS</span></span>

### <span data-ttu-id="c8e57-156">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8e57-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c8e57-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8e57-157">NOTES</span></span>

## <span data-ttu-id="c8e57-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8e57-158">RELATED LINKS</span></span>
