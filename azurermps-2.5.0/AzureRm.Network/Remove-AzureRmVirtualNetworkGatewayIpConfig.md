---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897854"
---
# <span data-ttu-id="3bd76-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3bd76-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3bd76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bd76-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd76-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bd76-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd76-104">Opis</span><span class="sxs-lookup"><span data-stu-id="3bd76-104">DESCRIPTION</span></span>

## <span data-ttu-id="3bd76-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bd76-105">EXAMPLES</span></span>

### <span data-ttu-id="3bd76-106">1:1</span><span class="sxs-lookup"><span data-stu-id="3bd76-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3bd76-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bd76-107">PARAMETERS</span></span>

### <span data-ttu-id="3bd76-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd76-108">-DefaultProfile</span></span>
<span data-ttu-id="3bd76-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd76-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd76-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bd76-110">-Name</span></span>
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

### <span data-ttu-id="3bd76-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3bd76-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="3bd76-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bd76-112">-Confirm</span></span>
<span data-ttu-id="3bd76-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd76-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd76-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd76-114">-WhatIf</span></span>
<span data-ttu-id="3bd76-115">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd76-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd76-116">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bd76-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd76-117">CommonParameters</span></span>
<span data-ttu-id="3bd76-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd76-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd76-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bd76-120">INPUTS</span></span>

### <span data-ttu-id="3bd76-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3bd76-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3bd76-122">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3bd76-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3bd76-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bd76-123">OUTPUTS</span></span>

### <span data-ttu-id="3bd76-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3bd76-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3bd76-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bd76-125">NOTES</span></span>

## <span data-ttu-id="3bd76-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bd76-126">RELATED LINKS</span></span>

