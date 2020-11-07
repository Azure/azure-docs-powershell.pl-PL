---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 59f4a96c324a9743c876cf987e1347bbe0c8d946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709046"
---
# <span data-ttu-id="24765-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="24765-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24765-102">SYNOPSIS</span></span>
<span data-ttu-id="24765-103">Resetuje bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="24765-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="24765-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24765-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24765-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24765-105">DESCRIPTION</span></span>
<span data-ttu-id="24765-106">Resetuje bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="24765-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="24765-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24765-107">EXAMPLES</span></span>

### <span data-ttu-id="24765-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="24765-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="24765-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24765-109">PARAMETERS</span></span>

### <span data-ttu-id="24765-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24765-110">-AsJob</span></span>
<span data-ttu-id="24765-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24765-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24765-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24765-112">-DefaultProfile</span></span>
<span data-ttu-id="24765-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24765-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24765-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="24765-114">-GatewayVip</span></span>
<span data-ttu-id="24765-115">Adres VIP bramy w celu zresetowania określonego wystąpienia bramy (na przykład w przypadku bram Active-Active z obsługą funkcji). Domyślnie wystąpienie główne bramy zostanie zresetowane, jeśli nie zostanie przekazana żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="24765-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="24765-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="24765-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24765-117">CommonParameters</span></span>
<span data-ttu-id="24765-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24765-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24765-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24765-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24765-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24765-120">INPUTS</span></span>

### <span data-ttu-id="24765-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="24765-122">System. String</span><span class="sxs-lookup"><span data-stu-id="24765-122">System.String</span></span>

## <span data-ttu-id="24765-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24765-123">OUTPUTS</span></span>

### <span data-ttu-id="24765-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="24765-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24765-125">NOTES</span></span>

## <span data-ttu-id="24765-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24765-126">RELATED LINKS</span></span>

[<span data-ttu-id="24765-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="24765-128">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="24765-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="24765-130">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="24765-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="24765-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
