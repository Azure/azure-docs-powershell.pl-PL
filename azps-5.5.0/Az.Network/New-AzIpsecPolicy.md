---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179698"
---
# <span data-ttu-id="5cbfe-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbfe-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="5cbfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbfe-103">Tworzy zasady IPSec.</span><span class="sxs-lookup"><span data-stu-id="5cbfe-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="5cbfe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5cbfe-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cbfe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5cbfe-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbfe-106">Polecenie New-AzIpsecPolicy cmdlet tworzy propozycję zasad IPSec, która ma być używana w połączeniu z wirtualną bramą sieciową.</span><span class="sxs-lookup"><span data-stu-id="5cbfe-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="5cbfe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5cbfe-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbfe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5cbfe-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="5cbfe-109">Tworzenie zasad IPSec, które mają być używane dla nowego połączenia wirtualnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5cbfe-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="5cbfe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cbfe-110">PARAMETERS</span></span>

### <span data-ttu-id="5cbfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbfe-111">-DefaultProfile</span></span>
<span data-ttu-id="5cbfe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbfe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbfe-113">- DhGroup</span><span class="sxs-lookup"><span data-stu-id="5cbfe-113">-DhGroup</span></span>
<span data-ttu-id="5cbfe-114">Grupy DH używane w fazie 1 IKE dla początkowego sa</span><span class="sxs-lookup"><span data-stu-id="5cbfe-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-115">- IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="5cbfe-115">-IkeEncryption</span></span>
<span data-ttu-id="5cbfe-116">Algorytm szyfrowania IKE (etap 1. IKE)</span><span class="sxs-lookup"><span data-stu-id="5cbfe-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="5cbfe-117">-IkeIntegrity</span></span>
<span data-ttu-id="5cbfe-118">Algorytm integralności IKE (etap 1. IKE)</span><span class="sxs-lookup"><span data-stu-id="5cbfe-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="5cbfe-119">-IpsecEncryption</span></span>
<span data-ttu-id="5cbfe-120">Algorytm szyfrowania IPSec (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="5cbfe-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="5cbfe-121">-IpsecIntegrity</span></span>
<span data-ttu-id="5cbfe-122">Algorytm integralności IPSec (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="5cbfe-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-123">- PfsGroup</span><span class="sxs-lookup"><span data-stu-id="5cbfe-123">-PfsGroup</span></span>
<span data-ttu-id="5cbfe-124">Grupy DH używane w fazie 2 IKE dla nowego dziecka SA</span><span class="sxs-lookup"><span data-stu-id="5cbfe-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbfe-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="5cbfe-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="5cbfe-126">Rozmiar obciążenia skojarzenia zabezpieczeń IPSec (nazywanego również trybem szybkim lub etapem 2 SA) w kb</span><span class="sxs-lookup"><span data-stu-id="5cbfe-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="5cbfe-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="5cbfe-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="5cbfe-128">Okres istnienia skojarzenia zabezpieczeń IPSec (nazywanego również trybem szybkim lub etapem 2 SA) w sekundach</span><span class="sxs-lookup"><span data-stu-id="5cbfe-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="5cbfe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbfe-129">CommonParameters</span></span>
<span data-ttu-id="5cbfe-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbfe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbfe-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbfe-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbfe-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cbfe-132">INPUTS</span></span>

### <span data-ttu-id="5cbfe-133">Brak</span><span class="sxs-lookup"><span data-stu-id="5cbfe-133">None</span></span>

## <span data-ttu-id="5cbfe-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cbfe-134">OUTPUTS</span></span>

### <span data-ttu-id="5cbfe-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbfe-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="5cbfe-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5cbfe-136">NOTES</span></span>

## <span data-ttu-id="5cbfe-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cbfe-137">RELATED LINKS</span></span>
