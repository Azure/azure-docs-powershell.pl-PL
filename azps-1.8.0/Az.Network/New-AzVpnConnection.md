---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 750af3bf948345a22c7cb7a86b09e07d4e266f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709208"
---
# <span data-ttu-id="843bd-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="843bd-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="843bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="843bd-102">SYNOPSIS</span></span>
<span data-ttu-id="843bd-103">Tworzy połączenie IPSec łączące VpnGateway z odległym rozgałęzieniem klientów, reprezentowany w dodatku RM jako VpnSite.</span><span class="sxs-lookup"><span data-stu-id="843bd-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="843bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="843bd-104">SYNTAX</span></span>

### <span data-ttu-id="843bd-105">ByVpnGatewayNameByVpnSiteObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="843bd-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843bd-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="843bd-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843bd-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="843bd-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843bd-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="843bd-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843bd-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="843bd-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843bd-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="843bd-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="843bd-111">Opis</span><span class="sxs-lookup"><span data-stu-id="843bd-111">DESCRIPTION</span></span>
<span data-ttu-id="843bd-112">Tworzy połączenie IPSec łączące VpnGateway z odległym rozgałęzieniem klientów, reprezentowany w dodatku RM jako VpnSite.</span><span class="sxs-lookup"><span data-stu-id="843bd-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="843bd-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="843bd-113">EXAMPLES</span></span>

### <span data-ttu-id="843bd-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="843bd-114">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="843bd-115">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="843bd-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="843bd-116">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="843bd-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="843bd-117">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="843bd-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="843bd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="843bd-118">PARAMETERS</span></span>

### <span data-ttu-id="843bd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="843bd-119">-AsJob</span></span>
<span data-ttu-id="843bd-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="843bd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="843bd-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="843bd-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="843bd-122">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="843bd-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="843bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843bd-123">-DefaultProfile</span></span>
<span data-ttu-id="843bd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="843bd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="843bd-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="843bd-125">-EnableBgp</span></span>
<span data-ttu-id="843bd-126">Włącz BGP dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="843bd-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="843bd-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="843bd-127">-IpSecPolicy</span></span>
<span data-ttu-id="843bd-128">Foneros, które muszą być obsługiwane przez to połączenie w MB/s.</span><span class="sxs-lookup"><span data-stu-id="843bd-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="843bd-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="843bd-129">-Name</span></span>
<span data-ttu-id="843bd-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="843bd-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="843bd-131">-ParentObject</span></span>
<span data-ttu-id="843bd-132">VpnGateway nadrzędny dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="843bd-132">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="843bd-133">-ParentResourceId</span></span>
<span data-ttu-id="843bd-134">Identyfikator zasobu dla VpnGateway nadrzędnego dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="843bd-134">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="843bd-135">-ParentResourceName</span></span>
<span data-ttu-id="843bd-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="843bd-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843bd-137">-ResourceGroupName</span></span>
<span data-ttu-id="843bd-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="843bd-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="843bd-139">-SharedKey</span></span>
<span data-ttu-id="843bd-140">Klucz udostępniony wymagany do ustawienia tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="843bd-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="843bd-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="843bd-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="843bd-142">Protokół połączeń z bramą: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="843bd-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="843bd-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="843bd-143">-VpnSite</span></span>
<span data-ttu-id="843bd-144">Zdalna witryna sieci VPN, do której jest podłączone połączenie z siecią wirtualną tego centrum.</span><span class="sxs-lookup"><span data-stu-id="843bd-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="843bd-145">-VpnSiteId</span></span>
<span data-ttu-id="843bd-146">Zdalna witryna sieci VPN, do której jest podłączone połączenie z siecią wirtualną tego centrum.</span><span class="sxs-lookup"><span data-stu-id="843bd-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843bd-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="843bd-147">-Confirm</span></span>
<span data-ttu-id="843bd-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="843bd-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="843bd-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="843bd-149">-WhatIf</span></span>
<span data-ttu-id="843bd-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="843bd-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="843bd-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="843bd-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="843bd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843bd-152">CommonParameters</span></span>
<span data-ttu-id="843bd-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843bd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843bd-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="843bd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843bd-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="843bd-155">INPUTS</span></span>

### <span data-ttu-id="843bd-156">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="843bd-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="843bd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="843bd-157">System.String</span></span>

## <span data-ttu-id="843bd-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="843bd-158">OUTPUTS</span></span>

### <span data-ttu-id="843bd-159">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="843bd-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="843bd-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="843bd-160">NOTES</span></span>

## <span data-ttu-id="843bd-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="843bd-161">RELATED LINKS</span></span>

[<span data-ttu-id="843bd-162">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="843bd-162">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="843bd-163">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="843bd-163">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="843bd-164">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="843bd-164">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)