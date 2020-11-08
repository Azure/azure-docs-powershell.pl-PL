---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055002"
---
# <span data-ttu-id="9d7d7-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="9d7d7-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="9d7d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7d7-103">Ustawia parametry protokołu IPsec dla połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="9d7d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d7d7-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d7d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7d7-106">Polecenie cmdlet **Set-AzureVNetGatewayIPsecParameters** ustawia parametry zabezpieczeń protokołu internetowego (IPSec) i IKE (Internet Key Exchange) połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="9d7d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d7d7-107">EXAMPLES</span></span>

## <span data-ttu-id="9d7d7-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d7d7-108">PARAMETERS</span></span>

### <span data-ttu-id="9d7d7-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="9d7d7-109">-EncryptionType</span></span>
<span data-ttu-id="9d7d7-110">Określa typ szyfrowania dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="9d7d7-111">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9d7d7-111">Valid values are:</span></span> 

- <span data-ttu-id="9d7d7-112">Noszyfrowania</span><span class="sxs-lookup"><span data-stu-id="9d7d7-112">NoEncryption</span></span> 
- <span data-ttu-id="9d7d7-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="9d7d7-113">RequireEncryption</span></span>

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

### <span data-ttu-id="9d7d7-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="9d7d7-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="9d7d7-115">Określa nazwę lokalnego połączenia z lokacją sieciową, dla którego to polecenie cmdlet skonfiguruje parametry protokołu IPsec i IKE.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="9d7d7-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="9d7d7-116">-PfsGroup</span></span>
<span data-ttu-id="9d7d7-117">Określa grupę doskonałego utajnienia przekazywania (PFS).</span><span class="sxs-lookup"><span data-stu-id="9d7d7-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="9d7d7-118">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9d7d7-118">Valid values are:</span></span> 

- <span data-ttu-id="9d7d7-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="9d7d7-119">PFS1</span></span> 
- <span data-ttu-id="9d7d7-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d7d7-120">None</span></span>

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

### <span data-ttu-id="9d7d7-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="9d7d7-121">-Profile</span></span>
<span data-ttu-id="9d7d7-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9d7d7-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d7d7-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="9d7d7-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="9d7d7-125">Określa rozmiar w kilobajtach skojarzenia zabezpieczeń (SA).</span><span class="sxs-lookup"><span data-stu-id="9d7d7-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="9d7d7-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="9d7d7-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="9d7d7-127">Określa w sekundach okres skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="9d7d7-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9d7d7-128">-VNetName</span></span>
<span data-ttu-id="9d7d7-129">Określa sieć wirtualną, w której to polecenie cmdlet ustawia parametry protokołu IPsec dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="9d7d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7d7-130">CommonParameters</span></span>
<span data-ttu-id="9d7d7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7d7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7d7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7d7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d7d7-133">INPUTS</span></span>

## <span data-ttu-id="9d7d7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d7d7-134">OUTPUTS</span></span>

## <span data-ttu-id="9d7d7-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d7d7-135">NOTES</span></span>

## <span data-ttu-id="9d7d7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d7d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d7d7-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="9d7d7-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


