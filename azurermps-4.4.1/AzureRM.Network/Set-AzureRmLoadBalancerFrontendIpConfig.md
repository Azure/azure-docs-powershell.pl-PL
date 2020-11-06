---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d071e6f20d91dacfd99ca9566c64c4734ae93e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543243"
---
# <span data-ttu-id="cc737-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc737-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cc737-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc737-102">SYNOPSIS</span></span>
<span data-ttu-id="cc737-103">Ustawia stan celu dla konfiguracji frontonu IP w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cc737-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc737-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc737-104">SYNTAX</span></span>

### <span data-ttu-id="cc737-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="cc737-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc737-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="cc737-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc737-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc737-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc737-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc737-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc737-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cc737-109">DESCRIPTION</span></span>
<span data-ttu-id="cc737-110">Polecenie cmdlet **Set-AzureRmLoadBalancerFrontendIpConfig** ustawia stan celu dla konfiguracji frontonu IP w usłudze równoważenia obciążenia Azure.</span><span class="sxs-lookup"><span data-stu-id="cc737-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="cc737-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc737-111">EXAMPLES</span></span>

### <span data-ttu-id="cc737-112">Przykład 1: modyfikowanie konfiguracji adresu IP frontonu modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="cc737-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="cc737-113">Pierwsze polecenie uzyskuje podsieć wirtualną o nazwie Subnet, a następnie zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="cc737-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="cc737-114">Drugie polecenie uzyskuje skojarzony moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="cc737-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="cc737-115">W trzecim poleceniu jest używany operator potoku umożliwiający przekazanie modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerFrontendIpConfig, które powoduje utworzenie zewnętrznej konfiguracji adresu IP o nazwie NewFrontend dla $slb.</span><span class="sxs-lookup"><span data-stu-id="cc737-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="cc737-116">Czwarte polecenie przekazuje moduł równoważenia obciążenia w $slb do polecenia **Set-AzureRmLoadBalancerFrontendIpConfig** , które umożliwia zapisywanie i aktualizowanie konfiguracji frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="cc737-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="cc737-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc737-117">PARAMETERS</span></span>

### <span data-ttu-id="cc737-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc737-118">-DefaultProfile</span></span>
<span data-ttu-id="cc737-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc737-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc737-120">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="cc737-120">-LoadBalancer</span></span>
<span data-ttu-id="cc737-121">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cc737-121">Specifies a load balancer.</span></span>
<span data-ttu-id="cc737-122">To polecenie cmdlet ustawia stan celu dla konfiguracji frontonu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cc737-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc737-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc737-123">-Name</span></span>
<span data-ttu-id="cc737-124">Określa nazwę konfiguracji adresu IP frontonu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="cc737-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="cc737-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc737-125">-PrivateIpAddress</span></span>
<span data-ttu-id="cc737-126">Określa prywatny adres IP modułu równoważenia obciążenia, który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="cc737-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="cc737-127">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="cc737-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc737-128">-PublicIpAddress</span></span>
<span data-ttu-id="cc737-129">Określa obiekt **PublicIpAddress** , który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="cc737-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cc737-130">-PublicIpAddressId</span></span>
<span data-ttu-id="cc737-131">Określa identyfikator obiektu **PublicIpAddress** skojarzonego z konfiguracją adresu IP frontonu, którą ustawia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc737-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-132">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="cc737-132">-Subnet</span></span>
<span data-ttu-id="cc737-133">Określa obiekt **podsieci** , który zawiera konfigurację adresu IP frontonu ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc737-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc737-134">-SubnetId</span></span>
<span data-ttu-id="cc737-135">Określa identyfikator podsieci, w której znajduje się konfiguracja frontonu IP, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc737-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="cc737-136">-Zone</span></span>
<span data-ttu-id="cc737-137">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="cc737-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc737-138">CommonParameters</span></span>
<span data-ttu-id="cc737-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc737-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc737-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc737-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc737-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc737-141">INPUTS</span></span>

### <span data-ttu-id="cc737-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc737-142">PSLoadBalancer</span></span>
<span data-ttu-id="cc737-143">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="cc737-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="cc737-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc737-144">OUTPUTS</span></span>

### <span data-ttu-id="cc737-145">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc737-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cc737-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc737-146">NOTES</span></span>

## <span data-ttu-id="cc737-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc737-147">RELATED LINKS</span></span>

[<span data-ttu-id="cc737-148">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc737-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc737-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc737-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="cc737-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc737-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc737-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc737-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cc737-152">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc737-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc737-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc737-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


