---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055379"
---
# <span data-ttu-id="45397-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45397-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="45397-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45397-102">SYNOPSIS</span></span>
<span data-ttu-id="45397-103">Ustawia domyślną witrynę dla ruchu tunelowania wymuszonego.</span><span class="sxs-lookup"><span data-stu-id="45397-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="45397-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45397-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="45397-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45397-105">DESCRIPTION</span></span>
<span data-ttu-id="45397-106">Polecenie cmdlet **Set-AzureVNetGatewayDefaultSite** ustawia domyślną trasę do lokalnej witryny w celu wymuszenia ruchu tunelowania.</span><span class="sxs-lookup"><span data-stu-id="45397-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="45397-107">To polecenie ustawia trasę w bramie wirtualnej sieci prywatnej (VPN) platformy Azure dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45397-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="45397-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45397-108">EXAMPLES</span></span>

## <span data-ttu-id="45397-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45397-109">PARAMETERS</span></span>

### <span data-ttu-id="45397-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="45397-110">-DefaultSite</span></span>
<span data-ttu-id="45397-111">Określa nazwę lokalnej lokalnej sieci dla ruchu tunelowania wymuszonego.</span><span class="sxs-lookup"><span data-stu-id="45397-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="45397-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="45397-112">-Profile</span></span>
<span data-ttu-id="45397-113">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45397-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45397-114">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="45397-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45397-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="45397-115">-VNetName</span></span>
<span data-ttu-id="45397-116">Określa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="45397-116">Specifies a virtual network.</span></span>
<span data-ttu-id="45397-117">To polecenie cmdlet ustawia domyślną trasę bramy VPN dla ruchu wymuszonego tunelowania dla sieci wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="45397-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="45397-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45397-118">CommonParameters</span></span>
<span data-ttu-id="45397-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45397-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45397-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45397-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45397-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45397-121">INPUTS</span></span>

## <span data-ttu-id="45397-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45397-122">OUTPUTS</span></span>

## <span data-ttu-id="45397-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45397-123">NOTES</span></span>

## <span data-ttu-id="45397-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45397-124">RELATED LINKS</span></span>

[<span data-ttu-id="45397-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45397-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
