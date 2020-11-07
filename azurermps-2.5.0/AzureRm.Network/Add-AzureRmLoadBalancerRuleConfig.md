---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898902"
---
# <span data-ttu-id="7dd7b-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dd7b-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7dd7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd7b-103">Umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dd7b-104">SYNTAX</span></span>

### <span data-ttu-id="7dd7b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7dd7b-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dd7b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7dd7b-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7dd7b-107">DESCRIPTION</span></span>
<span data-ttu-id="7dd7b-108">Polecenie cmdlet **Add-AzureRmLoadBalancerRuleConfig** umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7dd7b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dd7b-109">EXAMPLES</span></span>

### <span data-ttu-id="7dd7b-110">Przykład 1. Dodawanie konfiguracji reguły do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7dd7b-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="7dd7b-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="7dd7b-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzureRmLoadBalancerRuleConfig** , które dodaje konfigurację reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="7dd7b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dd7b-113">PARAMETERS</span></span>

### <span data-ttu-id="7dd7b-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7dd7b-114">-BackendAddressPool</span></span>
<span data-ttu-id="7dd7b-115">Określa pulę adresów zaplecza, która ma zostać skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7dd7b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="7dd7b-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7dd7b-118">-BackendPort</span></span>
<span data-ttu-id="7dd7b-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd7b-120">-DefaultProfile</span></span>
<span data-ttu-id="7dd7b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd7b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7dd7b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7dd7b-123">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7dd7b-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7dd7b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="7dd7b-125">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7dd7b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7dd7b-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7dd7b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7dd7b-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7dd7b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7dd7b-130">-FrontendPort</span></span>
<span data-ttu-id="7dd7b-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7dd7b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7dd7b-133">Określa długość czasu (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="7dd7b-134">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7dd7b-134">-LoadBalancer</span></span>
<span data-ttu-id="7dd7b-135">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="7dd7b-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7dd7b-136">To polecenie cmdlet umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7dd7b-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7dd7b-137">-LoadDistribution</span></span>
<span data-ttu-id="7dd7b-138">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="7dd7b-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7dd7b-139">-Name</span></span>
<span data-ttu-id="7dd7b-140">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-141">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="7dd7b-141">-Probe</span></span>
<span data-ttu-id="7dd7b-142">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="7dd7b-143">-ProbeId</span></span>
<span data-ttu-id="7dd7b-144">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7dd7b-145">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7dd7b-145">-Protocol</span></span>
<span data-ttu-id="7dd7b-146">Specfies protokół zgodny z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="7dd7b-147">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7dd7b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd7b-148">CommonParameters</span></span>
<span data-ttu-id="7dd7b-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd7b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd7b-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd7b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd7b-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dd7b-151">INPUTS</span></span>

### <span data-ttu-id="7dd7b-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7dd7b-152">PSLoadBalancer</span></span>
<span data-ttu-id="7dd7b-153">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="7dd7b-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7dd7b-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dd7b-154">OUTPUTS</span></span>

### <span data-ttu-id="7dd7b-155">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7dd7b-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7dd7b-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dd7b-156">NOTES</span></span>

## <span data-ttu-id="7dd7b-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dd7b-157">RELATED LINKS</span></span>

[<span data-ttu-id="7dd7b-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7dd7b-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="7dd7b-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dd7b-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7dd7b-160">Nowe — AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dd7b-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7dd7b-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dd7b-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7dd7b-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dd7b-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


