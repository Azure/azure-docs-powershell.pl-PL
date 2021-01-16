---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342730"
---
# <span data-ttu-id="576ec-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="576ec-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="576ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="576ec-102">SYNOPSIS</span></span>
<span data-ttu-id="576ec-103">Usuwa konfigurację puli adresów NAT przychodzącą z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="576ec-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="576ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="576ec-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="576ec-105">DESCRIPTION</span></span>
<span data-ttu-id="576ec-106">Polecenie cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** usuwa konfigurację puli adresów NAT przychodzącą z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="576ec-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="576ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="576ec-107">EXAMPLES</span></span>

### <span data-ttu-id="576ec-108">1: Usuń</span><span class="sxs-lookup"><span data-stu-id="576ec-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="576ec-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="576ec-109">PARAMETERS</span></span>

### <span data-ttu-id="576ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ec-110">-DefaultProfile</span></span>
<span data-ttu-id="576ec-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="576ec-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576ec-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="576ec-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="576ec-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="576ec-113">-Name</span></span>
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

### <span data-ttu-id="576ec-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="576ec-114">-Confirm</span></span>
<span data-ttu-id="576ec-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ec-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576ec-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576ec-116">-WhatIf</span></span>
<span data-ttu-id="576ec-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ec-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="576ec-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="576ec-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ec-119">CommonParameters</span></span>
<span data-ttu-id="576ec-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ec-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576ec-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ec-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="576ec-122">INPUTS</span></span>

### <span data-ttu-id="576ec-123">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="576ec-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="576ec-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="576ec-124">OUTPUTS</span></span>

### <span data-ttu-id="576ec-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="576ec-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="576ec-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="576ec-126">NOTES</span></span>

## <span data-ttu-id="576ec-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="576ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="576ec-128">Dodaj-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="576ec-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="576ec-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="576ec-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="576ec-130">Nowe — AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="576ec-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="576ec-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="576ec-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
