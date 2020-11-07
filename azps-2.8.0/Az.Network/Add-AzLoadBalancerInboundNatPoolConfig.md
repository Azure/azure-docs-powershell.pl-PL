---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 672829daffa2117265e8f43b30f504adc702f3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870860"
---
# <span data-ttu-id="7797f-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7797f-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7797f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7797f-102">SYNOPSIS</span></span>
<span data-ttu-id="7797f-103">Dodaje przychodzącą pulę NAT do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7797f-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7797f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7797f-104">SYNTAX</span></span>

### <span data-ttu-id="7797f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7797f-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7797f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7797f-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7797f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7797f-107">DESCRIPTION</span></span>
<span data-ttu-id="7797f-108">Polecenie cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** dodaje przychodzącą pulę NAT do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7797f-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7797f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7797f-109">EXAMPLES</span></span>

### <span data-ttu-id="7797f-110">1: Dodawanie</span><span class="sxs-lookup"><span data-stu-id="7797f-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="7797f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7797f-111">PARAMETERS</span></span>

### <span data-ttu-id="7797f-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7797f-112">-BackendPort</span></span>
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

### <span data-ttu-id="7797f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7797f-113">-DefaultProfile</span></span>
<span data-ttu-id="7797f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7797f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7797f-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7797f-115">-EnableFloatingIP</span></span>
<span data-ttu-id="7797f-116">Umożliwia skonfigurowanie punktu końcowego maszyny wirtualnej dla przestawnego adresu IP wymaganego do skonfigurowania grupy dostępności funkcji SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="7797f-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="7797f-117">To ustawienie jest wymagane w przypadku używania grup dostępności funkcji SQL AlwaysOn w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7797f-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="7797f-118">Tego ustawienia nie można zmienić po utworzeniu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7797f-118">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7797f-119">-EnableTcpReset</span></span>
<span data-ttu-id="7797f-120">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="7797f-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7797f-121">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="7797f-121">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7797f-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7797f-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7797f-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="7797f-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7797f-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="7797f-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7797f-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7797f-127">Limit czasu bezczynności połączenia TCP.</span><span class="sxs-lookup"><span data-stu-id="7797f-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="7797f-128">Wartość może być ustawiona między 4 a 30 minut.</span><span class="sxs-lookup"><span data-stu-id="7797f-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="7797f-129">Wartość domyślna to 4 minuty.</span><span class="sxs-lookup"><span data-stu-id="7797f-129">The default value is 4 minutes.</span></span> <span data-ttu-id="7797f-130">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="7797f-130">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7797f-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="7797f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7797f-132">-Name</span></span>
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

### <span data-ttu-id="7797f-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7797f-133">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7797f-134">-Confirm</span></span>
<span data-ttu-id="7797f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7797f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7797f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7797f-136">-WhatIf</span></span>
<span data-ttu-id="7797f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7797f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7797f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7797f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7797f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7797f-139">CommonParameters</span></span>
<span data-ttu-id="7797f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7797f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7797f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7797f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7797f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7797f-142">INPUTS</span></span>

### <span data-ttu-id="7797f-143">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7797f-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7797f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7797f-144">System.String</span></span>

### <span data-ttu-id="7797f-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7797f-145">System.Int32</span></span>

### <span data-ttu-id="7797f-146">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7797f-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7797f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7797f-147">OUTPUTS</span></span>

### <span data-ttu-id="7797f-148">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7797f-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7797f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7797f-149">NOTES</span></span>

## <span data-ttu-id="7797f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7797f-150">RELATED LINKS</span></span>

[<span data-ttu-id="7797f-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7797f-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7797f-152">Nowe — AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7797f-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7797f-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7797f-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7797f-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7797f-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
