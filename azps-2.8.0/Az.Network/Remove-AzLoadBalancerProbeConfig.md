---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6a1e5f4de5ec98030cc9bd3300d9e9fd447f6f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869720"
---
# <span data-ttu-id="9bd17-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bd17-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9bd17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bd17-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd17-103">Umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9bd17-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="9bd17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bd17-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bd17-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd17-106">Polecenie cmdlet **Remove-AzLoadBalancerProbeConfig** umożliwia usunięcie konfiguracji sondy z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9bd17-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="9bd17-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bd17-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd17-108">Przykład 1: Usuwanie konfiguracji sondy z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9bd17-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9bd17-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9bd17-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="9bd17-110">Drugie polecenie usuwa konfigurację o nazwie Moja Sonda z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9bd17-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9bd17-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bd17-111">PARAMETERS</span></span>

### <span data-ttu-id="9bd17-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd17-112">-DefaultProfile</span></span>
<span data-ttu-id="9bd17-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd17-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd17-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9bd17-114">-LoadBalancer</span></span>
<span data-ttu-id="9bd17-115">Umożliwia określenie modułu równoważenia obciążenia zawierającego konfigurację sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd17-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bd17-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bd17-116">-Name</span></span>
<span data-ttu-id="9bd17-117">Określa nazwę konfiguracji sondy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd17-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bd17-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bd17-118">-Confirm</span></span>
<span data-ttu-id="9bd17-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd17-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd17-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd17-120">-WhatIf</span></span>
<span data-ttu-id="9bd17-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd17-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bd17-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bd17-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd17-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd17-123">CommonParameters</span></span>
<span data-ttu-id="9bd17-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd17-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd17-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd17-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd17-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bd17-126">INPUTS</span></span>

### <span data-ttu-id="9bd17-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bd17-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9bd17-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bd17-128">OUTPUTS</span></span>

### <span data-ttu-id="9bd17-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bd17-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9bd17-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bd17-130">NOTES</span></span>

## <span data-ttu-id="9bd17-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bd17-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bd17-132">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bd17-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bd17-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bd17-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9bd17-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bd17-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bd17-135">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bd17-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bd17-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bd17-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


