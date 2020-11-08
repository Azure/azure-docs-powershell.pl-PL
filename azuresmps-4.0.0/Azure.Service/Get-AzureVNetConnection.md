---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055253"
---
# <span data-ttu-id="c65cb-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="c65cb-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="c65cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c65cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c65cb-103">Pobiera połączenia z siecią wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c65cb-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="c65cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c65cb-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c65cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c65cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c65cb-106">Polecenie cmdlet **Get-AzureVNetConnection** zwraca obiekt, który określa wszystkie aktywne połączenia wirtualnej sieci prywatnej (VPN) z siecią wirtualną Azure.</span><span class="sxs-lookup"><span data-stu-id="c65cb-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="c65cb-107">Połączenia sieci VPN obejmują sieci VPN międzylokacyjnych połączeń międzylokacyjnych i sieć wirtualną z wirtualnymi połączeniami sieciowymi.</span><span class="sxs-lookup"><span data-stu-id="c65cb-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="c65cb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c65cb-108">EXAMPLES</span></span>

## <span data-ttu-id="c65cb-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c65cb-109">PARAMETERS</span></span>

### <span data-ttu-id="c65cb-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="c65cb-110">-Profile</span></span>
<span data-ttu-id="c65cb-111">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65cb-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c65cb-112">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c65cb-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c65cb-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c65cb-113">-VNetName</span></span>
<span data-ttu-id="c65cb-114">Określa nazwę sieci wirtualnej, z której to polecenie cmdlet zwraca połączenia.</span><span class="sxs-lookup"><span data-stu-id="c65cb-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="c65cb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65cb-115">CommonParameters</span></span>
<span data-ttu-id="c65cb-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65cb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65cb-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65cb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65cb-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c65cb-118">INPUTS</span></span>

## <span data-ttu-id="c65cb-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c65cb-119">OUTPUTS</span></span>

## <span data-ttu-id="c65cb-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c65cb-120">NOTES</span></span>

## <span data-ttu-id="c65cb-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c65cb-121">RELATED LINKS</span></span>

