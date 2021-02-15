---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189475"
---
# <span data-ttu-id="c43e1-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c43e1-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c43e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c43e1-103">Aktualizuje konfigurację sprzętu do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c43e1-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c43e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c43e1-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c43e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c43e1-106">Polecenie **cmdlet Set-AzLoadBalancerProbeConfig** aktualizuje konfigurację dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c43e1-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c43e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c43e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c43e1-108">Przykład 1. Modyfikowanie konfiguracji konfigurację równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c43e1-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="c43e1-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $slb zmienną.</span><span class="sxs-lookup"><span data-stu-id="c43e1-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c43e1-110">Drugie polecenie używa operatora potoku do przekazania równoważenia obciążenia w programie $slb do dodatku AzLoadBalancerProbeConfig, co powoduje dodanie do niego nowej konfiguracji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="c43e1-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="c43e1-111">Trzecie polecenie przekazuje równoważenie obciążenia do **set-AzLoadBalancerProbeConfig,** który ustawia nową konfigurację.</span><span class="sxs-lookup"><span data-stu-id="c43e1-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="c43e1-112">Należy pamiętać, że konieczne jest określenie kilku tych samych parametrów, które zostały określone w poprzednim poleceniu, ponieważ są one wymagane przez bieżące polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43e1-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="c43e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c43e1-113">PARAMETERS</span></span>

### <span data-ttu-id="c43e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43e1-114">-DefaultProfile</span></span>
<span data-ttu-id="c43e1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c43e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c43e1-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c43e1-116">-IntervalInSeconds</span></span>
<span data-ttu-id="c43e1-117">Określa interwał (w sekundach) między poszczególnymi wystąpieniami usługi z obciążeniem.</span><span class="sxs-lookup"><span data-stu-id="c43e1-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="c43e1-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c43e1-118">-LoadBalancer</span></span>
<span data-ttu-id="c43e1-119">Określa równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c43e1-119">Specifies a load balancer.</span></span>
<span data-ttu-id="c43e1-120">To polecenie cmdlet aktualizuje konfigurację równoważenia obciążenia określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c43e1-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c43e1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c43e1-121">-Name</span></span>
<span data-ttu-id="c43e1-122">Określa nazwę konfiguracji konfiguracji tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43e1-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c43e1-123">— Port</span><span class="sxs-lookup"><span data-stu-id="c43e1-123">-Port</span></span>
<span data-ttu-id="c43e1-124">Określa port, za pomocą którego sieci powinny łączyć się z usługą z obciążeniem.</span><span class="sxs-lookup"><span data-stu-id="c43e1-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="c43e1-125">-Count</span><span class="sxs-lookup"><span data-stu-id="c43e1-125">-ProbeCount</span></span>
<span data-ttu-id="c43e1-126">Określa liczbę kolejnych wystąpień wystąpień wystąpienia, które zostaną uznane za usterki.</span><span class="sxs-lookup"><span data-stu-id="c43e1-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="c43e1-127">— Protokół</span><span class="sxs-lookup"><span data-stu-id="c43e1-127">-Protocol</span></span>
<span data-ttu-id="c43e1-128">Określa protokół, który ma być używany do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="c43e1-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="c43e1-129">Dopuszczalne wartości dla tego parametru to: Tcp lub Http.</span><span class="sxs-lookup"><span data-stu-id="c43e1-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="c43e1-130">- RequestPath</span><span class="sxs-lookup"><span data-stu-id="c43e1-130">-RequestPath</span></span>
<span data-ttu-id="c43e1-131">Określa ścieżkę w usłudze równoważenia obciążenia, która ma być określana kondycję.</span><span class="sxs-lookup"><span data-stu-id="c43e1-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="c43e1-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c43e1-132">-Confirm</span></span>
<span data-ttu-id="c43e1-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c43e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43e1-134">-WhatIf</span></span>
<span data-ttu-id="c43e1-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43e1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c43e1-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c43e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43e1-137">CommonParameters</span></span>
<span data-ttu-id="c43e1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43e1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43e1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43e1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43e1-140">INPUTS</span></span>

### <span data-ttu-id="c43e1-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c43e1-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c43e1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c43e1-142">System.String</span></span>

### <span data-ttu-id="c43e1-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c43e1-143">System.Int32</span></span>

## <span data-ttu-id="c43e1-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43e1-144">OUTPUTS</span></span>

### <span data-ttu-id="c43e1-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c43e1-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c43e1-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c43e1-146">NOTES</span></span>

## <span data-ttu-id="c43e1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c43e1-147">RELATED LINKS</span></span>

[<span data-ttu-id="c43e1-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c43e1-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c43e1-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c43e1-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c43e1-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c43e1-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c43e1-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c43e1-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c43e1-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c43e1-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


