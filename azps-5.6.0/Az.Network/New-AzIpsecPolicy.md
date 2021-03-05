---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 059f94c8289b601d5a368266310e61d665e217fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003578"
---
# <span data-ttu-id="45bac-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="45bac-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="45bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45bac-102">SYNOPSIS</span></span>
<span data-ttu-id="45bac-103">Tworzy zasady IPSec.</span><span class="sxs-lookup"><span data-stu-id="45bac-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="45bac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45bac-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45bac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="45bac-105">DESCRIPTION</span></span>
<span data-ttu-id="45bac-106">Polecenie New-AzIpsecPolicy cmdlet tworzy propozycję zasad IPSec, która ma być używana w połączeniu z wirtualną bramą sieciową.</span><span class="sxs-lookup"><span data-stu-id="45bac-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="45bac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45bac-107">EXAMPLES</span></span>

### <span data-ttu-id="45bac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45bac-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="45bac-109">Tworzenie zasad IPSec, które mają być używane dla nowego połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45bac-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="45bac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45bac-110">PARAMETERS</span></span>

### <span data-ttu-id="45bac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bac-111">-DefaultProfile</span></span>
<span data-ttu-id="45bac-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45bac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45bac-113">- DhGroup</span><span class="sxs-lookup"><span data-stu-id="45bac-113">-DhGroup</span></span>
<span data-ttu-id="45bac-114">Grupy DH używane w fazie 1 IKE dla początkowego sa</span><span class="sxs-lookup"><span data-stu-id="45bac-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="45bac-115">- IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="45bac-115">-IkeEncryption</span></span>
<span data-ttu-id="45bac-116">Algorytm szyfrowania IKE (etap 1. IKE)</span><span class="sxs-lookup"><span data-stu-id="45bac-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="45bac-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="45bac-117">-IkeIntegrity</span></span>
<span data-ttu-id="45bac-118">Algorytm integralności IKE (etap 1. IKE)</span><span class="sxs-lookup"><span data-stu-id="45bac-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="45bac-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="45bac-119">-IpsecEncryption</span></span>
<span data-ttu-id="45bac-120">Algorytm szyfrowania IPSec (etap 2 usługi IKE)</span><span class="sxs-lookup"><span data-stu-id="45bac-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="45bac-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="45bac-121">-IpsecIntegrity</span></span>
<span data-ttu-id="45bac-122">Algorytm integralności IPSec (etap 2. IKE)</span><span class="sxs-lookup"><span data-stu-id="45bac-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="45bac-123">- PfsGroup</span><span class="sxs-lookup"><span data-stu-id="45bac-123">-PfsGroup</span></span>
<span data-ttu-id="45bac-124">Grupy DH używane w fazie 2 IKE dla nowego dziecka SA</span><span class="sxs-lookup"><span data-stu-id="45bac-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="45bac-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="45bac-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="45bac-126">Rozmiar obciążenia skojarzenia zabezpieczeń IPSec (nazywanego również trybem szybkim lub etapem 2 SA) w kb</span><span class="sxs-lookup"><span data-stu-id="45bac-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="45bac-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="45bac-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="45bac-128">Okres istnienia skojarzenia zabezpieczeń IPSec (nazywanego również trybem szybkim lub etapem 2 SA) w sekundach</span><span class="sxs-lookup"><span data-stu-id="45bac-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="45bac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bac-129">CommonParameters</span></span>
<span data-ttu-id="45bac-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bac-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bac-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bac-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45bac-132">INPUTS</span></span>

### <span data-ttu-id="45bac-133">Brak</span><span class="sxs-lookup"><span data-stu-id="45bac-133">None</span></span>

## <span data-ttu-id="45bac-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45bac-134">OUTPUTS</span></span>

### <span data-ttu-id="45bac-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="45bac-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="45bac-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45bac-136">NOTES</span></span>

## <span data-ttu-id="45bac-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45bac-137">RELATED LINKS</span></span>
