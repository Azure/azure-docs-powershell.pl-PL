---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543187"
---
# <span data-ttu-id="3c471-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3c471-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c471-102">SYNOPSIS</span></span>
<span data-ttu-id="3c471-103">Konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3c471-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c471-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c471-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c471-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c471-105">DESCRIPTION</span></span>
<span data-ttu-id="3c471-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnection** konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3c471-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="3c471-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c471-107">EXAMPLES</span></span>

## <span data-ttu-id="3c471-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c471-108">PARAMETERS</span></span>

### <span data-ttu-id="3c471-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3c471-109">-EnableBgp</span></span>
<span data-ttu-id="3c471-110">Czy sesja BGP ma być używana w tunelu VPN S2S</span><span class="sxs-lookup"><span data-stu-id="3c471-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3c471-111">-Force</span></span>
<span data-ttu-id="3c471-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c471-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="3c471-113">-IpsecPolicies</span></span>
<span data-ttu-id="3c471-114">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="3c471-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="3c471-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="3c471-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="3c471-116">Czy używać selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="3c471-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="3c471-118">Określa obiekt PSVirtualNetworkGatewayConnection, którego używa polecenie cmdlet do modyfikowania połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3c471-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c471-119">-Confirm</span></span>
<span data-ttu-id="3c471-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c471-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c471-121">-WhatIf</span></span>
<span data-ttu-id="3c471-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c471-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c471-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c471-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c471-124">-DefaultProfile</span></span>
<span data-ttu-id="3c471-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c471-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c471-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c471-126">CommonParameters</span></span>
<span data-ttu-id="3c471-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c471-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c471-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c471-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c471-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c471-129">INPUTS</span></span>

### <span data-ttu-id="3c471-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="3c471-131">Parametr "VirtualNetworkGatewayConnection" akceptuje wartość typu "PSVirtualNetworkGatewayConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3c471-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="3c471-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c471-132">OUTPUTS</span></span>

### <span data-ttu-id="3c471-133">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3c471-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c471-134">NOTES</span></span>

## <span data-ttu-id="3c471-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c471-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c471-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3c471-137">Nowe — AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3c471-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3c471-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


