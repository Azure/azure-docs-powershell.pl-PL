---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 10539a09c8849f1afd5cd3c5bd9e249929577342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963898"
---
# <span data-ttu-id="34c41-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="34c41-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="34c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c41-102">SYNOPSIS</span></span>
<span data-ttu-id="34c41-103">Ustawia konfigurację puli nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34c41-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="34c41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34c41-104">SYNTAX</span></span>

### <span data-ttu-id="34c41-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="34c41-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c41-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34c41-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c41-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34c41-107">DESCRIPTION</span></span>
<span data-ttu-id="34c41-108">Polecenie **cmdlet Set-AzLoadBalancerInboundNatPoolConfig** ustawia konfigurację puli nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34c41-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="34c41-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34c41-109">EXAMPLES</span></span>

### <span data-ttu-id="34c41-110">Przykład 1. Ustaw</span><span class="sxs-lookup"><span data-stu-id="34c41-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="34c41-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34c41-111">PARAMETERS</span></span>

### <span data-ttu-id="34c41-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="34c41-112">-BackendPort</span></span>
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

### <span data-ttu-id="34c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c41-113">-DefaultProfile</span></span>
<span data-ttu-id="34c41-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34c41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c41-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="34c41-115">-EnableFloatingIP</span></span>
<span data-ttu-id="34c41-116">Konfiguruje punkt końcowy maszyny wirtualnej dla funkcji przestawnego adresu IP wymaganej do skonfigurowania grupy dostępności usługi SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="34c41-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="34c41-117">To ustawienie jest wymagane w przypadku korzystania z grup dostępności usługi SQL AlwaysOn w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="34c41-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="34c41-118">Po utworzeniu punktu końcowego nie można zmienić tego ustawienia.</span><span class="sxs-lookup"><span data-stu-id="34c41-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="34c41-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="34c41-119">-EnableTcpReset</span></span>
<span data-ttu-id="34c41-120">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="34c41-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="34c41-121">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="34c41-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="34c41-122">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="34c41-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="34c41-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34c41-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="34c41-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="34c41-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="34c41-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="34c41-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="34c41-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="34c41-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="34c41-127">Limit czasu dla bezczynnych połączeń TCP.</span><span class="sxs-lookup"><span data-stu-id="34c41-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="34c41-128">Wartość można ustawić między 4 a 30 minutami.</span><span class="sxs-lookup"><span data-stu-id="34c41-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="34c41-129">Wartość domyślna to 4 minuty.</span><span class="sxs-lookup"><span data-stu-id="34c41-129">The default value is 4 minutes.</span></span> <span data-ttu-id="34c41-130">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="34c41-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="34c41-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34c41-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="34c41-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34c41-132">-Name</span></span>
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

### <span data-ttu-id="34c41-133">— Protokół</span><span class="sxs-lookup"><span data-stu-id="34c41-133">-Protocol</span></span>
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

### <span data-ttu-id="34c41-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34c41-134">-Confirm</span></span>
<span data-ttu-id="34c41-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34c41-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c41-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c41-136">-WhatIf</span></span>
<span data-ttu-id="34c41-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34c41-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34c41-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34c41-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c41-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c41-139">CommonParameters</span></span>
<span data-ttu-id="34c41-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c41-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c41-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c41-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c41-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34c41-142">INPUTS</span></span>

### <span data-ttu-id="34c41-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34c41-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="34c41-144">System.String</span><span class="sxs-lookup"><span data-stu-id="34c41-144">System.String</span></span>

### <span data-ttu-id="34c41-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="34c41-145">System.Int32</span></span>

### <span data-ttu-id="34c41-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34c41-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="34c41-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34c41-147">OUTPUTS</span></span>

### <span data-ttu-id="34c41-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34c41-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="34c41-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34c41-149">NOTES</span></span>

## <span data-ttu-id="34c41-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34c41-150">RELATED LINKS</span></span>

[<span data-ttu-id="34c41-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="34c41-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="34c41-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="34c41-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="34c41-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="34c41-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="34c41-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="34c41-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
