---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552640"
---
# <span data-ttu-id="33742-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="33742-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33742-102">SYNOPSIS</span></span>
<span data-ttu-id="33742-103">Resetuje bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="33742-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33742-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33742-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33742-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33742-105">DESCRIPTION</span></span>
<span data-ttu-id="33742-106">Resetuje bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="33742-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="33742-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33742-107">EXAMPLES</span></span>

### <span data-ttu-id="33742-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="33742-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="33742-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33742-109">PARAMETERS</span></span>

### <span data-ttu-id="33742-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33742-110">-AsJob</span></span>
<span data-ttu-id="33742-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="33742-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33742-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33742-112">-DefaultProfile</span></span>
<span data-ttu-id="33742-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33742-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33742-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="33742-114">-GatewayVip</span></span>
<span data-ttu-id="33742-115">Adres VIP bramy w celu zresetowania określonego wystąpienia bramy (na przykład w przypadku bram Active-Active z obsługą funkcji). Domyślnie wystąpienie główne bramy zostanie zresetowane, jeśli nie zostanie przekazana żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="33742-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33742-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33742-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33742-117">CommonParameters</span></span>
<span data-ttu-id="33742-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33742-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33742-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33742-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33742-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33742-120">INPUTS</span></span>

### <span data-ttu-id="33742-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="33742-122">Parametry: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33742-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="33742-123">System. String</span><span class="sxs-lookup"><span data-stu-id="33742-123">System.String</span></span>
<span data-ttu-id="33742-124">Parametry: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33742-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="33742-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33742-125">OUTPUTS</span></span>

### <span data-ttu-id="33742-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="33742-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33742-127">NOTES</span></span>

## <span data-ttu-id="33742-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33742-128">RELATED LINKS</span></span>

[<span data-ttu-id="33742-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="33742-130">Nowe — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="33742-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="33742-132">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="33742-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33742-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


