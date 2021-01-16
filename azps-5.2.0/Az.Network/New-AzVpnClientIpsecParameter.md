---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327558"
---
# <span data-ttu-id="00ff9-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00ff9-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="00ff9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="00ff9-103">To polecenie umożliwia użytkownikom tworzenie obiektu parametry protokołu IPsec sieci VPN z podaniem jednej lub wszystkich wartości, takich jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia istniejącej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="00ff9-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="00ff9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00ff9-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ff9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="00ff9-106">To polecenie umożliwia użytkownikom tworzenie obiektu parametry protokołu IPsec sieci VPN z podaniem jednej lub wszystkich wartości, takich jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia istniejącej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="00ff9-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="00ff9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="00ff9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00ff9-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="00ff9-109">Polecenie cmdlet New-AzVpnClientIpsecParameter służy do tworzenia obiektu parametry IPsec sieci VPN z użyciem wartości przekazanych jeden lub wszystkie parametry, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w obszarze zasobów.</span><span class="sxs-lookup"><span data-stu-id="00ff9-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="00ff9-110">Ten obiekt VpnClientIPsecParameters został przekazany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych zasad niestandardowych IPSec VPN w bramie sieci wirtualnej, jak pokazano na przykładzie powyżej.</span><span class="sxs-lookup"><span data-stu-id="00ff9-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="00ff9-111">To polecenie zwraca obiekt VpnClientIPsecParameters, w którym pokazano parametry Set.</span><span class="sxs-lookup"><span data-stu-id="00ff9-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="00ff9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00ff9-112">PARAMETERS</span></span>

### <span data-ttu-id="00ff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ff9-113">-DefaultProfile</span></span>
<span data-ttu-id="00ff9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00ff9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ff9-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="00ff9-115">-DhGroup</span></span>
<span data-ttu-id="00ff9-116">Grupy VpnClient DH używane w usłudze IKE phase 1 w przypadku początkowego skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="00ff9-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="00ff9-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="00ff9-117">-IkeEncryption</span></span>
<span data-ttu-id="00ff9-118">Algorytm szyfrowania VpnClient IKE (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="00ff9-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="00ff9-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="00ff9-119">-IkeIntegrity</span></span>
<span data-ttu-id="00ff9-120">Algorytm integralności usługi IKE VpnClient (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="00ff9-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="00ff9-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="00ff9-121">-IpsecEncryption</span></span>
<span data-ttu-id="00ff9-122">Algorytm szyfrowania IPSec VpnClient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="00ff9-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="00ff9-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="00ff9-123">-IpsecIntegrity</span></span>
<span data-ttu-id="00ff9-124">Algorytm integralności protokołu IPSec VpnClient (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="00ff9-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="00ff9-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="00ff9-125">-PfsGroup</span></span>
<span data-ttu-id="00ff9-126">Grupy PFS VpnClient używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="00ff9-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="00ff9-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="00ff9-127">-SADataSize</span></span>
<span data-ttu-id="00ff9-128">Rozmiar ładunku skojarzenia zabezpieczeń IPSec VpnClient (nazywanego także trybem szybkim lub fazą 2 SA) w KB</span><span class="sxs-lookup"><span data-stu-id="00ff9-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="00ff9-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="00ff9-129">-SALifeTime</span></span>
<span data-ttu-id="00ff9-130">W sekundach skojarzenie zabezpieczeń IPSec VpnClient (nazywane także trybem szybkim lub fazą 2 SA)</span><span class="sxs-lookup"><span data-stu-id="00ff9-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="00ff9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ff9-131">CommonParameters</span></span>
<span data-ttu-id="00ff9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ff9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ff9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ff9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ff9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00ff9-134">INPUTS</span></span>

### <span data-ttu-id="00ff9-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="00ff9-135">None</span></span>

## <span data-ttu-id="00ff9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00ff9-136">OUTPUTS</span></span>

### <span data-ttu-id="00ff9-137">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="00ff9-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="00ff9-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00ff9-138">NOTES</span></span>

## <span data-ttu-id="00ff9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00ff9-139">RELATED LINKS</span></span>

[<span data-ttu-id="00ff9-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00ff9-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00ff9-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00ff9-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00ff9-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00ff9-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
