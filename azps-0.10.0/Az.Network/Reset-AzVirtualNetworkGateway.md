---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892882"
---
# <span data-ttu-id="59da4-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="59da4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59da4-102">SYNOPSIS</span></span>

## <span data-ttu-id="59da4-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59da4-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59da4-104">Opis</span><span class="sxs-lookup"><span data-stu-id="59da4-104">DESCRIPTION</span></span>

## <span data-ttu-id="59da4-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59da4-105">EXAMPLES</span></span>

### <span data-ttu-id="59da4-106">1:1</span><span class="sxs-lookup"><span data-stu-id="59da4-106">1:</span></span>
```

```

## <span data-ttu-id="59da4-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59da4-107">PARAMETERS</span></span>

### <span data-ttu-id="59da4-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59da4-108">-AsJob</span></span>
<span data-ttu-id="59da4-109">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="59da4-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59da4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59da4-110">-DefaultProfile</span></span>
<span data-ttu-id="59da4-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59da4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59da4-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="59da4-112">-GatewayVip</span></span>
<span data-ttu-id="59da4-113">Adres VIP bramy w celu zresetowania określonego wystąpienia bramy (na przykład w przypadku bram Active-Active z obsługą funkcji). Domyślnie wystąpienie główne bramy zostanie zresetowane, jeśli nie zostanie przekazana żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="59da4-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="59da4-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="59da4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59da4-115">CommonParameters</span></span>
<span data-ttu-id="59da4-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59da4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59da4-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59da4-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59da4-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59da4-118">INPUTS</span></span>

### <span data-ttu-id="59da4-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="59da4-119">String</span></span>
<span data-ttu-id="59da4-120">Parametr "GatewayVip" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="59da4-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="59da4-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="59da4-122">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="59da4-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="59da4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59da4-123">OUTPUTS</span></span>

### <span data-ttu-id="59da4-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="59da4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59da4-125">NOTES</span></span>

## <span data-ttu-id="59da4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59da4-126">RELATED LINKS</span></span>

[<span data-ttu-id="59da4-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="59da4-128">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="59da4-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="59da4-130">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="59da4-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59da4-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


