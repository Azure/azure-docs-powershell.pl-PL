---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055055"
---
# <span data-ttu-id="7812d-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7812d-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7812d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7812d-102">SYNOPSIS</span></span>
<span data-ttu-id="7812d-103">Resetuje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7812d-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7812d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7812d-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7812d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7812d-105">DESCRIPTION</span></span>
<span data-ttu-id="7812d-106">Polecenie cmdlet **Reset-AzureVirtualNetworkGatewayConnection** resetuje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7812d-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7812d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7812d-107">EXAMPLES</span></span>

## <span data-ttu-id="7812d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7812d-108">PARAMETERS</span></span>

### <span data-ttu-id="7812d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="7812d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="7812d-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="7812d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="7812d-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7812d-111">-EnableBgp</span></span>
<span data-ttu-id="7812d-112">Włącza protokół BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="7812d-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7812d-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7812d-113">-GatewayId</span></span>
<span data-ttu-id="7812d-114">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="7812d-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7812d-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="7812d-115">-Profile</span></span>
<span data-ttu-id="7812d-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7812d-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7812d-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7812d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7812d-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7812d-118">-RoutingWeight</span></span>
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

### <span data-ttu-id="7812d-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7812d-119">-SharedKey</span></span>
<span data-ttu-id="7812d-120">Określa klucz współużytkowany.</span><span class="sxs-lookup"><span data-stu-id="7812d-120">Specifies a shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7812d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7812d-121">CommonParameters</span></span>
<span data-ttu-id="7812d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7812d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7812d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7812d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7812d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7812d-124">INPUTS</span></span>

## <span data-ttu-id="7812d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7812d-125">OUTPUTS</span></span>

## <span data-ttu-id="7812d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7812d-126">NOTES</span></span>

## <span data-ttu-id="7812d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7812d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7812d-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7812d-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7812d-129">Nowe — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7812d-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7812d-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7812d-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


