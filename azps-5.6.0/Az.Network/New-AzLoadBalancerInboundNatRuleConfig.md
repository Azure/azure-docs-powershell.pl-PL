---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a6bec76345df188ca58e8b790637e35606de1f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001098"
---
# <span data-ttu-id="9eaf0-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9eaf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaf0-103">Tworzy konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9eaf0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9eaf0-104">SYNTAX</span></span>

### <span data-ttu-id="9eaf0-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9eaf0-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eaf0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9eaf0-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eaf0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9eaf0-107">DESCRIPTION</span></span>
<span data-ttu-id="9eaf0-108">Polecenie **cmdlet New-AzLoadBalancerInboundNatRuleConfig** tworzy konfigurację reguły translacji przychodzącego adresu sieciowego (NAT) dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9eaf0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9eaf0-109">EXAMPLES</span></span>

### <span data-ttu-id="9eaf0-110">Przykład 1. Tworzenie konfiguracji reguły nat ruchu przychodzącego dla równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9eaf0-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="9eaf0-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje go w zmiennej $publicip adresowej.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9eaf0-112">Drugie polecenie tworzy konfigurację frontonu adresu IP o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w programie $publicip, a następnie przechowuje ją w $frontend danych.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="9eaf0-113">Trzecie polecenie tworzy konfigurację reguły przychodzącego nat o nazwie MyInboundNatRule przy użyciu obiektu frontoronu w u $frontend.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="9eaf0-114">Protokół TCP jest określony, a port frontonie to 3389, taki sam jak port zaplecza w tym przypadku.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="9eaf0-115">Parametry *FrontendIpConfiguration,* *Protocol,* *FrontendPort* i *BackendPort* są wymagane do utworzenia konfiguracji reguły przychodzącego nat.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="9eaf0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eaf0-116">PARAMETERS</span></span>

### <span data-ttu-id="9eaf0-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9eaf0-117">-BackendPort</span></span>
<span data-ttu-id="9eaf0-118">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="9eaf0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaf0-119">-DefaultProfile</span></span>
<span data-ttu-id="9eaf0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eaf0-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9eaf0-121">-EnableFloatingIP</span></span>
<span data-ttu-id="9eaf0-122">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9eaf0-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9eaf0-123">-EnableTcpReset</span></span>
<span data-ttu-id="9eaf0-124">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9eaf0-125">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9eaf0-126">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eaf0-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9eaf0-127">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9eaf0-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9eaf0-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9eaf0-129">Określa identyfikator konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9eaf0-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9eaf0-130">-FrontendPort</span></span>
<span data-ttu-id="9eaf0-131">Określa port frontoronu, który jest do siebie dopasowany przez konfigurację reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9eaf0-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9eaf0-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9eaf0-133">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9eaf0-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9eaf0-134">-Name</span></span>
<span data-ttu-id="9eaf0-135">Określa nazwę konfiguracji reguły, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9eaf0-136">— Protokół</span><span class="sxs-lookup"><span data-stu-id="9eaf0-136">-Protocol</span></span>
<span data-ttu-id="9eaf0-137">Określa protokół.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-137">Specifies a protocol.</span></span>
<span data-ttu-id="9eaf0-138">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9eaf0-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9eaf0-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="9eaf0-139">Tcp</span></span>
- <span data-ttu-id="9eaf0-140">Udp</span><span class="sxs-lookup"><span data-stu-id="9eaf0-140">Udp</span></span>

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

### <span data-ttu-id="9eaf0-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9eaf0-141">-Confirm</span></span>
<span data-ttu-id="9eaf0-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eaf0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eaf0-143">-WhatIf</span></span>
<span data-ttu-id="9eaf0-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9eaf0-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eaf0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaf0-146">CommonParameters</span></span>
<span data-ttu-id="9eaf0-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaf0-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eaf0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaf0-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9eaf0-149">INPUTS</span></span>

### <span data-ttu-id="9eaf0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9eaf0-150">System.String</span></span>

### <span data-ttu-id="9eaf0-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9eaf0-151">System.Int32</span></span>

### <span data-ttu-id="9eaf0-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eaf0-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9eaf0-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9eaf0-153">OUTPUTS</span></span>

### <span data-ttu-id="9eaf0-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="9eaf0-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="9eaf0-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9eaf0-155">NOTES</span></span>

## <span data-ttu-id="9eaf0-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9eaf0-156">RELATED LINKS</span></span>

[<span data-ttu-id="9eaf0-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9eaf0-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9eaf0-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9eaf0-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9eaf0-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="9eaf0-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9eaf0-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9eaf0-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


