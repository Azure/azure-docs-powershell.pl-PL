---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892777"
---
# <span data-ttu-id="1a1d2-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a1d2-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="1a1d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1d2-103">Umożliwia ustawienie stanu celu dla konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="1a1d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a1d2-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a1d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="1a1d2-106">Polecenie cmdlet **Set-AzLoadBalancerProbeConfig** ustawia stan celu dla konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="1a1d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a1d2-107">EXAMPLES</span></span>

### <span data-ttu-id="1a1d2-108">Przykład 1: modyfikowanie konfiguracji sondy w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="1a1d2-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="1a1d2-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="1a1d2-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerProbeConfig, które umożliwia dodanie nowej konfiguracji sondy.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="1a1d2-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancerProbeConfig** , co ustawia nową konfigurację.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="1a1d2-112">Należy zauważyć, że konieczne jest określenie kilku parametrów, które zostały określone w poprzednim poleceniu, ponieważ są one wymagane przez bieżące polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="1a1d2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a1d2-113">PARAMETERS</span></span>

### <span data-ttu-id="1a1d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1d2-114">-DefaultProfile</span></span>
<span data-ttu-id="1a1d2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1a1d2-116">-IntervalInSeconds</span></span>
<span data-ttu-id="1a1d2-117">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-118">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="1a1d2-118">-LoadBalancer</span></span>
<span data-ttu-id="1a1d2-119">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-119">Specifies a load balancer.</span></span>
<span data-ttu-id="1a1d2-120">To polecenie cmdlet ustawia stan celu dla konfiguracji sondy dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a1d2-121">-Name</span></span>
<span data-ttu-id="1a1d2-122">Określa nazwę konfiguracji sondy, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-123">-Port</span><span class="sxs-lookup"><span data-stu-id="1a1d2-123">-Port</span></span>
<span data-ttu-id="1a1d2-124">Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="1a1d2-125">-ProbeCount</span></span>
<span data-ttu-id="1a1d2-126">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="1a1d2-127">-Protocol</span></span>
<span data-ttu-id="1a1d2-128">Określa protokół, który ma być używany do sondowania.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="1a1d2-129">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="1a1d2-130">-RequestPath</span></span>
<span data-ttu-id="1a1d2-131">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1d2-132">CommonParameters</span></span>
<span data-ttu-id="1a1d2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1d2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1d2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1d2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a1d2-135">INPUTS</span></span>

### <span data-ttu-id="1a1d2-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a1d2-136">PSLoadBalancer</span></span>
<span data-ttu-id="1a1d2-137">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="1a1d2-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1a1d2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a1d2-138">OUTPUTS</span></span>

### <span data-ttu-id="1a1d2-139">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a1d2-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1a1d2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a1d2-140">NOTES</span></span>

## <span data-ttu-id="1a1d2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a1d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="1a1d2-142">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a1d2-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a1d2-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a1d2-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1a1d2-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a1d2-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a1d2-145">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a1d2-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a1d2-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a1d2-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


