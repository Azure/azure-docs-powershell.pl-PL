---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898882"
---
# <span data-ttu-id="87124-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="87124-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87124-102">SYNOPSIS</span></span>
<span data-ttu-id="87124-103">Konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87124-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87124-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87124-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87124-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87124-105">DESCRIPTION</span></span>
<span data-ttu-id="87124-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnection** konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87124-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="87124-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87124-107">EXAMPLES</span></span>

### <span data-ttu-id="87124-108">1:1</span><span class="sxs-lookup"><span data-stu-id="87124-108">1:</span></span>
```

```

## <span data-ttu-id="87124-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87124-109">PARAMETERS</span></span>

### <span data-ttu-id="87124-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87124-110">-AsJob</span></span>
<span data-ttu-id="87124-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="87124-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87124-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87124-112">-DefaultProfile</span></span>
<span data-ttu-id="87124-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87124-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87124-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="87124-114">-EnableBgp</span></span>
<span data-ttu-id="87124-115">Czy sesja BGP ma być używana w tunelu VPN S2S</span><span class="sxs-lookup"><span data-stu-id="87124-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87124-116">-Force</span><span class="sxs-lookup"><span data-stu-id="87124-116">-Force</span></span>
<span data-ttu-id="87124-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87124-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87124-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="87124-118">-IpsecPolicies</span></span>
<span data-ttu-id="87124-119">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="87124-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87124-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="87124-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="87124-121">Czy używać selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="87124-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="87124-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="87124-123">Określa obiekt PSVirtualNetworkGatewayConnection, którego używa polecenie cmdlet do modyfikowania połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87124-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87124-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87124-124">-Confirm</span></span>
<span data-ttu-id="87124-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87124-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87124-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87124-126">-WhatIf</span></span>
<span data-ttu-id="87124-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87124-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87124-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87124-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87124-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87124-129">CommonParameters</span></span>
<span data-ttu-id="87124-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87124-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87124-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87124-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87124-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87124-132">INPUTS</span></span>

### <span data-ttu-id="87124-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="87124-134">Parametr "VirtualNetworkGatewayConnection" akceptuje wartość typu "PSVirtualNetworkGatewayConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="87124-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="87124-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87124-135">OUTPUTS</span></span>

### <span data-ttu-id="87124-136">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="87124-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87124-137">NOTES</span></span>

## <span data-ttu-id="87124-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87124-138">RELATED LINKS</span></span>

[<span data-ttu-id="87124-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="87124-140">Nowe — AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="87124-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="87124-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


