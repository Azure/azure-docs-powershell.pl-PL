---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: a089f5b9e27a6fd7458dc02937a8bb75d1cbbb02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894397"
---
# <span data-ttu-id="ca76b-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca76b-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="ca76b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca76b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca76b-103">Umożliwia utworzenie konfiguracji reguły ruchu wychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ca76b-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ca76b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca76b-104">SYNTAX</span></span>

### <span data-ttu-id="ca76b-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca76b-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca76b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca76b-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca76b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ca76b-107">DESCRIPTION</span></span>
<span data-ttu-id="ca76b-108">Polecenie cmdlet **New-AzLoadBalancerOutboundRuleConfig** tworzy konfigurację reguły ruchu wychodzącego dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca76b-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ca76b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca76b-109">EXAMPLES</span></span>

### <span data-ttu-id="ca76b-110">Przykład 1. Tworzenie konfiguracji reguły ruchu wychodzącego dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="ca76b-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="ca76b-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="ca76b-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="ca76b-112">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip, a następnie zapisuje ją w zmiennej $frontend.</span><span class="sxs-lookup"><span data-stu-id="ca76b-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="ca76b-113">Trzecie polecenie tworzy konfigurację puli adresów zaplecza o nazwie BackendAddressPool01, a następnie zapisuje ją w zmiennej $backend.</span><span class="sxs-lookup"><span data-stu-id="ca76b-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="ca76b-114">Czwarte polecenie tworzy konfigurację reguły ruchu wychodzącego o nazwie MyOutboundRule, używając obiektów frontonu i zaplecza w $frontend i $backend.</span><span class="sxs-lookup"><span data-stu-id="ca76b-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="ca76b-115">Do utworzenia konfiguracji reguły ruchu wychodzącego wymagane są wszystkie parametry *Protocol* , *FrontendIPConfiguration* i *BackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="ca76b-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="ca76b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca76b-116">PARAMETERS</span></span>

### <span data-ttu-id="ca76b-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="ca76b-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="ca76b-118">Liczba portów wychodzących, które mają być używane do obsługi translatora adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ca76b-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="ca76b-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ca76b-119">-BackendAddressPool</span></span>
<span data-ttu-id="ca76b-120">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="ca76b-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="ca76b-121">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="ca76b-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="ca76b-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ca76b-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="ca76b-123">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="ca76b-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="ca76b-124">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="ca76b-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="ca76b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca76b-125">-DefaultProfile</span></span>
<span data-ttu-id="ca76b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca76b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca76b-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ca76b-127">-EnableTcpReset</span></span>
<span data-ttu-id="ca76b-128">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="ca76b-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="ca76b-129">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="ca76b-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ca76b-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca76b-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ca76b-131">Adresy IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ca76b-131">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="ca76b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ca76b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ca76b-133">Limit czasu bezczynności połączenia TCP</span><span class="sxs-lookup"><span data-stu-id="ca76b-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="ca76b-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca76b-134">-Name</span></span>
<span data-ttu-id="ca76b-135">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="ca76b-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="ca76b-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="ca76b-136">-Protocol</span></span>
<span data-ttu-id="ca76b-137">Protocol-TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="ca76b-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="ca76b-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca76b-138">-Confirm</span></span>
<span data-ttu-id="ca76b-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca76b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca76b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca76b-140">-WhatIf</span></span>
<span data-ttu-id="ca76b-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca76b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca76b-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca76b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca76b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca76b-143">CommonParameters</span></span>
<span data-ttu-id="ca76b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca76b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca76b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca76b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca76b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca76b-146">INPUTS</span></span>

### <span data-ttu-id="ca76b-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ca76b-147">System.Int32</span></span>

### <span data-ttu-id="ca76b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ca76b-148">System.String</span></span>

### <span data-ttu-id="ca76b-149">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="ca76b-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="ca76b-150">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ca76b-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="ca76b-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca76b-151">OUTPUTS</span></span>

### <span data-ttu-id="ca76b-152">Microsoft. Azure. Commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="ca76b-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="ca76b-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca76b-153">NOTES</span></span>

## <span data-ttu-id="ca76b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca76b-154">RELATED LINKS</span></span>

[<span data-ttu-id="ca76b-155">Dodaj-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca76b-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ca76b-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca76b-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ca76b-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca76b-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ca76b-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca76b-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
