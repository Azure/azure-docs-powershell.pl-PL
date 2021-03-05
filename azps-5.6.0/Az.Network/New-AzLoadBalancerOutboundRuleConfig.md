---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50f3c3a02410adda37b26c88cd5196c4ae232f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971905"
---
# <span data-ttu-id="03f58-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03f58-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="03f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f58-102">SYNOPSIS</span></span>
<span data-ttu-id="03f58-103">Tworzy konfigurację reguły ruchu wychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03f58-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="03f58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03f58-104">SYNTAX</span></span>

### <span data-ttu-id="03f58-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="03f58-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03f58-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03f58-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03f58-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03f58-107">DESCRIPTION</span></span>
<span data-ttu-id="03f58-108">Polecenie **cmdlet New-AzLoadBalancerOutboundRuleConfig** tworzy konfigurację reguły ruchu wychodzącego dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03f58-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="03f58-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03f58-109">EXAMPLES</span></span>

### <span data-ttu-id="03f58-110">Przykład 1. Tworzenie konfiguracji reguły ruchu wychodzącego dla równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="03f58-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="03f58-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje go w zmiennej $publicip adresowej.</span><span class="sxs-lookup"><span data-stu-id="03f58-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="03f58-112">Drugie polecenie tworzy konfigurację frontonu adresu IP o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w programie $publicip, a następnie przechowuje ją w $frontend danych.</span><span class="sxs-lookup"><span data-stu-id="03f58-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="03f58-113">Trzecie polecenie tworzy konfigurację puli adresów zaplecza o nazwie BackendAddressPool01, a następnie zapisuje ją w zmiennej $backend adresowej.</span><span class="sxs-lookup"><span data-stu-id="03f58-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="03f58-114">Czwarte polecenie tworzy konfigurację reguł ruchu wychodzącego o nazwie MyOutboundRule, używając obiektów frontoronu i back-end w $frontend i $backend.</span><span class="sxs-lookup"><span data-stu-id="03f58-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="03f58-115">Parametry *Protocol* *,FrontendIPConfiguration* i *BackendAddressPool* są wymagane do utworzenia konfiguracji reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="03f58-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="03f58-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03f58-116">Example 2</span></span>

<span data-ttu-id="03f58-117">Tworzy konfigurację reguły ruchu wychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03f58-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="03f58-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="03f58-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="03f58-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03f58-119">PARAMETERS</span></span>

### <span data-ttu-id="03f58-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="03f58-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="03f58-121">Liczba portów wychodzących, które mają być używane na pasku nat.</span><span class="sxs-lookup"><span data-stu-id="03f58-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="03f58-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="03f58-122">-BackendAddressPool</span></span>
<span data-ttu-id="03f58-123">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="03f58-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="03f58-124">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="03f58-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f58-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="03f58-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="03f58-126">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="03f58-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="03f58-127">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="03f58-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f58-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f58-128">-DefaultProfile</span></span>
<span data-ttu-id="03f58-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03f58-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f58-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="03f58-130">-EnableTcpReset</span></span>
<span data-ttu-id="03f58-131">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="03f58-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="03f58-132">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="03f58-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="03f58-133">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="03f58-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="03f58-134">Adresy IP frontendu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="03f58-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f58-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="03f58-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="03f58-136">Limit czasu dla bezczynne połączenie TCP</span><span class="sxs-lookup"><span data-stu-id="03f58-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="03f58-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03f58-137">-Name</span></span>
<span data-ttu-id="03f58-138">Nazwa reguły wychodzącej.</span><span class="sxs-lookup"><span data-stu-id="03f58-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="03f58-139">— Protokół</span><span class="sxs-lookup"><span data-stu-id="03f58-139">-Protocol</span></span>
<span data-ttu-id="03f58-140">Protokół — TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="03f58-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="03f58-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03f58-141">-Confirm</span></span>
<span data-ttu-id="03f58-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03f58-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03f58-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03f58-143">-WhatIf</span></span>
<span data-ttu-id="03f58-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03f58-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03f58-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03f58-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03f58-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f58-146">CommonParameters</span></span>
<span data-ttu-id="03f58-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f58-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f58-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f58-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f58-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03f58-149">INPUTS</span></span>

### <span data-ttu-id="03f58-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="03f58-150">System.Int32</span></span>

### <span data-ttu-id="03f58-151">System.String</span><span class="sxs-lookup"><span data-stu-id="03f58-151">System.String</span></span>

### <span data-ttu-id="03f58-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="03f58-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="03f58-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="03f58-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="03f58-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03f58-154">OUTPUTS</span></span>

### <span data-ttu-id="03f58-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="03f58-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="03f58-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03f58-156">NOTES</span></span>

## <span data-ttu-id="03f58-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03f58-157">RELATED LINKS</span></span>

[<span data-ttu-id="03f58-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03f58-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="03f58-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03f58-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="03f58-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03f58-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="03f58-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03f58-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
