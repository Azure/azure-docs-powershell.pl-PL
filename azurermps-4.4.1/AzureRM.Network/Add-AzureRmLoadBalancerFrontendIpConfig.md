---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 026e9a5bcad55312156be4a14eea238c063b9caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717828"
---
# <span data-ttu-id="499c8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="499c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="499c8-102">SYNOPSIS</span></span>
<span data-ttu-id="499c8-103">Umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="499c8-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="499c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="499c8-104">SYNTAX</span></span>

### <span data-ttu-id="499c8-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="499c8-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="499c8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="499c8-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="499c8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="499c8-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="499c8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="499c8-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="499c8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="499c8-109">DESCRIPTION</span></span>
<span data-ttu-id="499c8-110">Polecenie cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="499c8-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="499c8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="499c8-111">EXAMPLES</span></span>

### <span data-ttu-id="499c8-112">Przykład 1 Dodawanie konfiguracji frontonu IP z dynamicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="499c8-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="499c8-113">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="499c8-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="499c8-114">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="499c8-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="499c8-115">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia o dynamicznym prywatnym adresie IP z podsieci przechowywanej w zmiennej o nazwie $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="499c8-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="499c8-116">Przykład 2 Dodawanie konfiguracji frontonu IP ze statycznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="499c8-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="499c8-117">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="499c8-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="499c8-118">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="499c8-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="499c8-119">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia ze statycznym prywatnym adresem IP z podsieci przechowywanej w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="499c8-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="499c8-120">Przykład 3 Dodawanie konfiguracji frontonu IP przy użyciu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="499c8-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="499c8-121">Pierwsze polecenie uzyskuje publiczny adres IP usługi Azure o nazwie MyPub i zapisuje wynik w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="499c8-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="499c8-122">Drugie polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia z publicznym adresem IP przechowywanym w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="499c8-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="499c8-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="499c8-123">PARAMETERS</span></span>

### <span data-ttu-id="499c8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499c8-124">-DefaultProfile</span></span>
<span data-ttu-id="499c8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="499c8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="499c8-126">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="499c8-126">-LoadBalancer</span></span>
<span data-ttu-id="499c8-127">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="499c8-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="499c8-128">To polecenie cmdlet umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="499c8-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="499c8-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="499c8-129">-Name</span></span>
<span data-ttu-id="499c8-130">Określa nazwę konfiguracji adresu IP frontonu do dodania.</span><span class="sxs-lookup"><span data-stu-id="499c8-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="499c8-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="499c8-131">-PrivateIpAddress</span></span>
<span data-ttu-id="499c8-132">Określa prywatny adres IP, który ma być skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="499c8-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="499c8-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="499c8-133">-PublicIpAddress</span></span>
<span data-ttu-id="499c8-134">Określa publiczny adres IP, który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="499c8-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="499c8-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="499c8-135">-PublicIpAddressId</span></span>
<span data-ttu-id="499c8-136">Specifes identyfikator publicznego adresu IP, w którym ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="499c8-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="499c8-137">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="499c8-137">-Subnet</span></span>
<span data-ttu-id="499c8-138">Określa obiekt podsieci, do którego ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="499c8-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="499c8-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="499c8-139">-SubnetId</span></span>
<span data-ttu-id="499c8-140">Określa identyfikator podsieci, do której ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="499c8-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="499c8-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="499c8-141">-Zone</span></span>
<span data-ttu-id="499c8-142">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="499c8-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="499c8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499c8-143">CommonParameters</span></span>
<span data-ttu-id="499c8-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499c8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499c8-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="499c8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499c8-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="499c8-146">INPUTS</span></span>

### <span data-ttu-id="499c8-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="499c8-147">PSLoadBalancer</span></span>
<span data-ttu-id="499c8-148">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="499c8-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="499c8-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="499c8-149">OUTPUTS</span></span>

### <span data-ttu-id="499c8-150">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="499c8-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="499c8-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="499c8-151">NOTES</span></span>

## <span data-ttu-id="499c8-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="499c8-152">RELATED LINKS</span></span>

[<span data-ttu-id="499c8-153">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="499c8-154">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="499c8-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="499c8-155">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="499c8-156">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="499c8-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="499c8-158">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="499c8-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

