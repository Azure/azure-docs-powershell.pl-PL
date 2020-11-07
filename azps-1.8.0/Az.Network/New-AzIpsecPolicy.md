---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 48677fd6f187f20e62a556d9ced0a35dc888f89f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709298"
---
# <span data-ttu-id="c4a69-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a69-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="c4a69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4a69-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a69-103">Tworzy zasady IPSec.</span><span class="sxs-lookup"><span data-stu-id="c4a69-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="c4a69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4a69-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4a69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4a69-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a69-106">Polecenie cmdlet New-AzIpsecPolicy powoduje utworzenie propozycji zasad IPSec, która ma być używana w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4a69-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="c4a69-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4a69-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a69-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4a69-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="c4a69-109">Tworzenie zasad IPSec, które mają być używane w przypadku nowego połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4a69-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="c4a69-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4a69-110">PARAMETERS</span></span>

### <span data-ttu-id="c4a69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a69-111">-DefaultProfile</span></span>
<span data-ttu-id="c4a69-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a69-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a69-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="c4a69-113">-DhGroup</span></span>
<span data-ttu-id="c4a69-114">Grupy DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="c4a69-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="c4a69-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="c4a69-115">-IkeEncryption</span></span>
<span data-ttu-id="c4a69-116">Algorytm szyfrowania IKE (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="c4a69-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="c4a69-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="c4a69-117">-IkeIntegrity</span></span>
<span data-ttu-id="c4a69-118">Algorytm integralności IKE (Usługa IKE faza 1)</span><span class="sxs-lookup"><span data-stu-id="c4a69-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="c4a69-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="c4a69-119">-IpsecEncryption</span></span>
<span data-ttu-id="c4a69-120">Algorytm szyfrowania protokołu IPSec (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="c4a69-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="c4a69-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="c4a69-121">-IpsecIntegrity</span></span>
<span data-ttu-id="c4a69-122">Algorytm integralności protokołu IPSec (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="c4a69-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="c4a69-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="c4a69-123">-PfsGroup</span></span>
<span data-ttu-id="c4a69-124">Grupy DH używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="c4a69-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="c4a69-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="c4a69-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="c4a69-126">Rozmiar ładunku skojarzenia zabezpieczeń IPSec (nazywany także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń) w KB</span><span class="sxs-lookup"><span data-stu-id="c4a69-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="c4a69-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="c4a69-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="c4a69-128">W sekundach skojarzenia zabezpieczeń IPSec (nazywanego także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń)</span><span class="sxs-lookup"><span data-stu-id="c4a69-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="c4a69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a69-129">CommonParameters</span></span>
<span data-ttu-id="c4a69-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a69-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a69-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a69-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4a69-132">INPUTS</span></span>

### <span data-ttu-id="c4a69-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c4a69-133">None</span></span>

## <span data-ttu-id="c4a69-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4a69-134">OUTPUTS</span></span>

### <span data-ttu-id="c4a69-135">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a69-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="c4a69-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4a69-136">NOTES</span></span>

## <span data-ttu-id="c4a69-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4a69-137">RELATED LINKS</span></span>
