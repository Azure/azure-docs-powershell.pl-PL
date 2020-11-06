---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553483"
---
# <span data-ttu-id="31ab7-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="31ab7-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="31ab7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="31ab7-103">To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="31ab7-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="31ab7-104">To polecenie umożliwia obiektowi Output określenie zasad IPSec dla sieci VPN zarówno dla bramy New/dopełnienie.</span><span class="sxs-lookup"><span data-stu-id="31ab7-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ab7-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31ab7-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ab7-106">Opis</span><span class="sxs-lookup"><span data-stu-id="31ab7-106">DESCRIPTION</span></span>
<span data-ttu-id="31ab7-107">To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="31ab7-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="31ab7-108">To polecenie umożliwia obiektowi Output określenie zasad IPSec dla sieci VPN zarówno dla bramy New/dopełnienie.</span><span class="sxs-lookup"><span data-stu-id="31ab7-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="31ab7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31ab7-109">EXAMPLES</span></span>

### <span data-ttu-id="31ab7-110">Definiowanie obiektu zasad IPSec sieci VPN:</span><span class="sxs-lookup"><span data-stu-id="31ab7-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="31ab7-111">To polecenie cmdlet służy do tworzenia obiektu zasad IPSec sieci VPN przy użyciu wartości przekazana jedna lub wszystkie parametry ', które użytkownik może przekazać do parametru PARAM: VpnClientIpsecPolicy z polecenia PS: New-AzureRmVirtualNetworkGateway (Tworzenie nowego bramy sieci VPN)/Set-AzureRmVirtualNetworkGateway (istniejąca aktualizacja bramy sieci VPN) w obszarze zasobów.</span><span class="sxs-lookup"><span data-stu-id="31ab7-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="31ab7-112">Utwórz nową bramę sieci wirtualnej z ustawieniem niestandardowych zasad IPSec sieci VPN:</span><span class="sxs-lookup"><span data-stu-id="31ab7-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="31ab7-113">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="31ab7-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="31ab7-114">Ustawianie niestandardowych zasad IPSec sieci VPN w istniejącej bramie sieci wirtualnej:</span><span class="sxs-lookup"><span data-stu-id="31ab7-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="31ab7-115">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad IPSec sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="31ab7-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="31ab7-116">Uzyskaj bramę sieci wirtualnej, aby sprawdzić, czy zasady niestandardowe sieci VPN są ustawione poprawnie:</span><span class="sxs-lookup"><span data-stu-id="31ab7-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="31ab7-117">To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31ab7-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="31ab7-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31ab7-118">PARAMETERS</span></span>

### <span data-ttu-id="31ab7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ab7-119">-DefaultProfile</span></span>
<span data-ttu-id="31ab7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31ab7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ab7-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="31ab7-121">-DhGroup</span></span>
<span data-ttu-id="31ab7-122">Grupy Vpnclient DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="31ab7-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="31ab7-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="31ab7-123">-IkeEncryption</span></span>
<span data-ttu-id="31ab7-124">Algorytm szyfrowania Vpnclient IKE (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="31ab7-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="31ab7-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="31ab7-125">-IkeIntegrity</span></span>
<span data-ttu-id="31ab7-126">Algorytm integralności usługi IKE Vpnclient (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="31ab7-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="31ab7-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="31ab7-127">-IpsecEncryption</span></span>
<span data-ttu-id="31ab7-128">Algorytm szyfrowania IPSec Vpnclient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="31ab7-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="31ab7-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="31ab7-129">-IpsecIntegrity</span></span>
<span data-ttu-id="31ab7-130">Algorytm integralności protokołu IPSec Vpnclient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="31ab7-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="31ab7-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="31ab7-131">-PfsGroup</span></span>
<span data-ttu-id="31ab7-132">Grupy PFS Vpnclient używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="31ab7-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="31ab7-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="31ab7-133">-SADataSize</span></span>
<span data-ttu-id="31ab7-134">Rozmiar ładunku skojarzenia zabezpieczeń IPSec Vpnclient (nazywanego także trybem szybkim lub fazą 2 SA) w KB</span><span class="sxs-lookup"><span data-stu-id="31ab7-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="31ab7-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="31ab7-135">-SALifeTime</span></span>
<span data-ttu-id="31ab7-136">W sekundach skojarzenie zabezpieczeń IPSec Vpnclient (nazywane także trybem szybkim lub fazą 2 SA)</span><span class="sxs-lookup"><span data-stu-id="31ab7-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="31ab7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ab7-137">CommonParameters</span></span>
<span data-ttu-id="31ab7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ab7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ab7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ab7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ab7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31ab7-140">INPUTS</span></span>

### <span data-ttu-id="31ab7-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="31ab7-141">None</span></span>

## <span data-ttu-id="31ab7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31ab7-142">OUTPUTS</span></span>

### <span data-ttu-id="31ab7-143">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="31ab7-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="31ab7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31ab7-144">NOTES</span></span>

## <span data-ttu-id="31ab7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31ab7-145">RELATED LINKS</span></span>
