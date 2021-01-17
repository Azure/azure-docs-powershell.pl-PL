---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365589"
---
# <span data-ttu-id="b6504-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6504-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b6504-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6504-102">SYNOPSIS</span></span>
<span data-ttu-id="b6504-103">Dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6504-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b6504-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6504-104">SYNTAX</span></span>

### <span data-ttu-id="b6504-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6504-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6504-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6504-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6504-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b6504-107">DESCRIPTION</span></span>
<span data-ttu-id="b6504-108">Polecenie cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** umożliwia dodanie konfiguracji reguł translacji adresów sieciowych (NAT) do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6504-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b6504-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6504-109">EXAMPLES</span></span>

### <span data-ttu-id="b6504-110">Przykład 1: Dodawanie konfiguracji reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b6504-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="b6504-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyloadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="b6504-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b6504-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzLoadBalancerInboundNatRuleConfig**, które dodaje konfigurację reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6504-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="b6504-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6504-113">PARAMETERS</span></span>

### <span data-ttu-id="b6504-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b6504-114">-BackendPort</span></span>
<span data-ttu-id="b6504-115">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="b6504-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b6504-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6504-116">-DefaultProfile</span></span>
<span data-ttu-id="b6504-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6504-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6504-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b6504-118">-EnableFloatingIP</span></span>
<span data-ttu-id="b6504-119">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="b6504-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b6504-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b6504-120">-EnableTcpReset</span></span>
<span data-ttu-id="b6504-121">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="b6504-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b6504-122">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="b6504-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b6504-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6504-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b6504-124">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="b6504-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b6504-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6504-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b6504-126">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b6504-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b6504-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b6504-127">-FrontendPort</span></span>
<span data-ttu-id="b6504-128">Określa port frontonu zgodny z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="b6504-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b6504-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6504-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b6504-130">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6504-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b6504-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b6504-131">-LoadBalancer</span></span>
<span data-ttu-id="b6504-132">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="b6504-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b6504-133">To polecenie cmdlet dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b6504-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6504-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6504-134">-Name</span></span>
<span data-ttu-id="b6504-135">Określa nazwę konfiguracji przychodzącej reguły NAT do dodania.</span><span class="sxs-lookup"><span data-stu-id="b6504-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="b6504-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b6504-136">-Protocol</span></span>
<span data-ttu-id="b6504-137">Określa protokół zgodny z regułą ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="b6504-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="b6504-138">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="b6504-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b6504-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6504-139">-Confirm</span></span>
<span data-ttu-id="b6504-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6504-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6504-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6504-141">-WhatIf</span></span>
<span data-ttu-id="b6504-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6504-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6504-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6504-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6504-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6504-144">CommonParameters</span></span>
<span data-ttu-id="b6504-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6504-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6504-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6504-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6504-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6504-147">INPUTS</span></span>

### <span data-ttu-id="b6504-148">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6504-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b6504-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b6504-149">System.String</span></span>

### <span data-ttu-id="b6504-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b6504-150">System.Int32</span></span>

### <span data-ttu-id="b6504-151">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6504-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b6504-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6504-152">OUTPUTS</span></span>

### <span data-ttu-id="b6504-153">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6504-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b6504-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6504-154">NOTES</span></span>

## <span data-ttu-id="b6504-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6504-155">RELATED LINKS</span></span>

[<span data-ttu-id="b6504-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6504-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b6504-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6504-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6504-158">Nowe — AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6504-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6504-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6504-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6504-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6504-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="b6504-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6504-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


