---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964113"
---
# <span data-ttu-id="fb444-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fb444-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="fb444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb444-102">SYNOPSIS</span></span>
<span data-ttu-id="fb444-103">To polecenie umożliwia użytkownikom utworzenie obiektu zasad vpn ipsec określającego jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="fb444-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="fb444-104">To polecenie pozwala obiektowi wyjścioweowi na ustawianie zasad ipsec sieci vpn zarówno dla nowej/ istniejącej bramy, jak i dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="fb444-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="fb444-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb444-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb444-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb444-106">DESCRIPTION</span></span>
<span data-ttu-id="fb444-107">To polecenie umożliwia użytkownikom utworzenie obiektu zasad vpn ipsec określającego jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="fb444-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="fb444-108">To polecenie pozwala obiektowi wyjścioweowi na ustawianie zasad ipsec sieci vpn zarówno dla nowej/ istniejącej bramy, jak i dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="fb444-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="fb444-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb444-109">EXAMPLES</span></span>

### <span data-ttu-id="fb444-110">Przykład 1. Definiowanie obiektu zasad vpn ipsec:</span><span class="sxs-lookup"><span data-stu-id="fb444-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="fb444-111">To polecenie cmdlet służy do tworzenia obiektu zasad vpn ipsec przy użyciu wartości przekazywanego jednego lub wszystkich parametrów, które użytkownik może przekazać do parametru:VpnClientIpsecPolicy z polecenia PS let: New-AzVirtualNetworkGateway (Tworzenie nowej bramy VPN) / Set-AzVirtualNetworkGateway (istniejąca aktualizacja bramy VPN) w grupie Zasobów:</span><span class="sxs-lookup"><span data-stu-id="fb444-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="fb444-112">Przykład 2. Tworzenie nowej bramy sieci wirtualnej z ustawieniem niestandardowych zasad ipsec sieci vpn:</span><span class="sxs-lookup"><span data-stu-id="fb444-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="fb444-113">To polecenie cmdlet zwraca obiekt wirtualnej bramy sieciowej po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="fb444-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="fb444-114">Przykład 3. Ustawianie niestandardowych zasad ipsec sieci vpn dla istniejącej bramy sieci wirtualnej:</span><span class="sxs-lookup"><span data-stu-id="fb444-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="fb444-115">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad ipsec sieci vpn.</span><span class="sxs-lookup"><span data-stu-id="fb444-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="fb444-116">Przykład 4. Uzyskaj wirtualną bramę sieciową, aby sprawdzić, czy niestandardowe zasady sieci vpn są poprawnie ustawione:</span><span class="sxs-lookup"><span data-stu-id="fb444-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="fb444-117">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb444-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="fb444-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb444-118">PARAMETERS</span></span>

### <span data-ttu-id="fb444-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb444-119">-DefaultProfile</span></span>
<span data-ttu-id="fb444-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb444-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb444-121">- DhGroup</span><span class="sxs-lookup"><span data-stu-id="fb444-121">-DhGroup</span></span>
<span data-ttu-id="fb444-122">Grupy VPNClient DH używane w IKE Phase 1 dla początkowego SA</span><span class="sxs-lookup"><span data-stu-id="fb444-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-123">- IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="fb444-123">-IkeEncryption</span></span>
<span data-ttu-id="fb444-124">Algorytm szyfrowania IKE vpnClient (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="fb444-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="fb444-125">-IkeIntegrity</span></span>
<span data-ttu-id="fb444-126">Algorytm integralności IKE vpnClient (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="fb444-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="fb444-127">-IpsecEncryption</span></span>
<span data-ttu-id="fb444-128">Algorytm szyfrowania IPSec usługi VpnClient (etap IKE 1)</span><span class="sxs-lookup"><span data-stu-id="fb444-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="fb444-129">-IpsecIntegrity</span></span>
<span data-ttu-id="fb444-130">Algorytm integralności IPSec usługi VpnClient (etap IKE 1)</span><span class="sxs-lookup"><span data-stu-id="fb444-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-131">- PfsGroup</span><span class="sxs-lookup"><span data-stu-id="fb444-131">-PfsGroup</span></span>
<span data-ttu-id="fb444-132">Grupy VPNClient PFS używane w fazie 2 IKE dla nowego dziecka SA</span><span class="sxs-lookup"><span data-stu-id="fb444-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="fb444-133">-SADataSize</span></span>
<span data-ttu-id="fb444-134">Rozmiar ładowania vpnClient IPSec Security Association (nazywany również szybkim trybem lub etapem 2 SA) w KB</span><span class="sxs-lookup"><span data-stu-id="fb444-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="fb444-135">-SALifeTime</span></span>
<span data-ttu-id="fb444-136">Okres istnienia skojarzenia zabezpieczeń IPSec usługi VpnClient (nazywanego również trybem szybkim lub etapem 2 SA) w ciągu kilku sekund</span><span class="sxs-lookup"><span data-stu-id="fb444-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb444-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb444-137">CommonParameters</span></span>
<span data-ttu-id="fb444-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb444-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb444-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb444-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb444-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb444-140">INPUTS</span></span>

### <span data-ttu-id="fb444-141">Brak</span><span class="sxs-lookup"><span data-stu-id="fb444-141">None</span></span>

## <span data-ttu-id="fb444-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb444-142">OUTPUTS</span></span>

### <span data-ttu-id="fb444-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fb444-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="fb444-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb444-144">NOTES</span></span>

## <span data-ttu-id="fb444-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb444-145">RELATED LINKS</span></span>
