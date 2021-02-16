---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203185"
---
# <span data-ttu-id="408a1-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="408a1-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="408a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408a1-102">SYNOPSIS</span></span>
<span data-ttu-id="408a1-103">Umożliwia dodanie konfiguracji konfiguracji do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="408a1-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="408a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="408a1-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="408a1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="408a1-105">DESCRIPTION</span></span>
<span data-ttu-id="408a1-106">Polecenie **cmdlet Add-AzLoadBalancerProbeConfig** dodaje konfigurację konfiguracji do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="408a1-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="408a1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="408a1-107">EXAMPLES</span></span>

### <span data-ttu-id="408a1-108">Przykład 1. Dodawanie konfiguracji konfiguracji do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="408a1-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="408a1-109">To polecenie pobiera równoważenie obciążenia o nazwie myLb, dodaje do niego określoną konfigurację konfiguracji konfiguracji, a następnie używa polecenia cmdlet **Set-AzLoadBalancer** w celu zaktualizowania równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="408a1-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="408a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="408a1-110">PARAMETERS</span></span>

### <span data-ttu-id="408a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408a1-111">-DefaultProfile</span></span>
<span data-ttu-id="408a1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="408a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408a1-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="408a1-113">-IntervalInSeconds</span></span>
<span data-ttu-id="408a1-114">Określa interwał (w sekundach) między poszczególnymi wystąpieniami usługi z obciążeniem.</span><span class="sxs-lookup"><span data-stu-id="408a1-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="408a1-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="408a1-115">-LoadBalancer</span></span>
<span data-ttu-id="408a1-116">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="408a1-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="408a1-117">To polecenie cmdlet dodaje konfigurację do równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="408a1-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="408a1-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="408a1-118">-Name</span></span>
<span data-ttu-id="408a1-119">Określa nazwę konfiguracji, która ma być do dodania.</span><span class="sxs-lookup"><span data-stu-id="408a1-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="408a1-120">— Port</span><span class="sxs-lookup"><span data-stu-id="408a1-120">-Port</span></span>
<span data-ttu-id="408a1-121">Określa port, za pomocą którego sieci powinny łączyć się z usługą z obciążeniem.</span><span class="sxs-lookup"><span data-stu-id="408a1-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="408a1-122">-Count</span><span class="sxs-lookup"><span data-stu-id="408a1-122">-ProbeCount</span></span>
<span data-ttu-id="408a1-123">Określa liczbę kolejnych wystąpień wystąpień wystąpienia, które zostaną uznane za usterki.</span><span class="sxs-lookup"><span data-stu-id="408a1-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="408a1-124">— Protokół</span><span class="sxs-lookup"><span data-stu-id="408a1-124">-Protocol</span></span>
<span data-ttu-id="408a1-125">Określa protokół, który ma być używany dla tego protokołu.</span><span class="sxs-lookup"><span data-stu-id="408a1-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="408a1-126">Dopuszczalne wartości dla tego parametru to: Tcp lub Http.</span><span class="sxs-lookup"><span data-stu-id="408a1-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="408a1-127">- RequestPath</span><span class="sxs-lookup"><span data-stu-id="408a1-127">-RequestPath</span></span>
<span data-ttu-id="408a1-128">Określa ścieżkę w usłudze równoważenia obciążenia, która ma być określana kondycję.</span><span class="sxs-lookup"><span data-stu-id="408a1-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="408a1-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="408a1-129">-Confirm</span></span>
<span data-ttu-id="408a1-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="408a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408a1-131">-WhatIf</span></span>
<span data-ttu-id="408a1-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="408a1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="408a1-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="408a1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408a1-134">CommonParameters</span></span>
<span data-ttu-id="408a1-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408a1-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408a1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408a1-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="408a1-137">INPUTS</span></span>

### <span data-ttu-id="408a1-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="408a1-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="408a1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="408a1-139">System.String</span></span>

### <span data-ttu-id="408a1-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="408a1-140">System.Int32</span></span>

## <span data-ttu-id="408a1-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="408a1-141">OUTPUTS</span></span>

### <span data-ttu-id="408a1-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="408a1-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="408a1-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="408a1-143">NOTES</span></span>

## <span data-ttu-id="408a1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="408a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="408a1-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="408a1-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="408a1-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="408a1-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="408a1-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="408a1-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="408a1-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="408a1-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="408a1-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="408a1-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


