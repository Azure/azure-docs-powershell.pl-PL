---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504394"
---
# <span data-ttu-id="e751a-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e751a-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e751a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e751a-102">SYNOPSIS</span></span>
<span data-ttu-id="e751a-103">Umożliwia zaktualizowanie konfiguracji sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e751a-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e751a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e751a-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e751a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e751a-105">DESCRIPTION</span></span>
<span data-ttu-id="e751a-106">Polecenie cmdlet **Set-AzLoadBalancerProbeConfig** umożliwia zaktualizowanie konfiguracji sondy modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e751a-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e751a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e751a-107">EXAMPLES</span></span>

### <span data-ttu-id="e751a-108">Przykład 1: modyfikowanie konfiguracji sondy w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e751a-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="e751a-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="e751a-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e751a-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerProbeConfig, które umożliwia dodanie nowej konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="e751a-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="e751a-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancerProbeConfig**, co ustawia nową konfigurację.</span><span class="sxs-lookup"><span data-stu-id="e751a-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="e751a-112">Należy zauważyć, że konieczne jest określenie kilku parametrów, które zostały określone w poprzednim poleceniu, ponieważ są one wymagane przez bieżące polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751a-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="e751a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e751a-113">PARAMETERS</span></span>

### <span data-ttu-id="e751a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e751a-114">-DefaultProfile</span></span>
<span data-ttu-id="e751a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e751a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e751a-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e751a-116">-IntervalInSeconds</span></span>
<span data-ttu-id="e751a-117">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e751a-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-118">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e751a-118">-LoadBalancer</span></span>
<span data-ttu-id="e751a-119">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e751a-119">Specifies a load balancer.</span></span>
<span data-ttu-id="e751a-120">To polecenie cmdlet umożliwia zaktualizowanie konfiguracji sondy dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e751a-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e751a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e751a-121">-Name</span></span>
<span data-ttu-id="e751a-122">Określa nazwę konfiguracji sondy, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751a-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-123">-Port</span><span class="sxs-lookup"><span data-stu-id="e751a-123">-Port</span></span>
<span data-ttu-id="e751a-124">Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e751a-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="e751a-125">-ProbeCount</span></span>
<span data-ttu-id="e751a-126">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="e751a-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e751a-127">-Protocol</span></span>
<span data-ttu-id="e751a-128">Określa protokół, który ma być używany do sondowania.</span><span class="sxs-lookup"><span data-stu-id="e751a-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="e751a-129">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="e751a-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="e751a-130">-RequestPath</span></span>
<span data-ttu-id="e751a-131">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="e751a-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e751a-132">-Confirm</span></span>
<span data-ttu-id="e751a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e751a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e751a-134">-WhatIf</span></span>
<span data-ttu-id="e751a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e751a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e751a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e751a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e751a-137">CommonParameters</span></span>
<span data-ttu-id="e751a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e751a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e751a-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e751a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e751a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e751a-140">INPUTS</span></span>

### <span data-ttu-id="e751a-141">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e751a-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e751a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e751a-142">System.String</span></span>

### <span data-ttu-id="e751a-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e751a-143">System.Int32</span></span>

## <span data-ttu-id="e751a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e751a-144">OUTPUTS</span></span>

### <span data-ttu-id="e751a-145">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e751a-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e751a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e751a-146">NOTES</span></span>

## <span data-ttu-id="e751a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e751a-147">RELATED LINKS</span></span>

[<span data-ttu-id="e751a-148">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e751a-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e751a-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e751a-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e751a-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e751a-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e751a-151">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e751a-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e751a-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e751a-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


