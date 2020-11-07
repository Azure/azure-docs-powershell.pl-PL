---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892725"
---
# <span data-ttu-id="e8c3b-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e8c3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c3b-103">Konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e8c3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8c3b-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8c3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c3b-106">Polecenie cmdlet **Set-AzVirtualNetworkGatewayConnection** konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e8c3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c3b-108">1:1</span><span class="sxs-lookup"><span data-stu-id="e8c3b-108">1:</span></span>
```

```

## <span data-ttu-id="e8c3b-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8c3b-109">PARAMETERS</span></span>

### <span data-ttu-id="e8c3b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8c3b-110">-AsJob</span></span>
<span data-ttu-id="e8c3b-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e8c3b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8c3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c3b-112">-DefaultProfile</span></span>
<span data-ttu-id="e8c3b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8c3b-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e8c3b-114">-EnableBgp</span></span>
<span data-ttu-id="e8c3b-115">Czy sesja BGP ma być używana w tunelu VPN S2S</span><span class="sxs-lookup"><span data-stu-id="e8c3b-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="e8c3b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e8c3b-116">-Force</span></span>
<span data-ttu-id="e8c3b-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8c3b-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="e8c3b-118">-IpsecPolicies</span></span>
<span data-ttu-id="e8c3b-119">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="e8c3b-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e8c3b-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e8c3b-121">Czy używać selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="e8c3b-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="e8c3b-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e8c3b-123">Określa obiekt PSVirtualNetworkGatewayConnection, którego używa polecenie cmdlet do modyfikowania połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e8c3b-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8c3b-124">-Confirm</span></span>
<span data-ttu-id="e8c3b-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c3b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c3b-126">-WhatIf</span></span>
<span data-ttu-id="e8c3b-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c3b-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c3b-129">CommonParameters</span></span>
<span data-ttu-id="e8c3b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c3b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c3b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c3b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8c3b-132">INPUTS</span></span>

### <span data-ttu-id="e8c3b-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e8c3b-134">Parametr "VirtualNetworkGatewayConnection" akceptuje wartość typu "PSVirtualNetworkGatewayConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e8c3b-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="e8c3b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="e8c3b-136">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e8c3b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8c3b-137">NOTES</span></span>

## <span data-ttu-id="e8c3b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8c3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e8c3b-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e8c3b-140">Nowe — AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e8c3b-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e8c3b-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


