---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055153"
---
# <span data-ttu-id="f60e9-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f60e9-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="f60e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f60e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f60e9-103">Tworzy bramę sieci VPN w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f60e9-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="f60e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f60e9-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f60e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f60e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f60e9-106">Polecenie cmdlet **New-AzureVNetGateway** tworzy bramę wirtualnej sieci prywatnej (VPN) w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f60e9-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="f60e9-107">Możesz również określić jednostkę SKU bramy (wartość domyślna, standardowa lub HighPerformance).</span><span class="sxs-lookup"><span data-stu-id="f60e9-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="f60e9-108">Możesz określić typ: StaticRouting lub DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="f60e9-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="f60e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f60e9-109">EXAMPLES</span></span>

### <span data-ttu-id="f60e9-110">Przykład 1: Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f60e9-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="f60e9-111">To polecenie tworzy wirtualną bramę sieciową dla sieci wirtualnej o nazwie ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="f60e9-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="f60e9-112">Brama to domyślna wersja jednostki SKU i korzysta z routingu dynamicznego.</span><span class="sxs-lookup"><span data-stu-id="f60e9-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="f60e9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f60e9-113">PARAMETERS</span></span>

### <span data-ttu-id="f60e9-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="f60e9-114">-GatewaySKU</span></span>
<span data-ttu-id="f60e9-115">Określa jednostkę SKU bramy sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e9-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="f60e9-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f60e9-116">Valid values are:</span></span> 

- <span data-ttu-id="f60e9-117">Domyślne</span><span class="sxs-lookup"><span data-stu-id="f60e9-117">Default</span></span> 
- <span data-ttu-id="f60e9-118">Standard</span><span class="sxs-lookup"><span data-stu-id="f60e9-118">Standard</span></span> 
- <span data-ttu-id="f60e9-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="f60e9-119">HighPerformance</span></span>

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

### <span data-ttu-id="f60e9-120">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="f60e9-120">-GatewayType</span></span>
<span data-ttu-id="f60e9-121">Określa typ bramy tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e9-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="f60e9-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f60e9-122">Valid values are:</span></span> 

- <span data-ttu-id="f60e9-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="f60e9-123">StaticRouting</span></span> 
- <span data-ttu-id="f60e9-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="f60e9-124">DynamicRouting</span></span>

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

### <span data-ttu-id="f60e9-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="f60e9-125">-Profile</span></span>
<span data-ttu-id="f60e9-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e9-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f60e9-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f60e9-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f60e9-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f60e9-128">-VNetName</span></span>
<span data-ttu-id="f60e9-129">Określa sieć wirtualną, w której to polecenie cmdlet umożliwia dodanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f60e9-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="f60e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60e9-130">CommonParameters</span></span>
<span data-ttu-id="f60e9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60e9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60e9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60e9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f60e9-133">INPUTS</span></span>

## <span data-ttu-id="f60e9-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f60e9-134">OUTPUTS</span></span>

## <span data-ttu-id="f60e9-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f60e9-135">NOTES</span></span>

## <span data-ttu-id="f60e9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f60e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="f60e9-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f60e9-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="f60e9-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f60e9-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="f60e9-139">Resetowanie — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f60e9-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="f60e9-140">Zmienianie rozmiaru — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f60e9-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="f60e9-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f60e9-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


