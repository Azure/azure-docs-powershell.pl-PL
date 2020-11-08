---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055241"
---
# <span data-ttu-id="85624-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="85624-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="85624-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85624-102">SYNOPSIS</span></span>
<span data-ttu-id="85624-103">Pobiera wstępnie udostępniony klucz dla połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="85624-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="85624-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85624-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="85624-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85624-105">DESCRIPTION</span></span>
<span data-ttu-id="85624-106">Polecenie cmdlet **Get-AzureVNetGatewayKey** pobiera wstępnie udostępniony klucz dla połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="85624-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="85624-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85624-107">EXAMPLES</span></span>

## <span data-ttu-id="85624-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85624-108">PARAMETERS</span></span>

### <span data-ttu-id="85624-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="85624-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="85624-110">Określa nazwę lokacji sieci lokalnej łączącej się z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="85624-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="85624-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="85624-111">-Profile</span></span>
<span data-ttu-id="85624-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85624-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="85624-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="85624-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85624-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="85624-114">-VNetName</span></span>
<span data-ttu-id="85624-115">Określa sieć wirtualną, za pomocą której to polecenie cmdlet pobiera klucz udostępniony dla połączeń.</span><span class="sxs-lookup"><span data-stu-id="85624-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="85624-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85624-116">CommonParameters</span></span>
<span data-ttu-id="85624-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85624-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85624-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85624-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85624-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85624-119">INPUTS</span></span>

## <span data-ttu-id="85624-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85624-120">OUTPUTS</span></span>

## <span data-ttu-id="85624-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85624-121">NOTES</span></span>

## <span data-ttu-id="85624-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85624-122">RELATED LINKS</span></span>

[<span data-ttu-id="85624-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="85624-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


