---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899220"
---
# <span data-ttu-id="f8647-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8647-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8647-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8647-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8647-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8647-104">Opis</span><span class="sxs-lookup"><span data-stu-id="f8647-104">DESCRIPTION</span></span>

## <span data-ttu-id="f8647-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8647-105">EXAMPLES</span></span>

### <span data-ttu-id="f8647-106">1:1</span><span class="sxs-lookup"><span data-stu-id="f8647-106">1:</span></span>
```

```

## <span data-ttu-id="f8647-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8647-107">PARAMETERS</span></span>

### <span data-ttu-id="f8647-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8647-108">-AsJob</span></span>
<span data-ttu-id="f8647-109">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8647-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8647-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8647-110">-DefaultProfile</span></span>
<span data-ttu-id="f8647-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8647-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8647-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="f8647-112">-GatewayVip</span></span>
<span data-ttu-id="f8647-113">Adres VIP bramy w celu zresetowania określonego wystąpienia bramy (na przykład w przypadku bram Active-Active z obsługą funkcji). Domyślnie wystąpienie główne bramy zostanie zresetowane, jeśli nie zostanie przekazana żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="f8647-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="f8647-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="f8647-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8647-115">CommonParameters</span></span>
<span data-ttu-id="f8647-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8647-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8647-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8647-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8647-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8647-118">INPUTS</span></span>

### <span data-ttu-id="f8647-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f8647-119">String</span></span>
<span data-ttu-id="f8647-120">Parametr "GatewayVip" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="f8647-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="f8647-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f8647-122">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f8647-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="f8647-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8647-123">OUTPUTS</span></span>

### <span data-ttu-id="f8647-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8647-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8647-125">NOTES</span></span>

## <span data-ttu-id="f8647-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8647-126">RELATED LINKS</span></span>

[<span data-ttu-id="f8647-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8647-128">Nowe — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8647-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8647-130">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8647-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8647-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


