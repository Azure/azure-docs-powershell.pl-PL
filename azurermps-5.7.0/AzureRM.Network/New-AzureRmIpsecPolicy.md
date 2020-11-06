---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: b5a5b3d9844a06e75938a2b87987f5a1f71f04e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548903"
---
# <span data-ttu-id="9152a-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9152a-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="9152a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9152a-102">SYNOPSIS</span></span>
<span data-ttu-id="9152a-103">Tworzy zasady IPSec.</span><span class="sxs-lookup"><span data-stu-id="9152a-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9152a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9152a-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9152a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9152a-105">DESCRIPTION</span></span>
<span data-ttu-id="9152a-106">Polecenie cmdlet New-AzureRmIpsecPolicy powoduje utworzenie propozycji zasad IPSec, która ma być używana w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9152a-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="9152a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9152a-107">EXAMPLES</span></span>

### <span data-ttu-id="9152a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9152a-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="9152a-109">Tworzenie zasad IPSec, które mają być używane w przypadku nowego połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9152a-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="9152a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9152a-110">PARAMETERS</span></span>

### <span data-ttu-id="9152a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9152a-111">-DefaultProfile</span></span>
<span data-ttu-id="9152a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9152a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="9152a-113">-DhGroup</span></span>
<span data-ttu-id="9152a-114">Grupy DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="9152a-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="9152a-115">-IkeEncryption</span></span>
<span data-ttu-id="9152a-116">Algorytm szyfrowania IKE (faza IKE 2)</span><span class="sxs-lookup"><span data-stu-id="9152a-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="9152a-117">-IkeIntegrity</span></span>
<span data-ttu-id="9152a-118">Algorytm integralności IKE (Usługa IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="9152a-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="9152a-119">-IpsecEncryption</span></span>
<span data-ttu-id="9152a-120">Algorytm szyfrowania protokołu IPSec (faza IKE 1)</span><span class="sxs-lookup"><span data-stu-id="9152a-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="9152a-121">-IpsecIntegrity</span></span>
<span data-ttu-id="9152a-122">Algorytm integralności protokołu IPSec (Usługa IKE faza 1)</span><span class="sxs-lookup"><span data-stu-id="9152a-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="9152a-123">-PfsGroup</span></span>
<span data-ttu-id="9152a-124">Grupy DH używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA</span><span class="sxs-lookup"><span data-stu-id="9152a-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="9152a-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="9152a-126">Rozmiar ładunku skojarzenia zabezpieczeń IPSec (nazywany także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń) w KB</span><span class="sxs-lookup"><span data-stu-id="9152a-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="9152a-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="9152a-128">W sekundach skojarzenia zabezpieczeń IPSec (nazywanego także trybem szybkim lub fazą 2 skojarzeń zabezpieczeń)</span><span class="sxs-lookup"><span data-stu-id="9152a-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9152a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9152a-129">CommonParameters</span></span>
<span data-ttu-id="9152a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9152a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9152a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9152a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9152a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9152a-132">INPUTS</span></span>

### <span data-ttu-id="9152a-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9152a-133">None</span></span>

## <span data-ttu-id="9152a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9152a-134">OUTPUTS</span></span>

### <span data-ttu-id="9152a-135">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9152a-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="9152a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9152a-136">NOTES</span></span>

## <span data-ttu-id="9152a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9152a-137">RELATED LINKS</span></span>

