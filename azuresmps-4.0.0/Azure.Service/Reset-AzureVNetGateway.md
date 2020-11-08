---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054431"
---
# <span data-ttu-id="cf0b8-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf0b8-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="cf0b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0b8-103">Resetuje wirtualną bramę sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="cf0b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf0b8-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf0b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf0b8-105">DESCRIPTION</span></span>
<span data-ttu-id="cf0b8-106">Polecenie cmdlet **Reset-AzureVNetGateway** resetuje i uruchamia ponownie bramę sieci wirtualnej wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="cf0b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf0b8-107">EXAMPLES</span></span>

### <span data-ttu-id="cf0b8-108">Przykład 1: Resetowanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cf0b8-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="cf0b8-109">To polecenie resetuje bramę sieci wirtualnej z sieci wirtualnej o nazwie ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="cf0b8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf0b8-110">PARAMETERS</span></span>

### <span data-ttu-id="cf0b8-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf0b8-111">-Profile</span></span>
<span data-ttu-id="cf0b8-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cf0b8-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf0b8-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="cf0b8-114">-VNetName</span></span>
<span data-ttu-id="cf0b8-115">Określa sieć wirtualną zawierającą bramę sieci wirtualnej, którą resetuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="cf0b8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0b8-116">CommonParameters</span></span>
<span data-ttu-id="cf0b8-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0b8-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0b8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0b8-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf0b8-119">INPUTS</span></span>

## <span data-ttu-id="cf0b8-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf0b8-120">OUTPUTS</span></span>

## <span data-ttu-id="cf0b8-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf0b8-121">NOTES</span></span>

## <span data-ttu-id="cf0b8-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf0b8-122">RELATED LINKS</span></span>

[<span data-ttu-id="cf0b8-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf0b8-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="cf0b8-124">Nowe — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf0b8-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="cf0b8-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf0b8-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="cf0b8-126">Zmienianie rozmiaru — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf0b8-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="cf0b8-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="cf0b8-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


