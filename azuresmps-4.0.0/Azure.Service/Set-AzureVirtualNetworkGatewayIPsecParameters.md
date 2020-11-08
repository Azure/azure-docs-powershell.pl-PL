---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055378"
---
# <span data-ttu-id="c263f-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c263f-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="c263f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c263f-102">SYNOPSIS</span></span>
<span data-ttu-id="c263f-103">Ustawia parametry protokołu IPsec dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c263f-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="c263f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c263f-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c263f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c263f-105">DESCRIPTION</span></span>
<span data-ttu-id="c263f-106">Polecenie cmdlet **Set-AzureVirtualNetworkGatewayIPsecParameters** ustawia parametry protokołu IPSec dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c263f-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="c263f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c263f-107">EXAMPLES</span></span>

## <span data-ttu-id="c263f-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c263f-108">PARAMETERS</span></span>

### <span data-ttu-id="c263f-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c263f-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c263f-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="c263f-110">Specifies the ID of a connected entity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c263f-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="c263f-111">-EncryptionType</span></span>
<span data-ttu-id="c263f-112">Określa typ szyfrowania dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c263f-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="c263f-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c263f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c263f-114">Noszyfrowania</span><span class="sxs-lookup"><span data-stu-id="c263f-114">NoEncryption</span></span>
- <span data-ttu-id="c263f-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="c263f-115">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c263f-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c263f-116">-GatewayId</span></span>
<span data-ttu-id="c263f-117">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="c263f-117">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c263f-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="c263f-118">-PfsGroup</span></span>
<span data-ttu-id="c263f-119">Określa grupę doskonałego utajnienia przekazywania (PFS).</span><span class="sxs-lookup"><span data-stu-id="c263f-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="c263f-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c263f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c263f-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="c263f-121">PFS1</span></span>
- <span data-ttu-id="c263f-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c263f-122">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c263f-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="c263f-123">-Profile</span></span>
<span data-ttu-id="c263f-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c263f-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c263f-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c263f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c263f-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="c263f-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="c263f-127">Określa rozmiar w kilobajtach skojarzenia zabezpieczeń (SA).</span><span class="sxs-lookup"><span data-stu-id="c263f-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="c263f-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="c263f-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="c263f-129">Określa w sekundach okres skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="c263f-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="c263f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c263f-130">CommonParameters</span></span>
<span data-ttu-id="c263f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c263f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c263f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c263f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c263f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c263f-133">INPUTS</span></span>

## <span data-ttu-id="c263f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c263f-134">OUTPUTS</span></span>

## <span data-ttu-id="c263f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c263f-135">NOTES</span></span>

## <span data-ttu-id="c263f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c263f-136">RELATED LINKS</span></span>

[<span data-ttu-id="c263f-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="c263f-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


