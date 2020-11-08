---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054776"
---
# <span data-ttu-id="03b00-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="03b00-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="03b00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03b00-102">SYNOPSIS</span></span>
<span data-ttu-id="03b00-103">Ustawia klucz wstępny dla połączenia między bramą sieci VPN platformy Azure a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="03b00-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="03b00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03b00-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03b00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03b00-105">DESCRIPTION</span></span>
<span data-ttu-id="03b00-106">Polecenie cmdlet **Set-AzureVNetGatewayKey** ustawia klucz wstępny dla połączenia między bramą wirtualnej sieci prywatnej (VPN) a lokalną lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="03b00-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="03b00-107">Klucz musi być równy kluczowi skonfigurowanemu w bramie lokalnej sieci.</span><span class="sxs-lookup"><span data-stu-id="03b00-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="03b00-108">Jeśli te klucze nie pasują do siebie, połączenie nie może nawiązać połączenia.</span><span class="sxs-lookup"><span data-stu-id="03b00-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="03b00-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03b00-109">EXAMPLES</span></span>

## <span data-ttu-id="03b00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03b00-110">PARAMETERS</span></span>

### <span data-ttu-id="03b00-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="03b00-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="03b00-112">Określa nazwę lokacji sieci lokalnej łączącej się z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03b00-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="03b00-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="03b00-113">-Profile</span></span>
<span data-ttu-id="03b00-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b00-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="03b00-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="03b00-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03b00-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="03b00-116">-SharedKey</span></span>
<span data-ttu-id="03b00-117">Określa klucz udostępniony, który ma zostać przypisany do bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="03b00-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="03b00-118">Wartość musi być ciągiem numerycznym o wartości alfanumerycznej, który nie przekracza 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="03b00-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="03b00-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="03b00-119">-VNetName</span></span>
<span data-ttu-id="03b00-120">Określa sieć wirtualną, za pomocą której to polecenie cmdlet ustawia klucz udostępniony dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="03b00-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="03b00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b00-121">CommonParameters</span></span>
<span data-ttu-id="03b00-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b00-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b00-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b00-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03b00-124">INPUTS</span></span>

## <span data-ttu-id="03b00-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03b00-125">OUTPUTS</span></span>

## <span data-ttu-id="03b00-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03b00-126">NOTES</span></span>

## <span data-ttu-id="03b00-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03b00-127">RELATED LINKS</span></span>

[<span data-ttu-id="03b00-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="03b00-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


