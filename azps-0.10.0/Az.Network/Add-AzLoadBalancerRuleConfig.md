---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890965"
---
# <span data-ttu-id="c7967-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7967-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c7967-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7967-102">SYNOPSIS</span></span>
<span data-ttu-id="c7967-103">Umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="c7967-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7967-104">SYNTAX</span></span>

### <span data-ttu-id="c7967-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7967-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7967-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7967-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7967-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c7967-107">DESCRIPTION</span></span>
<span data-ttu-id="c7967-108">Polecenie cmdlet **Add-AzLoadBalancerRuleConfig** umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c7967-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c7967-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7967-109">EXAMPLES</span></span>

### <span data-ttu-id="c7967-110">Przykład 1. Dodawanie konfiguracji reguły do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c7967-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="c7967-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="c7967-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="c7967-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzLoadBalancerRuleConfig** , które dodaje konfigurację reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="c7967-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="c7967-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7967-113">PARAMETERS</span></span>

### <span data-ttu-id="c7967-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c7967-114">-BackendAddressPool</span></span>
<span data-ttu-id="c7967-115">Określa pulę adresów zaplecza, która ma zostać skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c7967-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="c7967-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c7967-118">-BackendPort</span></span>
<span data-ttu-id="c7967-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7967-120">-DefaultProfile</span></span>
<span data-ttu-id="c7967-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7967-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7967-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c7967-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c7967-123">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c7967-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c7967-124">-EnableFloatingIP</span></span>
<span data-ttu-id="c7967-125">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="c7967-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c7967-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7967-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c7967-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7967-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c7967-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="c7967-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c7967-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7967-130">-FrontendPort</span></span>
<span data-ttu-id="c7967-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c7967-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c7967-133">Określa długość czasu (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="c7967-134">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c7967-134">-LoadBalancer</span></span>
<span data-ttu-id="c7967-135">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="c7967-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c7967-136">To polecenie cmdlet umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c7967-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7967-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c7967-137">-LoadDistribution</span></span>
<span data-ttu-id="c7967-138">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="c7967-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7967-139">-Name</span></span>
<span data-ttu-id="c7967-140">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-141">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="c7967-141">-Probe</span></span>
<span data-ttu-id="c7967-142">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c7967-143">-ProbeId</span></span>
<span data-ttu-id="c7967-144">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7967-145">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c7967-145">-Protocol</span></span>
<span data-ttu-id="c7967-146">Specfies protokół zgodny z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c7967-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="c7967-147">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="c7967-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c7967-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7967-148">CommonParameters</span></span>
<span data-ttu-id="c7967-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7967-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7967-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7967-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7967-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7967-151">INPUTS</span></span>

### <span data-ttu-id="c7967-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7967-152">PSLoadBalancer</span></span>
<span data-ttu-id="c7967-153">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="c7967-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c7967-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7967-154">OUTPUTS</span></span>

### <span data-ttu-id="c7967-155">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7967-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c7967-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7967-156">NOTES</span></span>

## <span data-ttu-id="c7967-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7967-157">RELATED LINKS</span></span>

[<span data-ttu-id="c7967-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7967-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c7967-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7967-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7967-160">Nowe — AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7967-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7967-161">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7967-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7967-162">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7967-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


