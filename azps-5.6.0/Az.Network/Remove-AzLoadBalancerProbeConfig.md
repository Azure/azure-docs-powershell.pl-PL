---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993665"
---
# <span data-ttu-id="2ca2d-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ca2d-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2ca2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca2d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca2d-103">Usuwa konfigurację konfiguracji konfiguracji z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="2ca2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ca2d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca2d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ca2d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca2d-106">Polecenie **cmdlet Remove-AzLoadBalancerProbeConfig** usuwa konfigurację konfiguracji konfiguracji ładowania.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="2ca2d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ca2d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca2d-108">Przykład 1. Usunięcie konfiguracji konfiguracji konfiguracji ładowania z urządzenia do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="2ca2d-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="2ca2d-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $loadbalancer ładowania.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="2ca2d-110">Drugie polecenie usuwa konfigurację o nazwie MyProbe z równoważenia obciążenia w programie $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="2ca2d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ca2d-111">PARAMETERS</span></span>

### <span data-ttu-id="2ca2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca2d-112">-DefaultProfile</span></span>
<span data-ttu-id="2ca2d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca2d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ca2d-114">-LoadBalancer</span></span>
<span data-ttu-id="2ca2d-115">Określa równoważenie obciążenia zawierające konfigurację, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2ca2d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ca2d-116">-Name</span></span>
<span data-ttu-id="2ca2d-117">Określa nazwę konfiguracji, która ma być usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2ca2d-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ca2d-118">-Confirm</span></span>
<span data-ttu-id="2ca2d-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca2d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca2d-120">-WhatIf</span></span>
<span data-ttu-id="2ca2d-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ca2d-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca2d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca2d-123">CommonParameters</span></span>
<span data-ttu-id="2ca2d-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca2d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca2d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca2d-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ca2d-126">INPUTS</span></span>

### <span data-ttu-id="2ca2d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ca2d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ca2d-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ca2d-128">OUTPUTS</span></span>

### <span data-ttu-id="2ca2d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ca2d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ca2d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ca2d-130">NOTES</span></span>

## <span data-ttu-id="2ca2d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ca2d-131">RELATED LINKS</span></span>

[<span data-ttu-id="2ca2d-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ca2d-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ca2d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ca2d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2ca2d-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ca2d-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ca2d-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ca2d-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ca2d-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ca2d-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


