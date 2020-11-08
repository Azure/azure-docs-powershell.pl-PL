---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055380"
---
# <span data-ttu-id="4d0a5-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="4d0a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0a5-103">Włącza lub wyłącza bramę sieci VPN dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="4d0a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d0a5-104">SYNTAX</span></span>

### <span data-ttu-id="4d0a5-105">Connect (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4d0a5-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d0a5-106">Zamyka</span><span class="sxs-lookup"><span data-stu-id="4d0a5-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4d0a5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d0a5-107">DESCRIPTION</span></span>
<span data-ttu-id="4d0a5-108">Polecenie cmdlet **Set-AzureVNetGateway** włącza lub wyłącza bramę wirtualnej sieci prywatnej (VPN) dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="4d0a5-109">Brama sieci wirtualnej to punkt końcowy sieci VPN umożliwiający połączenie z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="4d0a5-110">Określ parametr *Connect* lub *Disconnect* , aby włączyć lub wyłączyć połączenie VPN między lokalną lokacją sieci lokalnej a siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="4d0a5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d0a5-111">EXAMPLES</span></span>

### <span data-ttu-id="4d0a5-112">Przykład 1: Włączanie bramy sieci wirtualnej dla sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4d0a5-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="4d0a5-113">To polecenie włącza bramę sieci wirtualnej między wirtualną siecią Azure o nazwie ContosoProdNet a urządzeniem sieci VPN dla lokalnej lokacji sieciowej o nazwie ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="4d0a5-114">Przykład 2: wyłączenie bramy sieci wirtualnej dla sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4d0a5-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="4d0a5-115">To polecenie wyłącza bramę sieci wirtualnej między wirtualną siecią Azure o nazwie ContosoProdNet a urządzeniem sieci VPN dla lokalnej lokacji sieciowej o nazwie ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="4d0a5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d0a5-116">PARAMETERS</span></span>

### <span data-ttu-id="4d0a5-117">-Connect</span><span class="sxs-lookup"><span data-stu-id="4d0a5-117">-Connect</span></span>
<span data-ttu-id="4d0a5-118">Wskazuje, że to polecenie cmdlet włącza połączenie VPN między siecią wirtualną a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d0a5-119">-Disconnect</span><span class="sxs-lookup"><span data-stu-id="4d0a5-119">-Disconnect</span></span>
<span data-ttu-id="4d0a5-120">Wskazuje, że to polecenie cmdlet wyłącza połączenie VPN między siecią wirtualną a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d0a5-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="4d0a5-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="4d0a5-122">Określa nazwę lokalnej lokacji sieciowej, dla której to polecenie cmdlet włączy lub wyłącza połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="4d0a5-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="4d0a5-123">-Profile</span></span>
<span data-ttu-id="4d0a5-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4d0a5-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d0a5-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4d0a5-126">-VNetName</span></span>
<span data-ttu-id="4d0a5-127">Określa sieć wirtualną, w której to polecenie cmdlet włącza lub wyłącza połączenie VPN.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="4d0a5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0a5-128">CommonParameters</span></span>
<span data-ttu-id="4d0a5-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0a5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0a5-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d0a5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0a5-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d0a5-131">INPUTS</span></span>

## <span data-ttu-id="4d0a5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d0a5-132">OUTPUTS</span></span>

## <span data-ttu-id="4d0a5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d0a5-133">NOTES</span></span>

## <span data-ttu-id="4d0a5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d0a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d0a5-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="4d0a5-136">Nowe — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="4d0a5-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="4d0a5-138">Resetowanie — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="4d0a5-139">Zmienianie rozmiaru — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4d0a5-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


