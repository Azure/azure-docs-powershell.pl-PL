---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718635"
---
# <span data-ttu-id="ac69c-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ac69c-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="ac69c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac69c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac69c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac69c-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac69c-104">Opis</span><span class="sxs-lookup"><span data-stu-id="ac69c-104">DESCRIPTION</span></span>

## <span data-ttu-id="ac69c-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac69c-105">EXAMPLES</span></span>

### <span data-ttu-id="ac69c-106">1:1</span><span class="sxs-lookup"><span data-stu-id="ac69c-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ac69c-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac69c-107">PARAMETERS</span></span>

### <span data-ttu-id="ac69c-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac69c-108">-DefaultProfile</span></span>
<span data-ttu-id="ac69c-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac69c-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac69c-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac69c-110">-Name</span></span>
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

### <span data-ttu-id="ac69c-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac69c-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="ac69c-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac69c-112">-Confirm</span></span>
<span data-ttu-id="ac69c-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac69c-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac69c-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac69c-114">-WhatIf</span></span>
<span data-ttu-id="ac69c-115">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac69c-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac69c-116">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac69c-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac69c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac69c-117">CommonParameters</span></span>
<span data-ttu-id="ac69c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac69c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac69c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac69c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac69c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac69c-120">INPUTS</span></span>

### <span data-ttu-id="ac69c-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac69c-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ac69c-122">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ac69c-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="ac69c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac69c-123">OUTPUTS</span></span>

### <span data-ttu-id="ac69c-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac69c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ac69c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac69c-125">NOTES</span></span>

## <span data-ttu-id="ac69c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac69c-126">RELATED LINKS</span></span>

