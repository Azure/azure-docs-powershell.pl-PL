---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718894"
---
# <span data-ttu-id="42448-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="42448-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42448-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42448-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42448-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42448-104">Opis</span><span class="sxs-lookup"><span data-stu-id="42448-104">DESCRIPTION</span></span>

## <span data-ttu-id="42448-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42448-105">EXAMPLES</span></span>

## <span data-ttu-id="42448-106">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42448-106">PARAMETERS</span></span>

### <span data-ttu-id="42448-107">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42448-107">-AsJob</span></span>
<span data-ttu-id="42448-108">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="42448-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42448-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42448-109">-DefaultProfile</span></span>
<span data-ttu-id="42448-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42448-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42448-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="42448-111">-GatewayVip</span></span>
<span data-ttu-id="42448-112">Adres VIP bramy w celu zresetowania określonego wystąpienia bramy (na przykład w przypadku bram Active-Active z obsługą funkcji). Domyślnie wystąpienie główne bramy zostanie zresetowane, jeśli nie zostanie przekazana żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="42448-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42448-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-113">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42448-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42448-114">CommonParameters</span></span>
<span data-ttu-id="42448-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42448-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42448-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42448-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42448-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42448-117">INPUTS</span></span>

### <span data-ttu-id="42448-118">Ciąg</span><span class="sxs-lookup"><span data-stu-id="42448-118">String</span></span>
<span data-ttu-id="42448-119">Parametr "GatewayVip" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="42448-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="42448-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="42448-121">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="42448-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="42448-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42448-122">OUTPUTS</span></span>

### <span data-ttu-id="42448-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="42448-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42448-124">NOTES</span></span>

## <span data-ttu-id="42448-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42448-125">RELATED LINKS</span></span>

[<span data-ttu-id="42448-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="42448-127">Nowe — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="42448-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="42448-129">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="42448-130">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42448-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


