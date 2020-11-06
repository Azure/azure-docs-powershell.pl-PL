---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c7d0d5879b4c0ca7ee92a9f22d062241e1cb89a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545004"
---
# <span data-ttu-id="4951f-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4951f-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4951f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4951f-102">SYNOPSIS</span></span>
<span data-ttu-id="4951f-103">Ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4951f-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4951f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4951f-104">SYNTAX</span></span>

### <span data-ttu-id="4951f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4951f-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4951f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4951f-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4951f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4951f-107">DESCRIPTION</span></span>
<span data-ttu-id="4951f-108">Polecenie cmdlet **Set-AzureRmLoadBalancerInboundNatRuleConfig** ustawia konfigurację reguł translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4951f-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4951f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4951f-109">EXAMPLES</span></span>

### <span data-ttu-id="4951f-110">Przykład 1: modyfikowanie konfiguracji reguły NAT dla ruchu przychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4951f-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="4951f-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="4951f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4951f-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerInboundNatRuleConfig, które powoduje dodanie do niego konfiguracji przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="4951f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="4951f-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia **wartość Set-AzureRmLoadBalancerInboundNatRuleConfig** , która zapisuje i aktualizuje konfigurację reguły przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="4951f-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="4951f-114">Zauważ, że konfiguracja reguły została ustawiona bez włączania przestawnego adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="4951f-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="4951f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4951f-115">PARAMETERS</span></span>

### <span data-ttu-id="4951f-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4951f-116">-BackendPort</span></span>
<span data-ttu-id="4951f-117">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="4951f-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="4951f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4951f-118">-DefaultProfile</span></span>
<span data-ttu-id="4951f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4951f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4951f-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4951f-120">-EnableFloatingIP</span></span>
<span data-ttu-id="4951f-121">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="4951f-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4951f-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4951f-122">-EnableTcpReset</span></span>
<span data-ttu-id="4951f-123">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="4951f-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4951f-124">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="4951f-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4951f-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4951f-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4951f-126">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="4951f-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="4951f-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4951f-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4951f-128">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="4951f-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="4951f-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4951f-129">-FrontendPort</span></span>
<span data-ttu-id="4951f-130">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4951f-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4951f-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4951f-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4951f-132">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4951f-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="4951f-133">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4951f-133">-LoadBalancer</span></span>
<span data-ttu-id="4951f-134">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4951f-134">Specifies a load balancer.</span></span>
<span data-ttu-id="4951f-135">To polecenie cmdlet ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4951f-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4951f-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4951f-136">-Name</span></span>
<span data-ttu-id="4951f-137">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="4951f-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="4951f-138">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="4951f-138">-Protocol</span></span>
<span data-ttu-id="4951f-139">Określa protokół zgodny z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="4951f-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="4951f-140">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="4951f-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="4951f-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4951f-141">-Confirm</span></span>
<span data-ttu-id="4951f-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4951f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4951f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4951f-143">-WhatIf</span></span>
<span data-ttu-id="4951f-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4951f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4951f-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4951f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4951f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4951f-146">CommonParameters</span></span>
<span data-ttu-id="4951f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4951f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4951f-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4951f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4951f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4951f-149">INPUTS</span></span>

### <span data-ttu-id="4951f-150">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4951f-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4951f-151">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4951f-151">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="4951f-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4951f-152">OUTPUTS</span></span>

### <span data-ttu-id="4951f-153">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4951f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4951f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4951f-154">NOTES</span></span>

## <span data-ttu-id="4951f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4951f-155">RELATED LINKS</span></span>

[<span data-ttu-id="4951f-156">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4951f-156">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4951f-157">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4951f-157">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4951f-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4951f-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4951f-159">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4951f-159">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4951f-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4951f-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


