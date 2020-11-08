---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063944"
---
# <span data-ttu-id="a5cea-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a5cea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5cea-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cea-103">Tworzy konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a5cea-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a5cea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5cea-104">SYNTAX</span></span>

### <span data-ttu-id="a5cea-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5cea-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cea-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5cea-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5cea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a5cea-107">DESCRIPTION</span></span>
<span data-ttu-id="a5cea-108">Polecenie cmdlet **New-AzLoadBalancerInboundNatRuleConfig** tworzy konfigurację reguły translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cea-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a5cea-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5cea-109">EXAMPLES</span></span>

### <span data-ttu-id="a5cea-110">Przykład 1: Tworzenie konfiguracji przychodzącej reguły NAT dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a5cea-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="a5cea-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="a5cea-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="a5cea-112">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip, a następnie zapisuje ją w zmiennej $frontend.</span><span class="sxs-lookup"><span data-stu-id="a5cea-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="a5cea-113">Trzecie polecenie tworzy konfigurację reguły NAT dla ruchu przychodzącego o nazwie MyInboundNatRule przy użyciu obiektu front-end w $frontend.</span><span class="sxs-lookup"><span data-stu-id="a5cea-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="a5cea-114">Protokół TCP jest określony, a port frontonu to 3389, taki jak w przypadku portu wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a5cea-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="a5cea-115">Parametry *FrontendIpConfiguration* , *Protocol* , *FrontendPort* i *BackendPort* są wymagane do utworzenia konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="a5cea-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="a5cea-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5cea-116">PARAMETERS</span></span>

### <span data-ttu-id="a5cea-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a5cea-117">-BackendPort</span></span>
<span data-ttu-id="a5cea-118">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="a5cea-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a5cea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cea-119">-DefaultProfile</span></span>
<span data-ttu-id="a5cea-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cea-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cea-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a5cea-121">-EnableFloatingIP</span></span>
<span data-ttu-id="a5cea-122">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="a5cea-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a5cea-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a5cea-123">-EnableTcpReset</span></span>
<span data-ttu-id="a5cea-124">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="a5cea-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a5cea-125">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="a5cea-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a5cea-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5cea-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a5cea-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a5cea-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a5cea-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a5cea-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a5cea-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="a5cea-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a5cea-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5cea-130">-FrontendPort</span></span>
<span data-ttu-id="a5cea-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a5cea-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a5cea-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a5cea-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a5cea-133">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a5cea-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a5cea-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5cea-134">-Name</span></span>
<span data-ttu-id="a5cea-135">Określa nazwę konfiguracji reguły, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cea-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a5cea-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a5cea-136">-Protocol</span></span>
<span data-ttu-id="a5cea-137">Określa protokół.</span><span class="sxs-lookup"><span data-stu-id="a5cea-137">Specifies a protocol.</span></span>
<span data-ttu-id="a5cea-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a5cea-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5cea-139">Protokoł</span><span class="sxs-lookup"><span data-stu-id="a5cea-139">Tcp</span></span>
- <span data-ttu-id="a5cea-140">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="a5cea-140">Udp</span></span>

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

### <span data-ttu-id="a5cea-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5cea-141">-Confirm</span></span>
<span data-ttu-id="a5cea-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cea-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cea-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cea-143">-WhatIf</span></span>
<span data-ttu-id="a5cea-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cea-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5cea-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5cea-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cea-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cea-146">CommonParameters</span></span>
<span data-ttu-id="a5cea-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cea-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cea-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5cea-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cea-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5cea-149">INPUTS</span></span>

### <span data-ttu-id="a5cea-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a5cea-150">System.String</span></span>

### <span data-ttu-id="a5cea-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a5cea-151">System.Int32</span></span>

### <span data-ttu-id="a5cea-152">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5cea-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a5cea-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5cea-153">OUTPUTS</span></span>

### <span data-ttu-id="a5cea-154">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a5cea-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="a5cea-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5cea-155">NOTES</span></span>

## <span data-ttu-id="a5cea-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5cea-156">RELATED LINKS</span></span>

[<span data-ttu-id="a5cea-157">Dodaj-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5cea-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5cea-159">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a5cea-160">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5cea-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a5cea-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5cea-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5cea-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


