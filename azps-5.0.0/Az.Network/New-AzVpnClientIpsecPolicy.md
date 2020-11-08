---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234119"
---
# <span data-ttu-id="b3eac-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b3eac-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="b3eac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3eac-102">SYNOPSIS</span></span>
<span data-ttu-id="b3eac-103">To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="b3eac-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="b3eac-104">To polecenie umożliwia obiektowi Output określenie zasad IPSec sieci VPN zarówno dla nowej, jak i istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="b3eac-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="b3eac-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3eac-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3eac-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b3eac-106">DESCRIPTION</span></span>
<span data-ttu-id="b3eac-107">To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="b3eac-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="b3eac-108">To polecenie umożliwia obiektowi Output określenie zasad IPSec sieci VPN zarówno dla nowej, jak i istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="b3eac-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="b3eac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3eac-109">EXAMPLES</span></span>

### <span data-ttu-id="b3eac-110">Przykład 1: Definiowanie obiektu zasad IPSec sieci VPN:</span><span class="sxs-lookup"><span data-stu-id="b3eac-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="b3eac-111">To polecenie cmdlet służy do tworzenia obiektu zasad IPSec sieci VPN przy użyciu wartości przekazana jedna lub wszystkie parametry ', które użytkownik może przekazać do parametru PARAM: VpnClientIpsecPolicy z polecenia PS: New-AzVirtualNetworkGateway (Tworzenie nowego bramy sieci VPN)/Set-AzVirtualNetworkGateway (istniejąca aktualizacja bramy sieci VPN) w obszarze zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3eac-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="b3eac-112">Przykład 2: Utwórz nową bramę sieci wirtualnej z ustawieniem niestandardowych zasad IPSec sieci VPN:</span><span class="sxs-lookup"><span data-stu-id="b3eac-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="b3eac-113">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="b3eac-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="b3eac-114">Przykład 3: Ustawianie niestandardowych zasad IPSec sieci VPN w istniejącej bramie sieci wirtualnej:</span><span class="sxs-lookup"><span data-stu-id="b3eac-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="b3eac-115">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad IPSec sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="b3eac-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="b3eac-116">Przykład 4: Uzyskaj wirtualną bramę sieciową, aby sprawdzić, czy zasady niestandardowe sieci VPN są ustawione poprawnie:</span><span class="sxs-lookup"><span data-stu-id="b3eac-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="b3eac-117">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3eac-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="b3eac-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3eac-118">PARAMETERS</span></span>

### <span data-ttu-id="b3eac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3eac-119">-DefaultProfile</span></span>
<span data-ttu-id="b3eac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3eac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3eac-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="b3eac-121">-DhGroup</span></span>
<span data-ttu-id="b3eac-122">Grupy VpnClient DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="b3eac-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="b3eac-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="b3eac-123">-IkeEncryption</span></span>
<span data-ttu-id="b3eac-124">Algorytm szyfrowania VpnClient IKE (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="b3eac-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="b3eac-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="b3eac-125">-IkeIntegrity</span></span>
<span data-ttu-id="b3eac-126">Algorytm integralności usługi IKE VpnClient (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="b3eac-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="b3eac-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="b3eac-127">-IpsecEncryption</span></span>
<span data-ttu-id="b3eac-128">Algorytm szyfrowania IPSec VpnClient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="b3eac-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="b3eac-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="b3eac-129">-IpsecIntegrity</span></span>
<span data-ttu-id="b3eac-130">Algorytm integralności protokołu IPSec VpnClient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="b3eac-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="b3eac-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="b3eac-131">-PfsGroup</span></span>
<span data-ttu-id="b3eac-132">Grupy PFS VpnClient używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="b3eac-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="b3eac-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="b3eac-133">-SADataSize</span></span>
<span data-ttu-id="b3eac-134">Rozmiar ładunku skojarzenia zabezpieczeń IPSec VpnClient (nazywanego także trybem szybkim lub fazą 2 SA) w KB</span><span class="sxs-lookup"><span data-stu-id="b3eac-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="b3eac-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="b3eac-135">-SALifeTime</span></span>
<span data-ttu-id="b3eac-136">W sekundach skojarzenie zabezpieczeń IPSec VpnClient (nazywane także trybem szybkim lub fazą 2 SA)</span><span class="sxs-lookup"><span data-stu-id="b3eac-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="b3eac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3eac-137">CommonParameters</span></span>
<span data-ttu-id="b3eac-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3eac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3eac-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3eac-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3eac-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3eac-140">INPUTS</span></span>

### <span data-ttu-id="b3eac-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3eac-141">None</span></span>

## <span data-ttu-id="b3eac-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3eac-142">OUTPUTS</span></span>

### <span data-ttu-id="b3eac-143">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b3eac-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="b3eac-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3eac-144">NOTES</span></span>

## <span data-ttu-id="b3eac-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3eac-145">RELATED LINKS</span></span>
