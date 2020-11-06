---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551188"
---
# <span data-ttu-id="ae18d-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae18d-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ae18d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae18d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae18d-103">Umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ae18d-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae18d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae18d-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae18d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae18d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae18d-106">Polecenie cmdlet **Add-AzureRmLoadBalancerProbeConfig** umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae18d-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ae18d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae18d-107">EXAMPLES</span></span>

### <span data-ttu-id="ae18d-108">Przykład 1 Dodawanie konfiguracji sondy do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ae18d-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="ae18d-109">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie myLb, dodaje do niej określoną konfigurację sondy, a następnie używa polecenia cmdlet **Set-AzureRmLoadBalancer** w celu zaktualizowania modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ae18d-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="ae18d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae18d-110">PARAMETERS</span></span>

### <span data-ttu-id="ae18d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae18d-111">-DefaultProfile</span></span>
<span data-ttu-id="ae18d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae18d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae18d-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ae18d-113">-IntervalInSeconds</span></span>
<span data-ttu-id="ae18d-114">Określa interwał (w sekundach) między sondami dla każdego wystąpienia usługi równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ae18d-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="ae18d-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ae18d-115">-LoadBalancer</span></span>
<span data-ttu-id="ae18d-116">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="ae18d-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ae18d-117">To polecenie cmdlet umożliwia dodanie konfiguracji sondy do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ae18d-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae18d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae18d-118">-Name</span></span>
<span data-ttu-id="ae18d-119">Określa nazwę konfiguracji sondy, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="ae18d-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="ae18d-120">-Port</span><span class="sxs-lookup"><span data-stu-id="ae18d-120">-Port</span></span>
<span data-ttu-id="ae18d-121">Określa port, na którym sondy powinny być połączone z usługą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ae18d-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="ae18d-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ae18d-122">-ProbeCount</span></span>
<span data-ttu-id="ae18d-123">Określa liczbę kolejnych awarii dla wystąpienia, które można uznać za niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="ae18d-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="ae18d-124">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="ae18d-124">-Protocol</span></span>
<span data-ttu-id="ae18d-125">Określa protokół, który ma być używany do badania.</span><span class="sxs-lookup"><span data-stu-id="ae18d-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="ae18d-126">Dopuszczalne wartości tego parametru to: TCP lub http.</span><span class="sxs-lookup"><span data-stu-id="ae18d-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="ae18d-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ae18d-127">-RequestPath</span></span>
<span data-ttu-id="ae18d-128">Określa ścieżkę w usłudze równoważenia obciążenia do sondowania w celu określenia kondycji.</span><span class="sxs-lookup"><span data-stu-id="ae18d-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="ae18d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae18d-129">-Confirm</span></span>
<span data-ttu-id="ae18d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae18d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae18d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae18d-131">-WhatIf</span></span>
<span data-ttu-id="ae18d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae18d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae18d-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae18d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae18d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae18d-134">CommonParameters</span></span>
<span data-ttu-id="ae18d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae18d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae18d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae18d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae18d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae18d-137">INPUTS</span></span>

### <span data-ttu-id="ae18d-138">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae18d-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ae18d-139">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae18d-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="ae18d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae18d-140">OUTPUTS</span></span>

### <span data-ttu-id="ae18d-141">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae18d-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae18d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae18d-142">NOTES</span></span>

## <span data-ttu-id="ae18d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae18d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ae18d-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae18d-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae18d-145">Nowe — AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae18d-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae18d-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae18d-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae18d-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae18d-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="ae18d-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae18d-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


