---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b02b2abec8138170d574492c8429f463fc6a28a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717265"
---
# <span data-ttu-id="9d55b-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9d55b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d55b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d55b-103">Tworzy konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9d55b-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d55b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d55b-104">SYNTAX</span></span>

### <span data-ttu-id="9d55b-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d55b-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d55b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d55b-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d55b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d55b-107">DESCRIPTION</span></span>
<span data-ttu-id="9d55b-108">Polecenie cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** tworzy konfigurację reguły translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d55b-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9d55b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d55b-109">EXAMPLES</span></span>

### <span data-ttu-id="9d55b-110">Przykład 1: Tworzenie konfiguracji przychodzącej reguły NAT dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9d55b-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="9d55b-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="9d55b-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9d55b-112">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip, a następnie zapisuje ją w zmiennej $frontend.</span><span class="sxs-lookup"><span data-stu-id="9d55b-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="9d55b-113">Trzecie polecenie tworzy konfigurację reguły NAT dla ruchu przychodzącego o nazwie MyInboundNatRule przy użyciu obiektu front-end w $frontend.</span><span class="sxs-lookup"><span data-stu-id="9d55b-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="9d55b-114">Protokół TCP jest określony, a port frontonu to 3389, taki jak w przypadku portu wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9d55b-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="9d55b-115">Parametry *FrontendIpConfiguration* , *procotol* , *FrontendPort* i *BackendPort* są wymagane do utworzenia konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="9d55b-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="9d55b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d55b-116">PARAMETERS</span></span>

### <span data-ttu-id="9d55b-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9d55b-117">-BackendPort</span></span>
<span data-ttu-id="9d55b-118">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="9d55b-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="9d55b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d55b-119">-DefaultProfile</span></span>
<span data-ttu-id="9d55b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d55b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d55b-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9d55b-121">-EnableFloatingIP</span></span>
<span data-ttu-id="9d55b-122">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="9d55b-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9d55b-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9d55b-123">-EnableTcpReset</span></span>
<span data-ttu-id="9d55b-124">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d55b-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9d55b-125">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="9d55b-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9d55b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d55b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9d55b-127">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9d55b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9d55b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9d55b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9d55b-129">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="9d55b-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9d55b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9d55b-130">-FrontendPort</span></span>
<span data-ttu-id="9d55b-131">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9d55b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9d55b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9d55b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9d55b-133">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9d55b-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9d55b-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d55b-134">-Name</span></span>
<span data-ttu-id="9d55b-135">Określa nazwę konfiguracji reguły, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d55b-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9d55b-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="9d55b-136">-Protocol</span></span>
<span data-ttu-id="9d55b-137">Określa protokół.</span><span class="sxs-lookup"><span data-stu-id="9d55b-137">Specifies a protocol.</span></span>
<span data-ttu-id="9d55b-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d55b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d55b-139">Protokoł</span><span class="sxs-lookup"><span data-stu-id="9d55b-139">Tcp</span></span>
- <span data-ttu-id="9d55b-140">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="9d55b-140">Udp</span></span>

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

### <span data-ttu-id="9d55b-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d55b-141">-Confirm</span></span>
<span data-ttu-id="9d55b-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d55b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d55b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d55b-143">-WhatIf</span></span>
<span data-ttu-id="9d55b-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d55b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d55b-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d55b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d55b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d55b-146">CommonParameters</span></span>
<span data-ttu-id="9d55b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d55b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d55b-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d55b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d55b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d55b-149">INPUTS</span></span>

### <span data-ttu-id="9d55b-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d55b-150">None</span></span>

## <span data-ttu-id="9d55b-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d55b-151">OUTPUTS</span></span>

### <span data-ttu-id="9d55b-152">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="9d55b-152">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="9d55b-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d55b-153">NOTES</span></span>

## <span data-ttu-id="9d55b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d55b-154">RELATED LINKS</span></span>

[<span data-ttu-id="9d55b-155">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-155">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d55b-156">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-156">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d55b-157">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-157">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9d55b-158">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d55b-158">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9d55b-159">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-159">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d55b-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d55b-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

