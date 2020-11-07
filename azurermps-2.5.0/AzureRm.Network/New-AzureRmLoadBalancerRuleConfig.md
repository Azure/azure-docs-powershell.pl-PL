---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899246"
---
# <span data-ttu-id="091ff-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="091ff-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="091ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="091ff-102">SYNOPSIS</span></span>
<span data-ttu-id="091ff-103">Tworzy konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="091ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="091ff-104">SYNTAX</span></span>

### <span data-ttu-id="091ff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="091ff-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="091ff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="091ff-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="091ff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="091ff-107">DESCRIPTION</span></span>
<span data-ttu-id="091ff-108">Polecenie cmdlet **New-AzureRmLoadBalancerRuleConfig** tworzy konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="091ff-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="091ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="091ff-109">EXAMPLES</span></span>

### <span data-ttu-id="091ff-110">1: Tworzenie konfiguracji reguły dla modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="091ff-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="091ff-111">Pierwsze trzy polecenia konfigurują publiczny adres IP, fronton i sondę dla konfiguracji reguły w z poleceniu z dalej.</span><span class="sxs-lookup"><span data-stu-id="091ff-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="091ff-112">Polecenie Dalej powoduje utworzenie nowej reguły o nazwie MyLBrule z określonymi specyfikacjami.</span><span class="sxs-lookup"><span data-stu-id="091ff-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="091ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="091ff-113">PARAMETERS</span></span>

### <span data-ttu-id="091ff-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="091ff-114">-BackendAddressPool</span></span>
<span data-ttu-id="091ff-115">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="091ff-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="091ff-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="091ff-118">-BackendPort</span></span>
<span data-ttu-id="091ff-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091ff-120">-DefaultProfile</span></span>
<span data-ttu-id="091ff-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="091ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="091ff-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="091ff-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="091ff-123">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="091ff-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="091ff-124">-EnableFloatingIP</span></span>
<span data-ttu-id="091ff-125">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="091ff-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="091ff-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="091ff-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="091ff-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="091ff-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="091ff-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="091ff-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="091ff-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="091ff-130">-FrontendPort</span></span>
<span data-ttu-id="091ff-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="091ff-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="091ff-133">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="091ff-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="091ff-134">-LoadDistribution</span></span>
<span data-ttu-id="091ff-135">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-135">Specifies a load distribution.</span></span>
<span data-ttu-id="091ff-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="091ff-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="091ff-137">Domyślne</span><span class="sxs-lookup"><span data-stu-id="091ff-137">Default</span></span>
- <span data-ttu-id="091ff-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="091ff-138">SourceIP</span></span>
- <span data-ttu-id="091ff-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="091ff-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="091ff-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="091ff-140">-Name</span></span>
<span data-ttu-id="091ff-141">Określa nazwę reguły równoważenia obciążenia tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="091ff-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="091ff-142">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="091ff-142">-Probe</span></span>
<span data-ttu-id="091ff-143">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="091ff-144">-ProbeId</span></span>
<span data-ttu-id="091ff-145">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="091ff-146">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="091ff-146">-Protocol</span></span>
<span data-ttu-id="091ff-147">Określa protokół zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="091ff-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="091ff-148">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="091ff-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="091ff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091ff-149">CommonParameters</span></span>
<span data-ttu-id="091ff-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091ff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091ff-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="091ff-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091ff-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="091ff-152">INPUTS</span></span>

## <span data-ttu-id="091ff-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="091ff-153">OUTPUTS</span></span>

### <span data-ttu-id="091ff-154">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="091ff-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="091ff-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="091ff-155">NOTES</span></span>

## <span data-ttu-id="091ff-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="091ff-156">RELATED LINKS</span></span>

[<span data-ttu-id="091ff-157">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="091ff-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="091ff-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="091ff-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="091ff-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="091ff-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="091ff-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="091ff-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


