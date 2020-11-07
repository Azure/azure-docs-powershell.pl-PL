---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: fad24c7cb9b6146ecb5fa1f0c2c21e1f2c0adbf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718155"
---
# <span data-ttu-id="e63ec-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e63ec-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e63ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e63ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e63ec-103">Tworzy konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e63ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e63ec-104">SYNTAX</span></span>

### <span data-ttu-id="e63ec-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e63ec-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e63ec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e63ec-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e63ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e63ec-107">DESCRIPTION</span></span>
<span data-ttu-id="e63ec-108">Polecenie cmdlet **New-AzureRmLoadBalancerRuleConfig** tworzy konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e63ec-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e63ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e63ec-109">EXAMPLES</span></span>

### <span data-ttu-id="e63ec-110">1: Tworzenie konfiguracji reguły dla modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e63ec-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="e63ec-111">Pierwsze trzy polecenia konfigurują publiczny adres IP, fronton i sondę dla konfiguracji reguły w z poleceniu z dalej.</span><span class="sxs-lookup"><span data-stu-id="e63ec-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="e63ec-112">Polecenie Dalej powoduje utworzenie nowej reguły o nazwie MyLBrule z określonymi specyfikacjami.</span><span class="sxs-lookup"><span data-stu-id="e63ec-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="e63ec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e63ec-113">PARAMETERS</span></span>

### <span data-ttu-id="e63ec-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e63ec-114">-BackendAddressPool</span></span>
<span data-ttu-id="e63ec-115">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e63ec-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="e63ec-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e63ec-118">-BackendPort</span></span>
<span data-ttu-id="e63ec-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-120">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="e63ec-120">-DisableOutboundSNAT</span></span>
<span data-ttu-id="e63ec-121">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-121">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="e63ec-122">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e63ec-122">-EnableFloatingIP</span></span>
<span data-ttu-id="e63ec-123">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="e63ec-123">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e63ec-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e63ec-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e63ec-125">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-125">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e63ec-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e63ec-127">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="e63ec-127">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e63ec-128">-FrontendPort</span></span>
<span data-ttu-id="e63ec-129">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-129">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e63ec-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e63ec-131">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-132">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="e63ec-132">-LoadDistribution</span></span>
<span data-ttu-id="e63ec-133">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-133">Specifies a load distribution.</span></span>
<span data-ttu-id="e63ec-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e63ec-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63ec-135">Domyślne</span><span class="sxs-lookup"><span data-stu-id="e63ec-135">Default</span></span>
- <span data-ttu-id="e63ec-136">SourceIP</span><span class="sxs-lookup"><span data-stu-id="e63ec-136">SourceIP</span></span>
- <span data-ttu-id="e63ec-137">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="e63ec-137">SourceIPProtocol</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e63ec-138">-Name</span></span>
<span data-ttu-id="e63ec-139">Określa nazwę reguły równoważenia obciążenia tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e63ec-139">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e63ec-140">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="e63ec-140">-Probe</span></span>
<span data-ttu-id="e63ec-141">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-141">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-142">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e63ec-142">-ProbeId</span></span>
<span data-ttu-id="e63ec-143">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-143">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-144">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e63ec-144">-Protocol</span></span>
<span data-ttu-id="e63ec-145">Określa protokół zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e63ec-145">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="e63ec-146">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="e63ec-146">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63ec-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63ec-147">-DefaultProfile</span></span>
<span data-ttu-id="e63ec-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e63ec-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e63ec-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63ec-149">CommonParameters</span></span>
<span data-ttu-id="e63ec-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e63ec-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63ec-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63ec-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63ec-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e63ec-152">INPUTS</span></span>

## <span data-ttu-id="e63ec-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e63ec-153">OUTPUTS</span></span>

### <span data-ttu-id="e63ec-154">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="e63ec-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="e63ec-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e63ec-155">NOTES</span></span>

## <span data-ttu-id="e63ec-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e63ec-156">RELATED LINKS</span></span>

[<span data-ttu-id="e63ec-157">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e63ec-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e63ec-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e63ec-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e63ec-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e63ec-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e63ec-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e63ec-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


