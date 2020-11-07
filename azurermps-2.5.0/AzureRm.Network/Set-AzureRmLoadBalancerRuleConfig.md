---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 59e20a557c0e32d35dd853a0b3ff7e619ec2a955
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898233"
---
# <span data-ttu-id="0bb61-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0bb61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bb61-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb61-103">Ustawia stan celu dla konfiguracji reguł modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bb61-104">SYNTAX</span></span>

### <span data-ttu-id="0bb61-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb61-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bb61-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0bb61-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bb61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0bb61-107">DESCRIPTION</span></span>
<span data-ttu-id="0bb61-108">Polecenie cmdlet **Set-AzureRmLoadBalancerRuleConfig** ustawia stan celu dla konfiguracji reguł modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="0bb61-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bb61-109">EXAMPLES</span></span>

### <span data-ttu-id="0bb61-110">Przykład 1: modyfikowanie konfiguracji reguły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="0bb61-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="0bb61-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="0bb61-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="0bb61-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerRuleConfig, które umożliwia dodanie reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="0bb61-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="0bb61-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia **wartość Set-AzureRmLoadBalancerRuleConfig** , która ustawia konfigurację nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="0bb61-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="0bb61-114">Zauważ, że konfiguracja nie umożliwia przestawenia adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="0bb61-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="0bb61-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bb61-115">PARAMETERS</span></span>

### <span data-ttu-id="0bb61-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0bb61-116">-BackendAddressPool</span></span>
<span data-ttu-id="0bb61-117">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0bb61-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0bb61-119">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0bb61-120">-BackendPort</span></span>
<span data-ttu-id="0bb61-121">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="0bb61-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb61-122">-DefaultProfile</span></span>
<span data-ttu-id="0bb61-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb61-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb61-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="0bb61-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="0bb61-125">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0bb61-126">-EnableFloatingIP</span></span>
<span data-ttu-id="0bb61-127">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="0bb61-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bb61-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0bb61-129">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0bb61-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0bb61-131">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="0bb61-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0bb61-132">-FrontendPort</span></span>
<span data-ttu-id="0bb61-133">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0bb61-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0bb61-135">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-136">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="0bb61-136">-LoadBalancer</span></span>
<span data-ttu-id="0bb61-137">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-137">Specifies a load balancer.</span></span>
<span data-ttu-id="0bb61-138">To polecenie cmdlet ustawia konfigurację reguły stanu celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0bb61-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0bb61-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="0bb61-139">-LoadDistribution</span></span>
<span data-ttu-id="0bb61-140">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-140">Specifies a load distribution.</span></span>
<span data-ttu-id="0bb61-141">Dopuszczalne wartości tego parametru to: SourceIP oraz SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="0bb61-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bb61-142">-Name</span></span>
<span data-ttu-id="0bb61-143">Określa nazwę modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="0bb61-144">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="0bb61-144">-Probe</span></span>
<span data-ttu-id="0bb61-145">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="0bb61-146">-ProbeId</span></span>
<span data-ttu-id="0bb61-147">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-148">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="0bb61-148">-Protocol</span></span>
<span data-ttu-id="0bb61-149">Określa protokół zgodny z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0bb61-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="0bb61-150">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="0bb61-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb61-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb61-151">CommonParameters</span></span>
<span data-ttu-id="0bb61-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb61-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb61-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb61-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb61-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bb61-154">INPUTS</span></span>

### <span data-ttu-id="0bb61-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb61-155">PSLoadBalancer</span></span>
<span data-ttu-id="0bb61-156">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="0bb61-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0bb61-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bb61-157">OUTPUTS</span></span>

### <span data-ttu-id="0bb61-158">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb61-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0bb61-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bb61-159">NOTES</span></span>

## <span data-ttu-id="0bb61-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bb61-160">RELATED LINKS</span></span>

[<span data-ttu-id="0bb61-161">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bb61-162">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bb61-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bb61-164">Nowe — AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bb61-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb61-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


