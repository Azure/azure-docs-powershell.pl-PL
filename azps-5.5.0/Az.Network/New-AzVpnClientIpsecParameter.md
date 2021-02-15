---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187002"
---
# <span data-ttu-id="5ddb6-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="5ddb6-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="5ddb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ddb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddb6-103">To polecenie umożliwia użytkownikom utworzenie obiektu parametrów ipsec połączenia Vpn, który określa jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla istniejącej bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="5ddb6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ddb6-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ddb6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ddb6-105">DESCRIPTION</span></span>
<span data-ttu-id="5ddb6-106">To polecenie umożliwia użytkownikom utworzenie obiektu parametrów ipsec połączenia Vpn, który określa jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla istniejącej bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="5ddb6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ddb6-107">EXAMPLES</span></span>

### <span data-ttu-id="5ddb6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ddb6-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="5ddb6-109">New-AzVpnClientIpsecParameter cmdlet służy do tworzenia obiektu parametrów ipsec sieci vpn w celu użycia wartości przekazywanego jednego lub wszystkich parametrów, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w grupie Zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="5ddb6-110">Ten utworzony obiekt VpnClientIPsecParameters jest przekazywany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych niestandardowych zasad ipsec połączenia Vpn dla wirtualnej bramy sieciowej, jak pokazano w powyższym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="5ddb6-111">To polecenie zwraca obiekt VpnClientIPsecParameters, który pokazuje ustawione parametry.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="5ddb6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ddb6-112">PARAMETERS</span></span>

### <span data-ttu-id="5ddb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddb6-113">-DefaultProfile</span></span>
<span data-ttu-id="5ddb6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ddb6-115">- DhGroup</span><span class="sxs-lookup"><span data-stu-id="5ddb6-115">-DhGroup</span></span>
<span data-ttu-id="5ddb6-116">Grupy VPNClient DH używane w IKE Phase 1 dla początkowego SA.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="5ddb6-117">- IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="5ddb6-117">-IkeEncryption</span></span>
<span data-ttu-id="5ddb6-118">Algorytm szyfrowania IKE vpnClient (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="5ddb6-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="5ddb6-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="5ddb6-119">-IkeIntegrity</span></span>
<span data-ttu-id="5ddb6-120">Algorytm integralności IKE vpnClient (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="5ddb6-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="5ddb6-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="5ddb6-121">-IpsecEncryption</span></span>
<span data-ttu-id="5ddb6-122">Algorytm szyfrowania IPSec usługi VpnClient (etap IKE 1)</span><span class="sxs-lookup"><span data-stu-id="5ddb6-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="5ddb6-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="5ddb6-123">-IpsecIntegrity</span></span>
<span data-ttu-id="5ddb6-124">Algorytm integralności IPSec usługi VpnClient (etap IKE 1)</span><span class="sxs-lookup"><span data-stu-id="5ddb6-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="5ddb6-125">- PfsGroup</span><span class="sxs-lookup"><span data-stu-id="5ddb6-125">-PfsGroup</span></span>
<span data-ttu-id="5ddb6-126">Grupy VPNClient PFS używane w fazie 2 IKE dla nowego dziecka SA</span><span class="sxs-lookup"><span data-stu-id="5ddb6-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="5ddb6-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="5ddb6-127">-SADataSize</span></span>
<span data-ttu-id="5ddb6-128">Rozmiar ładowania vpnClient IPSec Security Association (nazywany również szybkim trybem lub etapem 2 SA) w KB</span><span class="sxs-lookup"><span data-stu-id="5ddb6-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="5ddb6-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="5ddb6-129">-SALifeTime</span></span>
<span data-ttu-id="5ddb6-130">Okres istnienia skojarzenia zabezpieczeń IPSec usługi VpnClient (nazywanego również trybem szybkim lub etapem 2 SA) w ciągu kilku sekund</span><span class="sxs-lookup"><span data-stu-id="5ddb6-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="5ddb6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-131">CommonParameters</span></span>
<span data-ttu-id="5ddb6-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddb6-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddb6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddb6-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ddb6-134">INPUTS</span></span>

### <span data-ttu-id="5ddb6-135">Brak</span><span class="sxs-lookup"><span data-stu-id="5ddb6-135">None</span></span>

## <span data-ttu-id="5ddb6-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ddb6-136">OUTPUTS</span></span>

### <span data-ttu-id="5ddb6-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="5ddb6-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ddb6-138">NOTES</span></span>

## <span data-ttu-id="5ddb6-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ddb6-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ddb6-140">Get-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="5ddb6-141">Remove-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="5ddb6-142">Set-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
