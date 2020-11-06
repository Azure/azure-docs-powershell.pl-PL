---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524385"
---
# <span data-ttu-id="31ca0-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31ca0-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="31ca0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31ca0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ca0-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31ca0-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ca0-104">Opis</span><span class="sxs-lookup"><span data-stu-id="31ca0-104">DESCRIPTION</span></span>

## <span data-ttu-id="31ca0-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31ca0-105">EXAMPLES</span></span>

### <span data-ttu-id="31ca0-106">1: Usuń</span><span class="sxs-lookup"><span data-stu-id="31ca0-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="31ca0-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31ca0-107">PARAMETERS</span></span>

### <span data-ttu-id="31ca0-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ca0-108">-DefaultProfile</span></span>
<span data-ttu-id="31ca0-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31ca0-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ca0-110">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="31ca0-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31ca0-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31ca0-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ca0-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31ca0-112">-Confirm</span></span>
<span data-ttu-id="31ca0-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ca0-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ca0-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ca0-114">-WhatIf</span></span>
<span data-ttu-id="31ca0-115">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ca0-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31ca0-116">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31ca0-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ca0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ca0-117">CommonParameters</span></span>
<span data-ttu-id="31ca0-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ca0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ca0-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ca0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ca0-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31ca0-120">INPUTS</span></span>

### <span data-ttu-id="31ca0-121">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31ca0-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="31ca0-122">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31ca0-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="31ca0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31ca0-123">OUTPUTS</span></span>

### <span data-ttu-id="31ca0-124">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31ca0-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="31ca0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31ca0-125">NOTES</span></span>

## <span data-ttu-id="31ca0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31ca0-126">RELATED LINKS</span></span>
