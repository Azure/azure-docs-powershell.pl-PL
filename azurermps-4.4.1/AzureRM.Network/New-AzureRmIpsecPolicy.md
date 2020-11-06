---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: 17b24668d497cd8d4405865d40f2969219ede719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551803"
---
# <span data-ttu-id="50e70-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="50e70-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="50e70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50e70-102">SYNOPSIS</span></span>
<span data-ttu-id="50e70-103">Tworzy zasady IPSec.</span><span class="sxs-lookup"><span data-stu-id="50e70-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50e70-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e70-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50e70-105">DESCRIPTION</span></span>
<span data-ttu-id="50e70-106">Polecenie cmdlet New-AzureRmIpsecPolicy powoduje utworzenie propozycji zasad IPSec, która ma być używana w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50e70-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="50e70-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50e70-107">EXAMPLES</span></span>

### <span data-ttu-id="50e70-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50e70-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="50e70-109">Tworzenie zasad IPSec, które mają być używane w przypadku nowego połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50e70-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="50e70-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50e70-110">PARAMETERS</span></span>

### <span data-ttu-id="50e70-111">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="50e70-111">-DhGroup</span></span>
<span data-ttu-id="50e70-112">Grupy DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="50e70-112">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="50e70-113">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="50e70-113">-IkeEncryption</span></span>
<span data-ttu-id="50e70-114">Algorytm szyfrowania IKE (faza IKE 2)</span><span class="sxs-lookup"><span data-stu-id="50e70-114">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="50e70-115">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="50e70-115">-IkeIntegrity</span></span>
<span data-ttu-id="50e70-116">Algorytm integralności IKE (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="50e70-116">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="50e70-117">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="50e70-117">-IpsecEncryption</span></span>
<span data-ttu-id="50e70-118">Algorytm szyfrowania protokołu IPSec (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="50e70-118">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="50e70-119">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="50e70-119">-IpsecIntegrity</span></span>
<span data-ttu-id="50e70-120">Algorytm integralności protokołu IPSec (Usługa IKE faza 1)</span><span class="sxs-lookup"><span data-stu-id="50e70-120">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="50e70-121">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="50e70-121">-PfsGroup</span></span>
<span data-ttu-id="50e70-122">Grupy DH używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="50e70-122">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="50e70-123">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="50e70-123">-SADataSizeKilobytes</span></span>
<span data-ttu-id="50e70-124">Rozmiar ładunku skojarzenia zabezpieczeń IPSec (nazywany także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń) w KB</span><span class="sxs-lookup"><span data-stu-id="50e70-124">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="50e70-125">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="50e70-125">-SALifeTimeSeconds</span></span>
<span data-ttu-id="50e70-126">W sekundach skojarzenia zabezpieczeń IPSec (nazywanego także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń)</span><span class="sxs-lookup"><span data-stu-id="50e70-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="50e70-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e70-127">-DefaultProfile</span></span>
<span data-ttu-id="50e70-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50e70-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e70-129">CommonParameters</span></span>
<span data-ttu-id="50e70-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e70-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e70-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e70-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50e70-132">INPUTS</span></span>

### <span data-ttu-id="50e70-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="50e70-133">None</span></span>

## <span data-ttu-id="50e70-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50e70-134">OUTPUTS</span></span>

### <span data-ttu-id="50e70-135">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="50e70-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="50e70-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50e70-136">NOTES</span></span>

## <span data-ttu-id="50e70-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50e70-137">RELATED LINKS</span></span>

