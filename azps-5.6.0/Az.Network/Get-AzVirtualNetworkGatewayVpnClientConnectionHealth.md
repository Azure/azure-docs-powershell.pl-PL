---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 560ab8485f9e5860230edeec904d53f57b43aa26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967809"
---
# <span data-ttu-id="18a99-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="18a99-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="18a99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a99-102">SYNOPSIS</span></span> 
<span data-ttu-id="18a99-103">Uzyskiwanie listy kondycji połączenia klienta sieci vpn bramy sieci wirtualnej Azure dla każdego połączenia klienta vpn</span><span class="sxs-lookup"><span data-stu-id="18a99-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="18a99-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18a99-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="18a99-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="18a99-105">DESCRIPTION</span></span>
<span data-ttu-id="18a99-106">Lista wszystkich kondycji połączenia klienta sieci vpn.</span><span class="sxs-lookup"><span data-stu-id="18a99-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="18a99-107">Dotyczy to: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="18a99-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="18a99-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18a99-108">EXAMPLES</span></span>

### <span data-ttu-id="18a99-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18a99-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="18a99-110">W przypadku bramy sieci wirtualnej platformy Azure o nazwie nazwana nazwa bramy w grupie zasobów resourceGroup pobiera obecnie połączone połączenie klienta vpn przy użyciu połączenia OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="18a99-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="18a99-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="18a99-111">Example 2</span></span>

<span data-ttu-id="18a99-112">Uzyskaj listę kondycji połączenia klienta vpn bramy sieci wirtualnej Azure dla każdego połączenia klienta vpn.</span><span class="sxs-lookup"><span data-stu-id="18a99-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="18a99-113">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="18a99-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="18a99-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18a99-114">PARAMETERS</span></span>

### <span data-ttu-id="18a99-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a99-115">-ResourceGroupName</span></span>
<span data-ttu-id="18a99-116">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18a99-116">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="18a99-117">-ResourceName</span></span>
<span data-ttu-id="18a99-118">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18a99-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="18a99-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18a99-119">-ResourceId</span></span>
<span data-ttu-id="18a99-120">Identyfikator zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18a99-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18a99-121">-InputObject</span></span>
<span data-ttu-id="18a99-122">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18a99-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="18a99-123">-AsJob</span></span>
<span data-ttu-id="18a99-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="18a99-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18a99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a99-125">CommonParameters</span></span>
<span data-ttu-id="18a99-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a99-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a99-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a99-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a99-128">INPUTS</span></span>

### <span data-ttu-id="18a99-129">System.String</span><span class="sxs-lookup"><span data-stu-id="18a99-129">System.String</span></span>

## <span data-ttu-id="18a99-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a99-130">OUTPUTS</span></span>

### <span data-ttu-id="18a99-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="18a99-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="18a99-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18a99-132">NOTES</span></span>

## <span data-ttu-id="18a99-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18a99-133">RELATED LINKS</span></span>
