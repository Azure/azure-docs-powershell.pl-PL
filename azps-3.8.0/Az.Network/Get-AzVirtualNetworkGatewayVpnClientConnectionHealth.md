---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 9033d389990efb7bf17c568512becedaf475cc56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050346"
---
# <span data-ttu-id="5a51d-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5a51d-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="5a51d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a51d-102">SYNOPSIS</span></span> 
<span data-ttu-id="5a51d-103">Uzyskiwanie listy kondycji połączenia klienta VPN bramy sieci wirtualnej platformy Azure dla połączenia klienta sieci VPN</span><span class="sxs-lookup"><span data-stu-id="5a51d-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="5a51d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a51d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="5a51d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a51d-105">DESCRIPTION</span></span>
<span data-ttu-id="5a51d-106">Lista wszystkich połączonych kondycji połączeń klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="5a51d-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="5a51d-107">Dotyczy to: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="5a51d-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="5a51d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a51d-108">EXAMPLES</span></span>

### <span data-ttu-id="5a51d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a51d-109">Example 1</span></span>
```
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

<span data-ttu-id="5a51d-110">W przypadku bramy sieci wirtualnej platformy Azure o nazwie bramaname w grupie zasób do przeprowadzenia grup zasobów Pobiera obecnie połączone połączenie klienta VPN przy użyciu OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="5a51d-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

## <span data-ttu-id="5a51d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a51d-111">PARAMETERS</span></span>

### <span data-ttu-id="5a51d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a51d-112">-ResourceGroupName</span></span>
<span data-ttu-id="5a51d-113">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a51d-113">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="5a51d-114">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5a51d-114">-ResourceName</span></span>
<span data-ttu-id="5a51d-115">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a51d-115">Virtual network gateway name</span></span>

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
### <span data-ttu-id="5a51d-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a51d-116">-ResourceId</span></span>
<span data-ttu-id="5a51d-117">Identyfikator zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a51d-117">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="5a51d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a51d-118">-InputObject</span></span>
<span data-ttu-id="5a51d-119">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a51d-119">Virtual network gateway object</span></span>

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

### <span data-ttu-id="5a51d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a51d-120">-AsJob</span></span>
<span data-ttu-id="5a51d-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5a51d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a51d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a51d-122">CommonParameters</span></span>
<span data-ttu-id="5a51d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a51d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a51d-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a51d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a51d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a51d-125">INPUTS</span></span>

### <span data-ttu-id="5a51d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5a51d-126">System.String</span></span>

## <span data-ttu-id="5a51d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a51d-127">OUTPUTS</span></span>

### <span data-ttu-id="5a51d-128">Microsoft. Azure. Commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="5a51d-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="5a51d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a51d-129">NOTES</span></span>

## <span data-ttu-id="5a51d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a51d-130">RELATED LINKS</span></span>
