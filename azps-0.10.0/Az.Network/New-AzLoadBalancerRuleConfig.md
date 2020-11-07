---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890481"
---
# <span data-ttu-id="99b7b-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99b7b-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="99b7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="99b7b-103">Tworzy konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="99b7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99b7b-104">SYNTAX</span></span>

### <span data-ttu-id="99b7b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="99b7b-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b7b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="99b7b-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99b7b-107">DESCRIPTION</span></span>
<span data-ttu-id="99b7b-108">Polecenie cmdlet **New-AzLoadBalancerRuleConfig** tworzy konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99b7b-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="99b7b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99b7b-109">EXAMPLES</span></span>

### <span data-ttu-id="99b7b-110">1: Tworzenie konfiguracji reguły dla modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="99b7b-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="99b7b-111">Pierwsze trzy polecenia konfigurują publiczny adres IP, fronton i sondę dla konfiguracji reguły w z poleceniu z dalej.</span><span class="sxs-lookup"><span data-stu-id="99b7b-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="99b7b-112">Polecenie Dalej powoduje utworzenie nowej reguły o nazwie MyLBrule z określonymi specyfikacjami.</span><span class="sxs-lookup"><span data-stu-id="99b7b-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="99b7b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99b7b-113">PARAMETERS</span></span>

### <span data-ttu-id="99b7b-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="99b7b-114">-BackendAddressPool</span></span>
<span data-ttu-id="99b7b-115">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="99b7b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="99b7b-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="99b7b-118">-BackendPort</span></span>
<span data-ttu-id="99b7b-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b7b-120">-DefaultProfile</span></span>
<span data-ttu-id="99b7b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99b7b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b7b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="99b7b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="99b7b-123">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="99b7b-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="99b7b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="99b7b-125">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="99b7b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b7b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="99b7b-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99b7b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="99b7b-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="99b7b-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="99b7b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="99b7b-130">-FrontendPort</span></span>
<span data-ttu-id="99b7b-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="99b7b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="99b7b-133">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="99b7b-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="99b7b-134">-LoadDistribution</span></span>
<span data-ttu-id="99b7b-135">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-135">Specifies a load distribution.</span></span>
<span data-ttu-id="99b7b-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="99b7b-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99b7b-137">Domyślne</span><span class="sxs-lookup"><span data-stu-id="99b7b-137">Default</span></span>
- <span data-ttu-id="99b7b-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="99b7b-138">SourceIP</span></span>
- <span data-ttu-id="99b7b-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="99b7b-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="99b7b-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99b7b-140">-Name</span></span>
<span data-ttu-id="99b7b-141">Określa nazwę reguły równoważenia obciążenia tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b7b-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="99b7b-142">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="99b7b-142">-Probe</span></span>
<span data-ttu-id="99b7b-143">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="99b7b-144">-ProbeId</span></span>
<span data-ttu-id="99b7b-145">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="99b7b-146">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="99b7b-146">-Protocol</span></span>
<span data-ttu-id="99b7b-147">Określa protokół zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99b7b-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="99b7b-148">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="99b7b-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="99b7b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b7b-149">CommonParameters</span></span>
<span data-ttu-id="99b7b-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b7b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b7b-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b7b-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b7b-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b7b-152">INPUTS</span></span>

## <span data-ttu-id="99b7b-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99b7b-153">OUTPUTS</span></span>

### <span data-ttu-id="99b7b-154">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="99b7b-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="99b7b-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99b7b-155">NOTES</span></span>

## <span data-ttu-id="99b7b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99b7b-156">RELATED LINKS</span></span>

[<span data-ttu-id="99b7b-157">Dodaj-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99b7b-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="99b7b-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99b7b-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="99b7b-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99b7b-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="99b7b-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99b7b-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


