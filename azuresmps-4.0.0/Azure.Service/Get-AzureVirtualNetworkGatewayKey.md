---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055479"
---
# <span data-ttu-id="40de8-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="40de8-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="40de8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40de8-102">SYNOPSIS</span></span>
<span data-ttu-id="40de8-103">Pobiera klucz bramy wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="40de8-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="40de8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40de8-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="40de8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40de8-105">DESCRIPTION</span></span>
<span data-ttu-id="40de8-106">Polecenie cmdlet **Get-AzureVirtualNetworkGatewayKey** Pobiera klucz bramy wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="40de8-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="40de8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40de8-107">EXAMPLES</span></span>

## <span data-ttu-id="40de8-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40de8-108">PARAMETERS</span></span>

### <span data-ttu-id="40de8-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="40de8-109">-ConnectedEntityId</span></span>
<span data-ttu-id="40de8-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="40de8-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="40de8-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="40de8-111">-GatewayId</span></span>
<span data-ttu-id="40de8-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="40de8-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="40de8-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="40de8-113">-Profile</span></span>
<span data-ttu-id="40de8-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40de8-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="40de8-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="40de8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40de8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40de8-116">CommonParameters</span></span>
<span data-ttu-id="40de8-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40de8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40de8-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40de8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40de8-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40de8-119">INPUTS</span></span>

## <span data-ttu-id="40de8-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40de8-120">OUTPUTS</span></span>

## <span data-ttu-id="40de8-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40de8-121">NOTES</span></span>

## <span data-ttu-id="40de8-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40de8-122">RELATED LINKS</span></span>

[<span data-ttu-id="40de8-123">Resetowanie — AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="40de8-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="40de8-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="40de8-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


