---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee0a001894570c66145ac7f75d12451df5faaab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717576"
---
# <span data-ttu-id="b6beb-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6beb-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b6beb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6beb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6beb-103">Dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6beb-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6beb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6beb-104">SYNTAX</span></span>

### <span data-ttu-id="b6beb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6beb-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6beb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6beb-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6beb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b6beb-107">DESCRIPTION</span></span>
<span data-ttu-id="b6beb-108">Polecenie cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** umożliwia dodanie konfiguracji reguł translacji adresów sieciowych (NAT) do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6beb-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b6beb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6beb-109">EXAMPLES</span></span>

### <span data-ttu-id="b6beb-110">Przykład 1: Dodawanie konfiguracji reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b6beb-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="b6beb-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyloadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="b6beb-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="b6beb-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzureRmLoadBalancerInboundNatRuleConfig** , które dodaje konfigurację reguły ruchu przychodzącego NAT do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6beb-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="b6beb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6beb-113">PARAMETERS</span></span>

### <span data-ttu-id="b6beb-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b6beb-114">-BackendPort</span></span>
<span data-ttu-id="b6beb-115">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="b6beb-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b6beb-116">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b6beb-116">-EnableFloatingIP</span></span>
<span data-ttu-id="b6beb-117">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="b6beb-117">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b6beb-118">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6beb-118">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b6beb-119">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją przychodzącej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="b6beb-119">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b6beb-120">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6beb-120">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b6beb-121">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b6beb-121">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b6beb-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b6beb-122">-FrontendPort</span></span>
<span data-ttu-id="b6beb-123">Określa port frontonu zgodny z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="b6beb-123">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b6beb-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6beb-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b6beb-125">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b6beb-125">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b6beb-126">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b6beb-126">-LoadBalancer</span></span>
<span data-ttu-id="b6beb-127">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="b6beb-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b6beb-128">To polecenie cmdlet dodaje konfigurację reguły NAT dla ruchu przychodzącego do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b6beb-128">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6beb-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6beb-129">-Name</span></span>
<span data-ttu-id="b6beb-130">Określa nazwę konfiguracji przychodzącej reguły NAT do dodania.</span><span class="sxs-lookup"><span data-stu-id="b6beb-130">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="b6beb-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b6beb-131">-Protocol</span></span>
<span data-ttu-id="b6beb-132">Określa protokół zgodny z regułą ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="b6beb-132">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="b6beb-133">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="b6beb-133">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b6beb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6beb-134">-DefaultProfile</span></span>
<span data-ttu-id="b6beb-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6beb-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6beb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6beb-136">CommonParameters</span></span>
<span data-ttu-id="b6beb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6beb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6beb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6beb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6beb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6beb-139">INPUTS</span></span>

### <span data-ttu-id="b6beb-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6beb-140">PSLoadBalancer</span></span>
<span data-ttu-id="b6beb-141">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="b6beb-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b6beb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6beb-142">OUTPUTS</span></span>

### <span data-ttu-id="b6beb-143">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6beb-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b6beb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6beb-144">NOTES</span></span>

## <span data-ttu-id="b6beb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6beb-145">RELATED LINKS</span></span>

[<span data-ttu-id="b6beb-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6beb-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b6beb-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6beb-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6beb-148">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6beb-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6beb-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6beb-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b6beb-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b6beb-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="b6beb-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6beb-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


