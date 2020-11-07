---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892898"
---
# <span data-ttu-id="efc5a-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="efc5a-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="efc5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efc5a-102">SYNOPSIS</span></span>

## <span data-ttu-id="efc5a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efc5a-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc5a-104">Opis</span><span class="sxs-lookup"><span data-stu-id="efc5a-104">DESCRIPTION</span></span>

## <span data-ttu-id="efc5a-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efc5a-105">EXAMPLES</span></span>

### <span data-ttu-id="efc5a-106">1:1</span><span class="sxs-lookup"><span data-stu-id="efc5a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="efc5a-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efc5a-107">PARAMETERS</span></span>

### <span data-ttu-id="efc5a-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc5a-108">-DefaultProfile</span></span>
<span data-ttu-id="efc5a-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="efc5a-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc5a-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="efc5a-110">-Name</span></span>
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

### <span data-ttu-id="efc5a-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="efc5a-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="efc5a-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efc5a-112">-Confirm</span></span>
<span data-ttu-id="efc5a-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc5a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc5a-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc5a-114">-WhatIf</span></span>
<span data-ttu-id="efc5a-115">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc5a-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc5a-116">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="efc5a-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc5a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc5a-117">CommonParameters</span></span>
<span data-ttu-id="efc5a-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc5a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc5a-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc5a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc5a-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc5a-120">INPUTS</span></span>

### <span data-ttu-id="efc5a-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="efc5a-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="efc5a-122">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="efc5a-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="efc5a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efc5a-123">OUTPUTS</span></span>

### <span data-ttu-id="efc5a-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="efc5a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="efc5a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efc5a-125">NOTES</span></span>

## <span data-ttu-id="efc5a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efc5a-126">RELATED LINKS</span></span>

