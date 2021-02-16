---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203082"
---
# <span data-ttu-id="fb7db-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fb7db-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="fb7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7db-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7db-103">Pobiera jedną lub więcej konfiguracji puli nat ruchu przychodzącego z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fb7db-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="fb7db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb7db-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7db-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb7db-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7db-106">Polecenie **cmdlet Get-AzLoadBalancerInboundNatPoolConfig** pobiera jedną lub więcej konfiguracji puli nat ruchu przychodzącego z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fb7db-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="fb7db-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb7db-107">EXAMPLES</span></span>

### <span data-ttu-id="fb7db-108">1: Pobierz</span><span class="sxs-lookup"><span data-stu-id="fb7db-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="fb7db-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb7db-109">PARAMETERS</span></span>

### <span data-ttu-id="fb7db-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7db-110">-DefaultProfile</span></span>
<span data-ttu-id="fb7db-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7db-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7db-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb7db-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="fb7db-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb7db-113">-Name</span></span>
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

### <span data-ttu-id="fb7db-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7db-114">CommonParameters</span></span>
<span data-ttu-id="fb7db-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7db-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7db-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb7db-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7db-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7db-117">INPUTS</span></span>

### <span data-ttu-id="fb7db-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb7db-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fb7db-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb7db-119">OUTPUTS</span></span>

### <span data-ttu-id="fb7db-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="fb7db-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="fb7db-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb7db-121">NOTES</span></span>

## <span data-ttu-id="fb7db-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7db-122">RELATED LINKS</span></span>

[<span data-ttu-id="fb7db-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fb7db-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fb7db-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fb7db-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fb7db-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fb7db-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fb7db-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fb7db-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
