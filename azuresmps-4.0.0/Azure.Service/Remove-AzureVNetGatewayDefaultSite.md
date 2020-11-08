---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054455"
---
# <span data-ttu-id="2ea24-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2ea24-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="2ea24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ea24-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea24-103">Usuwa trasę domyślną dla ruchu wymuszonego tunelowania.</span><span class="sxs-lookup"><span data-stu-id="2ea24-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="2ea24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ea24-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ea24-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ea24-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea24-106">Polecenie cmdlet **Remove-AzureVNetGatewayDefaultSite** usuwa trasę domyślną do witryny lokalnej w celu wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="2ea24-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="2ea24-107">To polecenie cmdlet powoduje usunięcie trasy z bramy wirtualnej sieci prywatnej (VPN) platformy Azure dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ea24-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="2ea24-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ea24-108">EXAMPLES</span></span>

### <span data-ttu-id="2ea24-109">Przykład 1. Usuwanie trasy do witryny domyślnej</span><span class="sxs-lookup"><span data-stu-id="2ea24-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="2ea24-110">To polecenie powoduje usunięcie trasy do witryny domyślnej z sieci VPN w sieci wirtualnej o nazwie ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="2ea24-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="2ea24-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ea24-111">PARAMETERS</span></span>

### <span data-ttu-id="2ea24-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ea24-112">-Profile</span></span>
<span data-ttu-id="2ea24-113">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ea24-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ea24-114">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ea24-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ea24-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2ea24-115">-VNetName</span></span>
<span data-ttu-id="2ea24-116">Określa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2ea24-116">Specifies a virtual network.</span></span>
<span data-ttu-id="2ea24-117">To polecenie cmdlet umożliwia usunięcie trasy domyślnej z bramy sieci VPN dla sieci wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2ea24-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ea24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea24-118">CommonParameters</span></span>
<span data-ttu-id="2ea24-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea24-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea24-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea24-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ea24-121">INPUTS</span></span>

## <span data-ttu-id="2ea24-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ea24-122">OUTPUTS</span></span>

## <span data-ttu-id="2ea24-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ea24-123">NOTES</span></span>

## <span data-ttu-id="2ea24-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ea24-124">RELATED LINKS</span></span>

[<span data-ttu-id="2ea24-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2ea24-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
