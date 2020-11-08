---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054403"
---
# <span data-ttu-id="9d322-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9d322-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="9d322-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d322-102">SYNOPSIS</span></span>
<span data-ttu-id="9d322-103">Ustawia klucz bramy sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d322-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9d322-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d322-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d322-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d322-105">DESCRIPTION</span></span>
<span data-ttu-id="9d322-106">Polecenie cmdlet **Set-AzureVirtualNetworkGatewayKey** ustawia klucz bramy wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="9d322-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="9d322-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d322-107">EXAMPLES</span></span>

## <span data-ttu-id="9d322-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d322-108">PARAMETERS</span></span>

### <span data-ttu-id="9d322-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="9d322-109">-ConnectedEntityId</span></span>
<span data-ttu-id="9d322-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="9d322-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="9d322-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9d322-111">-GatewayId</span></span>
<span data-ttu-id="9d322-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="9d322-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="9d322-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="9d322-113">-Profile</span></span>
<span data-ttu-id="9d322-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d322-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9d322-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9d322-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d322-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9d322-116">-SharedKey</span></span>
<span data-ttu-id="9d322-117">Określa klucz współużytkowany.</span><span class="sxs-lookup"><span data-stu-id="9d322-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="9d322-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d322-118">CommonParameters</span></span>
<span data-ttu-id="9d322-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d322-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d322-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d322-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d322-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d322-121">INPUTS</span></span>

## <span data-ttu-id="9d322-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d322-122">OUTPUTS</span></span>

## <span data-ttu-id="9d322-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d322-123">NOTES</span></span>

## <span data-ttu-id="9d322-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d322-124">RELATED LINKS</span></span>

[<span data-ttu-id="9d322-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9d322-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="9d322-126">Resetowanie — AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9d322-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


