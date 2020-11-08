---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054456"
---
# <span data-ttu-id="6bdb1-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="6bdb1-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="6bdb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bdb1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdb1-103">Usuwa bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="6bdb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bdb1-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6bdb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bdb1-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdb1-106">Polecenie cmdlet **Remove-AzureVNetGateway** Usuwa istniejącą bramę wirtualnej sieci prywatnej (VPN) dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="6bdb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bdb1-107">EXAMPLES</span></span>

### <span data-ttu-id="6bdb1-108">Przykład 1: usunięcie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6bdb1-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="6bdb1-109">To polecenie powoduje usunięcie bramy sieci wirtualnej z sieci wirtualnej o nazwie ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="6bdb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bdb1-110">PARAMETERS</span></span>

### <span data-ttu-id="6bdb1-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="6bdb1-111">-Profile</span></span>
<span data-ttu-id="6bdb1-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6bdb1-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bdb1-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="6bdb1-114">-VNetName</span></span>
<span data-ttu-id="6bdb1-115">Określa sieć wirtualną, w której to polecenie cmdlet usuwa bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="6bdb1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdb1-116">CommonParameters</span></span>
<span data-ttu-id="6bdb1-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bdb1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdb1-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bdb1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdb1-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bdb1-119">INPUTS</span></span>

## <span data-ttu-id="6bdb1-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bdb1-120">OUTPUTS</span></span>

## <span data-ttu-id="6bdb1-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bdb1-121">NOTES</span></span>

## <span data-ttu-id="6bdb1-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bdb1-122">RELATED LINKS</span></span>

[<span data-ttu-id="6bdb1-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="6bdb1-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="6bdb1-124">Nowe — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="6bdb1-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="6bdb1-125">Resetowanie — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="6bdb1-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="6bdb1-126">Zmienianie rozmiaru — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="6bdb1-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="6bdb1-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="6bdb1-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


