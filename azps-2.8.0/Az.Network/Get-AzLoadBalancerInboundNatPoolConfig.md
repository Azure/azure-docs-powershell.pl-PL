---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: da7004c8737bf454ea8847b529f003f5b1909f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870171"
---
# <span data-ttu-id="58b51-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58b51-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="58b51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58b51-102">SYNOPSIS</span></span>
<span data-ttu-id="58b51-103">Pobiera co najmniej jeden zestaw konfiguracji przychodzących adresów NAT z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b51-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="58b51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58b51-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58b51-105">DESCRIPTION</span></span>
<span data-ttu-id="58b51-106">Polecenie cmdlet **Get-AzLoadBalancerInboundNatPoolConfig** pobiera co najmniej jeden zestaw konfiguracji przychodzących adresów NAT z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b51-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="58b51-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58b51-107">EXAMPLES</span></span>

### <span data-ttu-id="58b51-108">1: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="58b51-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="58b51-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58b51-109">PARAMETERS</span></span>

### <span data-ttu-id="58b51-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b51-110">-DefaultProfile</span></span>
<span data-ttu-id="58b51-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58b51-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b51-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="58b51-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="58b51-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58b51-113">-Name</span></span>
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

### <span data-ttu-id="58b51-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b51-114">CommonParameters</span></span>
<span data-ttu-id="58b51-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b51-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b51-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58b51-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b51-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58b51-117">INPUTS</span></span>

### <span data-ttu-id="58b51-118">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58b51-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="58b51-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58b51-119">OUTPUTS</span></span>

### <span data-ttu-id="58b51-120">Microsoft. Azure. Commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="58b51-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="58b51-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58b51-121">NOTES</span></span>

## <span data-ttu-id="58b51-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58b51-122">RELATED LINKS</span></span>

[<span data-ttu-id="58b51-123">Dodaj-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58b51-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58b51-124">Nowe — AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58b51-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58b51-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58b51-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58b51-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58b51-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
