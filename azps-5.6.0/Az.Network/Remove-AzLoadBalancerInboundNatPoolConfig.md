---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9e266ad824d5637137649c73d4e3b427af2f176b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996290"
---
# <span data-ttu-id="26b12-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26b12-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="26b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b12-102">SYNOPSIS</span></span>
<span data-ttu-id="26b12-103">Usuwa konfigurację puli nat ruchu przychodzącego z urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="26b12-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="26b12-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26b12-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b12-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="26b12-105">DESCRIPTION</span></span>
<span data-ttu-id="26b12-106">Polecenie **cmdlet Remove-AzLoadBalancerInboundNatPoolConfig** usuwa konfigurację puli nat ruchu przychodzącego z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="26b12-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="26b12-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26b12-107">EXAMPLES</span></span>

### <span data-ttu-id="26b12-108">1. Usuń</span><span class="sxs-lookup"><span data-stu-id="26b12-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="26b12-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b12-109">PARAMETERS</span></span>

### <span data-ttu-id="26b12-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b12-110">-DefaultProfile</span></span>
<span data-ttu-id="26b12-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26b12-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b12-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26b12-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="26b12-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26b12-113">-Name</span></span>
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

### <span data-ttu-id="26b12-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26b12-114">-Confirm</span></span>
<span data-ttu-id="26b12-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26b12-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b12-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b12-116">-WhatIf</span></span>
<span data-ttu-id="26b12-117">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b12-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26b12-118">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26b12-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b12-119">CommonParameters</span></span>
<span data-ttu-id="26b12-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b12-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b12-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b12-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b12-122">INPUTS</span></span>

### <span data-ttu-id="26b12-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26b12-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26b12-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b12-124">OUTPUTS</span></span>

### <span data-ttu-id="26b12-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26b12-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26b12-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26b12-126">NOTES</span></span>

## <span data-ttu-id="26b12-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26b12-127">RELATED LINKS</span></span>

[<span data-ttu-id="26b12-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26b12-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="26b12-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26b12-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="26b12-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26b12-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="26b12-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26b12-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
