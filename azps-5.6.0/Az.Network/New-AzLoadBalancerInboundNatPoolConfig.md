---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 08ee19176c05e348f6af5b9c87aeeef8781336a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967802"
---
# <span data-ttu-id="15354-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="15354-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="15354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15354-102">SYNOPSIS</span></span>
<span data-ttu-id="15354-103">Tworzy konfigurację puli nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="15354-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="15354-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15354-104">SYNTAX</span></span>

### <span data-ttu-id="15354-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="15354-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15354-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15354-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15354-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="15354-107">DESCRIPTION</span></span>
<span data-ttu-id="15354-108">Polecenie **cmdlet New-AzLoadBalancerInboundNatPoolConfig** tworzy konfigurację puli nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="15354-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="15354-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15354-109">EXAMPLES</span></span>

### <span data-ttu-id="15354-110">Przykład 1. Nowy</span><span class="sxs-lookup"><span data-stu-id="15354-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="15354-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15354-111">PARAMETERS</span></span>

### <span data-ttu-id="15354-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="15354-112">-BackendPort</span></span>
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

### <span data-ttu-id="15354-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15354-113">-DefaultProfile</span></span>
<span data-ttu-id="15354-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15354-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15354-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="15354-115">-EnableFloatingIP</span></span>
<span data-ttu-id="15354-116">Konfiguruje punkt końcowy maszyny wirtualnej dla funkcji przestawnego adresu IP wymaganej do skonfigurowania grupy dostępności usługi SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="15354-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="15354-117">To ustawienie jest wymagane w przypadku korzystania z grup dostępności usługi SQL AlwaysOn w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="15354-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="15354-118">Po utworzeniu punktu końcowego nie można zmienić tego ustawienia.</span><span class="sxs-lookup"><span data-stu-id="15354-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="15354-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="15354-119">-EnableTcpReset</span></span>
<span data-ttu-id="15354-120">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="15354-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="15354-121">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="15354-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="15354-122">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="15354-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="15354-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="15354-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="15354-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="15354-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="15354-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="15354-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="15354-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="15354-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="15354-127">Limit czasu dla bezczynnych połączeń TCP.</span><span class="sxs-lookup"><span data-stu-id="15354-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="15354-128">Wartość można ustawić między 4 a 30 minutami.</span><span class="sxs-lookup"><span data-stu-id="15354-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="15354-129">Wartość domyślna to 4 minuty.</span><span class="sxs-lookup"><span data-stu-id="15354-129">The default value is 4 minutes.</span></span> <span data-ttu-id="15354-130">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="15354-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="15354-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="15354-131">-Name</span></span>
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

### <span data-ttu-id="15354-132">— Protokół</span><span class="sxs-lookup"><span data-stu-id="15354-132">-Protocol</span></span>
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

### <span data-ttu-id="15354-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15354-133">-Confirm</span></span>
<span data-ttu-id="15354-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="15354-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15354-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15354-135">-WhatIf</span></span>
<span data-ttu-id="15354-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15354-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15354-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="15354-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15354-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15354-138">CommonParameters</span></span>
<span data-ttu-id="15354-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15354-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15354-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15354-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15354-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15354-141">INPUTS</span></span>

### <span data-ttu-id="15354-142">System.String</span><span class="sxs-lookup"><span data-stu-id="15354-142">System.String</span></span>

### <span data-ttu-id="15354-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="15354-143">System.Int32</span></span>

### <span data-ttu-id="15354-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15354-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="15354-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15354-145">OUTPUTS</span></span>

### <span data-ttu-id="15354-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="15354-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="15354-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15354-147">NOTES</span></span>

## <span data-ttu-id="15354-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15354-148">RELATED LINKS</span></span>

[<span data-ttu-id="15354-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="15354-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="15354-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="15354-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="15354-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="15354-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="15354-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="15354-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
