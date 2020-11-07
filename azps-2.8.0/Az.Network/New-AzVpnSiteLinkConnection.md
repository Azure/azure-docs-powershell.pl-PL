---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: e62e697deec0d7e3894e7eaf787790f64d72641b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871316"
---
# <span data-ttu-id="7665a-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7665a-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="7665a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7665a-102">SYNOPSIS</span></span>
<span data-ttu-id="7665a-103">Tworzy obiekt Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="7665a-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="7665a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7665a-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7665a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7665a-105">DESCRIPTION</span></span>
<span data-ttu-id="7665a-106">Tworzy obiekt Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="7665a-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="7665a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7665a-107">EXAMPLES</span></span>

### <span data-ttu-id="7665a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7665a-108">Example 1</span></span>
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

<span data-ttu-id="7665a-109">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite z 1 VpnSiteLinks na zachodnim terenie Stanów Zjednoczonych w obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7665a-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="7665a-110">Brama sieci VPN zostanie utworzona później w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="7665a-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="7665a-111">Po utworzeniu bramy jest ona połączona z VpnSite za pomocą polecenia New-AzVpnConnection z 1 VpnSiteLinkConnections na VpnSiteLink VpnSite.</span><span class="sxs-lookup"><span data-stu-id="7665a-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="7665a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7665a-112">PARAMETERS</span></span>

### <span data-ttu-id="7665a-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="7665a-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="7665a-114">Przepustowość, która musi być obsługiwana przez to połączenie linku w MB/s.</span><span class="sxs-lookup"><span data-stu-id="7665a-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="7665a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7665a-115">-DefaultProfile</span></span>
<span data-ttu-id="7665a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7665a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7665a-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7665a-117">-EnableBgp</span></span>
<span data-ttu-id="7665a-118">Włącz protokół BGP dla tego połączenia linku</span><span class="sxs-lookup"><span data-stu-id="7665a-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="7665a-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7665a-119">-IpSecPolicy</span></span>
<span data-ttu-id="7665a-120">Zasady IpSec, które należy uwzględnić w przypadku tego połączenia z linkiem.</span><span class="sxs-lookup"><span data-stu-id="7665a-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="7665a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7665a-121">-Name</span></span>
<span data-ttu-id="7665a-122">Nazwę</span><span class="sxs-lookup"><span data-stu-id="7665a-122">Name</span></span>

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

### <span data-ttu-id="7665a-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7665a-123">-RoutingWeight</span></span>
<span data-ttu-id="7665a-124">Waga routingu</span><span class="sxs-lookup"><span data-stu-id="7665a-124">Routing Weight</span></span>

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

### <span data-ttu-id="7665a-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7665a-125">-SharedKey</span></span>
<span data-ttu-id="7665a-126">Klucz udostępniony wymagany do ustawienia tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="7665a-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="7665a-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7665a-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7665a-128">Użyj lokalnego adresu IP platformy Azure jako źródłowego adresu IP dla tego połączenia linku.</span><span class="sxs-lookup"><span data-stu-id="7665a-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="7665a-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7665a-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7665a-130">Użyj selektorów ruchu opartego na zasadach dla tego połączenia z linkiem.</span><span class="sxs-lookup"><span data-stu-id="7665a-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="7665a-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="7665a-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="7665a-132">Protokół połączeń z bramą: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="7665a-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="7665a-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7665a-133">-VpnSiteLink</span></span>
<span data-ttu-id="7665a-134">Obiekt linku witryny sieci VPN, z którym chcesz nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="7665a-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="7665a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7665a-135">CommonParameters</span></span>
<span data-ttu-id="7665a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7665a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7665a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7665a-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7665a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7665a-138">INPUTS</span></span>

### <span data-ttu-id="7665a-139">Microsoft. Azure. Commands. Network. models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7665a-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="7665a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7665a-140">OUTPUTS</span></span>

### <span data-ttu-id="7665a-141">Microsoft. Azure. Commands. Network. models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7665a-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="7665a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7665a-142">NOTES</span></span>

## <span data-ttu-id="7665a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7665a-143">RELATED LINKS</span></span>

[<span data-ttu-id="7665a-144">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7665a-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)