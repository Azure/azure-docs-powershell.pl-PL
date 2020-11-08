---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054451"
---
# <span data-ttu-id="2867d-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2867d-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2867d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2867d-102">SYNOPSIS</span></span>
<span data-ttu-id="2867d-103">Usuwa połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2867d-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="2867d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2867d-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2867d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2867d-105">DESCRIPTION</span></span>
<span data-ttu-id="2867d-106">Polecenie cmdlet **Remove-AzureVirtualNetworkGatewayConnection** usuwa połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2867d-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="2867d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2867d-107">EXAMPLES</span></span>

## <span data-ttu-id="2867d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2867d-108">PARAMETERS</span></span>

### <span data-ttu-id="2867d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="2867d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2867d-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="2867d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2867d-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2867d-111">-GatewayId</span></span>
<span data-ttu-id="2867d-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="2867d-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="2867d-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="2867d-113">-Profile</span></span>
<span data-ttu-id="2867d-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2867d-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2867d-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2867d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2867d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2867d-116">CommonParameters</span></span>
<span data-ttu-id="2867d-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2867d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2867d-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2867d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2867d-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2867d-119">INPUTS</span></span>

## <span data-ttu-id="2867d-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2867d-120">OUTPUTS</span></span>

## <span data-ttu-id="2867d-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2867d-121">NOTES</span></span>

## <span data-ttu-id="2867d-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2867d-122">RELATED LINKS</span></span>

[<span data-ttu-id="2867d-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2867d-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2867d-124">Nowe — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2867d-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2867d-125">Resetowanie — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2867d-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


