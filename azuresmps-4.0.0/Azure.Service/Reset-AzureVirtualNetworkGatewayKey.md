---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055054"
---
# <span data-ttu-id="314f1-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="314f1-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="314f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="314f1-102">SYNOPSIS</span></span>
<span data-ttu-id="314f1-103">Resetowanie klucza bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="314f1-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="314f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="314f1-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="314f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="314f1-105">DESCRIPTION</span></span>
<span data-ttu-id="314f1-106">Polecenie cmdlet **Reset-AzureVirtualNetworkGatewayKey** resetuje klucz bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="314f1-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="314f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="314f1-107">EXAMPLES</span></span>

## <span data-ttu-id="314f1-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="314f1-108">PARAMETERS</span></span>

### <span data-ttu-id="314f1-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="314f1-109">-ConnectedEntityId</span></span>
<span data-ttu-id="314f1-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="314f1-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="314f1-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="314f1-111">-GatewayId</span></span>
<span data-ttu-id="314f1-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="314f1-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="314f1-113">-Length</span><span class="sxs-lookup"><span data-stu-id="314f1-113">-keyLength</span></span>
<span data-ttu-id="314f1-114">Określa długość klucza.</span><span class="sxs-lookup"><span data-stu-id="314f1-114">Specifies the key length.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314f1-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="314f1-115">-Profile</span></span>
<span data-ttu-id="314f1-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="314f1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="314f1-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="314f1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="314f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314f1-118">CommonParameters</span></span>
<span data-ttu-id="314f1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314f1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314f1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="314f1-121">INPUTS</span></span>

## <span data-ttu-id="314f1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="314f1-122">OUTPUTS</span></span>

## <span data-ttu-id="314f1-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="314f1-123">NOTES</span></span>

## <span data-ttu-id="314f1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="314f1-124">RELATED LINKS</span></span>

[<span data-ttu-id="314f1-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="314f1-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="314f1-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="314f1-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
