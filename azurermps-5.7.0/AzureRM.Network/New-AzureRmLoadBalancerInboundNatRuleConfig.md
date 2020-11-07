---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 0b974d1d79be82f3c16f1052abe0eecc7fa9ba30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717728"
---
# <span data-ttu-id="34e3e-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="34e3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="34e3e-103">Tworzy konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34e3e-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34e3e-104">SYNTAX</span></span>

### <span data-ttu-id="34e3e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34e3e-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34e3e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="34e3e-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="34e3e-108">Polecenie cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** tworzy konfigurację reguły translacji adresów sieciowych (NAT) dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34e3e-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="34e3e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34e3e-109">EXAMPLES</span></span>

### <span data-ttu-id="34e3e-110">Przykład 1: Tworzenie konfiguracji przychodzącej reguły NAT dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="34e3e-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="34e3e-111">Pierwsze polecenie tworzy publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="34e3e-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="34e3e-112">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip, a następnie zapisuje ją w zmiennej $frontend.</span><span class="sxs-lookup"><span data-stu-id="34e3e-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="34e3e-113">Trzecie polecenie tworzy konfigurację reguły NAT dla ruchu przychodzącego o nazwie MyInboundNatRule przy użyciu obiektu front-end w $frontend.</span><span class="sxs-lookup"><span data-stu-id="34e3e-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="34e3e-114">Protokół TCP jest określony, a port frontonu to 3389, taki jak w przypadku portu wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="34e3e-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="34e3e-115">Parametry *FrontendIpConfiguration* , *procotol* , *FrontendPort* i *BackendPort* są wymagane do utworzenia konfiguracji reguły ruchu przychodzącego NAT.</span><span class="sxs-lookup"><span data-stu-id="34e3e-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="34e3e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34e3e-116">PARAMETERS</span></span>

### <span data-ttu-id="34e3e-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="34e3e-117">-BackendPort</span></span>
<span data-ttu-id="34e3e-118">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="34e3e-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="34e3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e3e-119">-DefaultProfile</span></span>
<span data-ttu-id="34e3e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34e3e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e3e-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="34e3e-121">-EnableFloatingIP</span></span>
<span data-ttu-id="34e3e-122">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="34e3e-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="34e3e-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e3e-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="34e3e-124">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34e3e-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="34e3e-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34e3e-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="34e3e-126">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="34e3e-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="34e3e-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="34e3e-127">-FrontendPort</span></span>
<span data-ttu-id="34e3e-128">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34e3e-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="34e3e-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="34e3e-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="34e3e-130">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34e3e-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="34e3e-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34e3e-131">-Name</span></span>
<span data-ttu-id="34e3e-132">Określa nazwę konfiguracji reguły, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e3e-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="34e3e-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="34e3e-133">-Protocol</span></span>
<span data-ttu-id="34e3e-134">Określa protokół.</span><span class="sxs-lookup"><span data-stu-id="34e3e-134">Specifies a protocol.</span></span>
<span data-ttu-id="34e3e-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="34e3e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34e3e-136">Protokoł</span><span class="sxs-lookup"><span data-stu-id="34e3e-136">Tcp</span></span>
- <span data-ttu-id="34e3e-137">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="34e3e-137">Udp</span></span>

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

### <span data-ttu-id="34e3e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e3e-138">CommonParameters</span></span>
<span data-ttu-id="34e3e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e3e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e3e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e3e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e3e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34e3e-141">INPUTS</span></span>

### <span data-ttu-id="34e3e-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34e3e-142">None</span></span>
<span data-ttu-id="34e3e-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="34e3e-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34e3e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34e3e-144">OUTPUTS</span></span>

### <span data-ttu-id="34e3e-145">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="34e3e-145">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="34e3e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34e3e-146">NOTES</span></span>

## <span data-ttu-id="34e3e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34e3e-147">RELATED LINKS</span></span>

[<span data-ttu-id="34e3e-148">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34e3e-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34e3e-150">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-150">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="34e3e-151">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34e3e-151">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="34e3e-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34e3e-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e3e-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


