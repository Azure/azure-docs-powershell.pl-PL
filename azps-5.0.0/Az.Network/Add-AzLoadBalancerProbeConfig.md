---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319260"
---
# <span data-ttu-id="f12ea-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f12ea-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f12ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f12ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f12ea-103">Umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f12ea-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="f12ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f12ea-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f12ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f12ea-105">DESCRIPTION</span></span>
<span data-ttu-id="f12ea-106">Polecenie cmdlet **Add-AzLoadBalancerProbeConfig** umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f12ea-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f12ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f12ea-107">EXAMPLES</span></span>

### <span data-ttu-id="f12ea-108">Przykład 1. Dodawanie konfiguracji sondy do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f12ea-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="f12ea-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie myLb, dodaje do niej określoną konfigurację sondy, a następnie używa polecenia cmdlet **Set-AzLoadBalancer** w celu zaktualizowania modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f12ea-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="f12ea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f12ea-110">PARAMETERS</span></span>

### <span data-ttu-id="f12ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12ea-111">-DefaultProfile</span></span>
<span data-ttu-id="f12ea-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f12ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f12ea-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f12ea-113">-IntervalInSeconds</span></span>
<span data-ttu-id="f12ea-114">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f12ea-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="f12ea-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f12ea-115">-LoadBalancer</span></span>
<span data-ttu-id="f12ea-116">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="f12ea-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f12ea-117">To polecenie cmdlet umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f12ea-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f12ea-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f12ea-118">-Name</span></span>
<span data-ttu-id="f12ea-119">Określa nazwę konfiguracji sondy, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="f12ea-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="f12ea-120">-Port</span><span class="sxs-lookup"><span data-stu-id="f12ea-120">-Port</span></span>
<span data-ttu-id="f12ea-121">Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f12ea-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="f12ea-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="f12ea-122">-ProbeCount</span></span>
<span data-ttu-id="f12ea-123">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="f12ea-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="f12ea-124">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f12ea-124">-Protocol</span></span>
<span data-ttu-id="f12ea-125">Określa protokół, który ma być używany do badania.</span><span class="sxs-lookup"><span data-stu-id="f12ea-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="f12ea-126">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="f12ea-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="f12ea-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="f12ea-127">-RequestPath</span></span>
<span data-ttu-id="f12ea-128">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="f12ea-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="f12ea-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f12ea-129">-Confirm</span></span>
<span data-ttu-id="f12ea-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f12ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f12ea-131">-WhatIf</span></span>
<span data-ttu-id="f12ea-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12ea-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f12ea-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f12ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f12ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12ea-134">CommonParameters</span></span>
<span data-ttu-id="f12ea-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12ea-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f12ea-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12ea-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f12ea-137">INPUTS</span></span>

### <span data-ttu-id="f12ea-138">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f12ea-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f12ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f12ea-139">System.String</span></span>

### <span data-ttu-id="f12ea-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f12ea-140">System.Int32</span></span>

## <span data-ttu-id="f12ea-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f12ea-141">OUTPUTS</span></span>

### <span data-ttu-id="f12ea-142">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f12ea-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f12ea-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f12ea-143">NOTES</span></span>

## <span data-ttu-id="f12ea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f12ea-144">RELATED LINKS</span></span>

[<span data-ttu-id="f12ea-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f12ea-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f12ea-146">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f12ea-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f12ea-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f12ea-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f12ea-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f12ea-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="f12ea-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f12ea-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


