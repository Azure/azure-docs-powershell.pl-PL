---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055151"
---
# <span data-ttu-id="c1ce3-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1ce3-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c1ce3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ce3-103">Tworzy połączenie sieciowe bramy wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="c1ce3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1ce3-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c1ce3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ce3-106">Polecenie cmdlet **New-AzureVirtualNetworkGatewayConnection** tworzy połączenie sieciowe bramy wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="c1ce3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1ce3-107">EXAMPLES</span></span>

## <span data-ttu-id="c1ce3-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1ce3-108">PARAMETERS</span></span>

### <span data-ttu-id="c1ce3-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c1ce3-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c1ce3-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="c1ce3-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c1ce3-111">-EnableBgp</span></span>
<span data-ttu-id="c1ce3-112">Włącza protokół BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="c1ce3-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="c1ce3-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="c1ce3-113">-GatewayConnectionName</span></span>
<span data-ttu-id="c1ce3-114">Określa nazwę połączenia bramy.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="c1ce3-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="c1ce3-115">-GatewayConnectionType</span></span>
<span data-ttu-id="c1ce3-116">Określa typ połączenia bramy.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ce3-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="c1ce3-117">-Profile</span></span>
<span data-ttu-id="c1ce3-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c1ce3-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c1ce3-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="c1ce3-120">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ce3-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c1ce3-121">-SharedKey</span></span>
<span data-ttu-id="c1ce3-122">Określa klucz współużytkowany.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="c1ce3-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="c1ce3-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="c1ce3-124">Określa identyfikator bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="c1ce3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ce3-125">CommonParameters</span></span>
<span data-ttu-id="c1ce3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ce3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ce3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ce3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ce3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1ce3-128">INPUTS</span></span>

## <span data-ttu-id="c1ce3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1ce3-129">OUTPUTS</span></span>

## <span data-ttu-id="c1ce3-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1ce3-130">NOTES</span></span>

## <span data-ttu-id="c1ce3-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1ce3-131">RELATED LINKS</span></span>

[<span data-ttu-id="c1ce3-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1ce3-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c1ce3-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1ce3-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c1ce3-134">Resetowanie — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1ce3-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


