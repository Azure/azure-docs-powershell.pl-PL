---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543244"
---
# <span data-ttu-id="c24fe-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24fe-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c24fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c24fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c24fe-103">Ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c24fe-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c24fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c24fe-104">SYNTAX</span></span>

### <span data-ttu-id="c24fe-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c24fe-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c24fe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c24fe-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c24fe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c24fe-107">DESCRIPTION</span></span>
<span data-ttu-id="c24fe-108">Polecenie cmdlet **Set-AzureRmLoadBalancerInboundNatRuleConfig** ustawia konfigurację reguł translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c24fe-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c24fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c24fe-109">EXAMPLES</span></span>

### <span data-ttu-id="c24fe-110">Przykład 1: modyfikowanie konfiguracji reguły NAT dla ruchu przychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c24fe-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="c24fe-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="c24fe-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="c24fe-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerInboundNatRuleConfig, które powoduje dodanie do niego konfiguracji przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c24fe-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="c24fe-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia **wartość Set-AzureRmLoadBalancerInboundNatRuleConfig** , która zapisuje i aktualizuje konfigurację reguły przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="c24fe-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="c24fe-114">Zauważ, że konfiguracja reguły została ustawiona bez włączania przestawnego adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="c24fe-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="c24fe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c24fe-115">PARAMETERS</span></span>

### <span data-ttu-id="c24fe-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c24fe-116">-BackendPort</span></span>
<span data-ttu-id="c24fe-117">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="c24fe-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="c24fe-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c24fe-118">-EnableFloatingIP</span></span>
<span data-ttu-id="c24fe-119">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="c24fe-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c24fe-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24fe-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c24fe-121">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c24fe-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="c24fe-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c24fe-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c24fe-123">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="c24fe-123">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c24fe-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c24fe-124">-FrontendPort</span></span>
<span data-ttu-id="c24fe-125">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c24fe-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c24fe-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c24fe-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c24fe-127">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c24fe-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c24fe-128">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c24fe-128">-LoadBalancer</span></span>
<span data-ttu-id="c24fe-129">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c24fe-129">Specifies a load balancer.</span></span>
<span data-ttu-id="c24fe-130">To polecenie cmdlet ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c24fe-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c24fe-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c24fe-131">-Name</span></span>
<span data-ttu-id="c24fe-132">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="c24fe-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="c24fe-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c24fe-133">-Protocol</span></span>
<span data-ttu-id="c24fe-134">Określa protokół zgodny z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="c24fe-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="c24fe-135">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="c24fe-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c24fe-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24fe-136">-DefaultProfile</span></span>
<span data-ttu-id="c24fe-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c24fe-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24fe-138">CommonParameters</span></span>
<span data-ttu-id="c24fe-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24fe-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24fe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24fe-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c24fe-141">INPUTS</span></span>

### <span data-ttu-id="c24fe-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c24fe-142">PSLoadBalancer</span></span>
<span data-ttu-id="c24fe-143">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="c24fe-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c24fe-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c24fe-144">OUTPUTS</span></span>

### <span data-ttu-id="c24fe-145">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c24fe-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c24fe-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c24fe-146">NOTES</span></span>

## <span data-ttu-id="c24fe-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c24fe-147">RELATED LINKS</span></span>

[<span data-ttu-id="c24fe-148">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24fe-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c24fe-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c24fe-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c24fe-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24fe-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c24fe-151">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24fe-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c24fe-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24fe-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


