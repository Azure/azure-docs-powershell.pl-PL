---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 402235f4d98b39ec78ffdc67bd0a01ab16e0400a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527878"
---
# <span data-ttu-id="c80d7-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c80d7-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c80d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c80d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c80d7-103">Dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c80d7-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c80d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c80d7-104">SYNTAX</span></span>

### <span data-ttu-id="c80d7-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c80d7-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c80d7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c80d7-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c80d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c80d7-107">DESCRIPTION</span></span>
<span data-ttu-id="c80d7-108">Polecenie cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** umożliwia dodanie konfiguracji reguł translacji adresów sieciowych (NAT) do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c80d7-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c80d7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c80d7-109">EXAMPLES</span></span>

### <span data-ttu-id="c80d7-110">Przykład 1: Dodawanie konfiguracji reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c80d7-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="c80d7-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyloadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="c80d7-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c80d7-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzureRmLoadBalancerInboundNatRuleConfig** , które dodaje konfigurację reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c80d7-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="c80d7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c80d7-113">PARAMETERS</span></span>

### <span data-ttu-id="c80d7-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c80d7-114">-BackendPort</span></span>
<span data-ttu-id="c80d7-115">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="c80d7-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="c80d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80d7-116">-DefaultProfile</span></span>
<span data-ttu-id="c80d7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c80d7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c80d7-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c80d7-118">-EnableFloatingIP</span></span>
<span data-ttu-id="c80d7-119">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="c80d7-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c80d7-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c80d7-120">-EnableTcpReset</span></span>
<span data-ttu-id="c80d7-121">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="c80d7-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c80d7-122">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="c80d7-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c80d7-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c80d7-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c80d7-124">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c80d7-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="c80d7-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c80d7-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c80d7-126">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="c80d7-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c80d7-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c80d7-127">-FrontendPort</span></span>
<span data-ttu-id="c80d7-128">Określa port frontonu zgodny z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="c80d7-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="c80d7-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c80d7-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c80d7-130">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c80d7-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c80d7-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c80d7-131">-LoadBalancer</span></span>
<span data-ttu-id="c80d7-132">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="c80d7-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c80d7-133">To polecenie cmdlet dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c80d7-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c80d7-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c80d7-134">-Name</span></span>
<span data-ttu-id="c80d7-135">Określa nazwę konfiguracji przychodzącej reguły NAT do dodania.</span><span class="sxs-lookup"><span data-stu-id="c80d7-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="c80d7-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c80d7-136">-Protocol</span></span>
<span data-ttu-id="c80d7-137">Określa protokół zgodny z regułą ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="c80d7-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="c80d7-138">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="c80d7-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c80d7-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c80d7-139">-Confirm</span></span>
<span data-ttu-id="c80d7-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c80d7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c80d7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c80d7-141">-WhatIf</span></span>
<span data-ttu-id="c80d7-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c80d7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c80d7-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c80d7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c80d7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80d7-144">CommonParameters</span></span>
<span data-ttu-id="c80d7-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80d7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80d7-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80d7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80d7-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c80d7-147">INPUTS</span></span>

### <span data-ttu-id="c80d7-148">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c80d7-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c80d7-149">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c80d7-149">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="c80d7-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c80d7-150">OUTPUTS</span></span>

### <span data-ttu-id="c80d7-151">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c80d7-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c80d7-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c80d7-152">NOTES</span></span>

## <span data-ttu-id="c80d7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c80d7-153">RELATED LINKS</span></span>

[<span data-ttu-id="c80d7-154">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c80d7-154">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c80d7-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c80d7-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c80d7-156">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c80d7-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c80d7-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c80d7-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c80d7-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c80d7-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="c80d7-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c80d7-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


