---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892786"
---
# <span data-ttu-id="a49b1-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a49b1-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a49b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a49b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a49b1-103">Ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a49b1-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a49b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a49b1-104">SYNTAX</span></span>

### <span data-ttu-id="a49b1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a49b1-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a49b1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a49b1-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a49b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a49b1-107">DESCRIPTION</span></span>
<span data-ttu-id="a49b1-108">Polecenie cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** ustawia konfigurację reguł translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a49b1-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a49b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a49b1-109">EXAMPLES</span></span>

### <span data-ttu-id="a49b1-110">Przykład 1: modyfikowanie konfiguracji reguły NAT dla ruchu przychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a49b1-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="a49b1-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="a49b1-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="a49b1-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerInboundNatRuleConfig, które powoduje dodanie do niego konfiguracji przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="a49b1-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="a49b1-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia **wartość Set-AzLoadBalancerInboundNatRuleConfig** , która zapisuje i aktualizuje konfigurację reguły przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="a49b1-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="a49b1-114">Zauważ, że konfiguracja reguły została ustawiona bez włączania przestawnego adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="a49b1-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="a49b1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a49b1-115">PARAMETERS</span></span>

### <span data-ttu-id="a49b1-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a49b1-116">-BackendPort</span></span>
<span data-ttu-id="a49b1-117">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="a49b1-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a49b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49b1-118">-DefaultProfile</span></span>
<span data-ttu-id="a49b1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a49b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a49b1-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a49b1-120">-EnableFloatingIP</span></span>
<span data-ttu-id="a49b1-121">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="a49b1-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a49b1-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a49b1-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a49b1-123">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="a49b1-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a49b1-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a49b1-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a49b1-125">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="a49b1-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a49b1-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a49b1-126">-FrontendPort</span></span>
<span data-ttu-id="a49b1-127">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a49b1-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a49b1-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a49b1-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a49b1-129">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a49b1-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a49b1-130">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a49b1-130">-LoadBalancer</span></span>
<span data-ttu-id="a49b1-131">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a49b1-131">Specifies a load balancer.</span></span>
<span data-ttu-id="a49b1-132">To polecenie cmdlet ustawia konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a49b1-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a49b1-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a49b1-133">-Name</span></span>
<span data-ttu-id="a49b1-134">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="a49b1-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a49b1-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a49b1-135">-Protocol</span></span>
<span data-ttu-id="a49b1-136">Określa protokół zgodny z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="a49b1-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="a49b1-137">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="a49b1-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49b1-138">CommonParameters</span></span>
<span data-ttu-id="a49b1-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49b1-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a49b1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49b1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a49b1-141">INPUTS</span></span>

### <span data-ttu-id="a49b1-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a49b1-142">PSLoadBalancer</span></span>
<span data-ttu-id="a49b1-143">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="a49b1-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a49b1-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a49b1-144">OUTPUTS</span></span>

### <span data-ttu-id="a49b1-145">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a49b1-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a49b1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a49b1-146">NOTES</span></span>

## <span data-ttu-id="a49b1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a49b1-147">RELATED LINKS</span></span>

[<span data-ttu-id="a49b1-148">Dodaj-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a49b1-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a49b1-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a49b1-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a49b1-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a49b1-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a49b1-151">Nowe — AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a49b1-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a49b1-152">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a49b1-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


