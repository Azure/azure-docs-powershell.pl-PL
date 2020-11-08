---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055053"
---
# <span data-ttu-id="01af2-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="01af2-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="01af2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01af2-102">SYNOPSIS</span></span>
<span data-ttu-id="01af2-103">Zmienia rozmiar bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="01af2-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="01af2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01af2-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="01af2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01af2-105">DESCRIPTION</span></span>
<span data-ttu-id="01af2-106">Polecenie cmdlet size **-AzureVNetGateway** powoduje zmianę rozmiaru bramy wirtualnej sieci prywatnej (VPN) do innej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="01af2-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="01af2-107">Prawidłowe jednostki SKU dla bramy sieci wirtualnej są domyślne, standardowe i HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="01af2-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="01af2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01af2-108">EXAMPLES</span></span>

### <span data-ttu-id="01af2-109">Przykład 1. Zmienianie jednostki SKU dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="01af2-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="01af2-110">To polecenie powoduje zmianę jednostki SKU bramy sieci wirtualnej dla sieci wirtualnej o nazwie ContosoVN07 na HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="01af2-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="01af2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01af2-111">PARAMETERS</span></span>

### <span data-ttu-id="01af2-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="01af2-112">-GatewaySKU</span></span>
<span data-ttu-id="01af2-113">Określa jednostkę SKU, do której to polecenie cmdlet zmienia rozmiar bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01af2-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="01af2-114">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="01af2-114">Valid values are:</span></span> 

- <span data-ttu-id="01af2-115">Domyślne</span><span class="sxs-lookup"><span data-stu-id="01af2-115">Default</span></span> 
- <span data-ttu-id="01af2-116">Standard</span><span class="sxs-lookup"><span data-stu-id="01af2-116">Standard</span></span> 
- <span data-ttu-id="01af2-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="01af2-117">HighPerformance</span></span>

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

### <span data-ttu-id="01af2-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="01af2-118">-Profile</span></span>
<span data-ttu-id="01af2-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01af2-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="01af2-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="01af2-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01af2-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="01af2-121">-VNetName</span></span>
<span data-ttu-id="01af2-122">Określa sieć wirtualną, w której to polecenie cmdlet zmienia rozmiar bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01af2-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="01af2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01af2-123">CommonParameters</span></span>
<span data-ttu-id="01af2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01af2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01af2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01af2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01af2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01af2-126">INPUTS</span></span>

## <span data-ttu-id="01af2-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01af2-127">OUTPUTS</span></span>

## <span data-ttu-id="01af2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01af2-128">NOTES</span></span>

## <span data-ttu-id="01af2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01af2-129">RELATED LINKS</span></span>

[<span data-ttu-id="01af2-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="01af2-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="01af2-131">Nowe — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="01af2-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="01af2-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="01af2-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="01af2-133">Resetowanie — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="01af2-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="01af2-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="01af2-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


