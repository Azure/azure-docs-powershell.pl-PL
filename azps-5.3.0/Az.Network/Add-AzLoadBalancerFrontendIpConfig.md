---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503258"
---
# <span data-ttu-id="96c8e-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="96c8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="96c8e-103">Umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="96c8e-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="96c8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96c8e-104">SYNTAX</span></span>

### <span data-ttu-id="96c8e-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96c8e-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c8e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="96c8e-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c8e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="96c8e-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96c8e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="96c8e-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96c8e-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96c8e-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96c8e-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96c8e-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96c8e-111">Opis</span><span class="sxs-lookup"><span data-stu-id="96c8e-111">DESCRIPTION</span></span>
<span data-ttu-id="96c8e-112">Polecenie cmdlet **Add-AzLoadBalancerFrontendIpConfig** umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="96c8e-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="96c8e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96c8e-113">EXAMPLES</span></span>

### <span data-ttu-id="96c8e-114">Przykład 1 Dodawanie konfiguracji frontonu IP z dynamicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="96c8e-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="96c8e-115">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="96c8e-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="96c8e-116">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="96c8e-117">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia o dynamicznym prywatnym adresie IP z podsieci przechowywanej w zmiennej o nazwie $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="96c8e-118">Przykład 2 Dodawanie konfiguracji frontonu IP ze statycznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="96c8e-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="96c8e-119">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="96c8e-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="96c8e-120">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="96c8e-121">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia ze statycznym prywatnym adresem IP z podsieci przechowywanej w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="96c8e-122">Przykład 3 Dodawanie konfiguracji frontonu IP przy użyciu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="96c8e-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="96c8e-123">Pierwsze polecenie uzyskuje publiczny adres IP usługi Azure o nazwie MyPub i zapisuje wynik w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="96c8e-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="96c8e-124">Drugie polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia z publicznym adresem IP przechowywanym w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="96c8e-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="96c8e-125">Przykład 4 Dodawanie konfiguracji frontonu IP za pomocą publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="96c8e-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="96c8e-126">Pierwsze polecenie powoduje wyświetlenie prefiksu publicznego adresu IP o nazwie MyPubPrefix i zapisanie wyniku w zmiennej o nazwie $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="96c8e-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="96c8e-127">Drugie polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia z publicznym prefiksem IP przechowywaną w zmiennej o nazwie $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="96c8e-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="96c8e-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96c8e-128">PARAMETERS</span></span>

### <span data-ttu-id="96c8e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c8e-129">-DefaultProfile</span></span>
<span data-ttu-id="96c8e-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96c8e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c8e-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="96c8e-131">-LoadBalancer</span></span>
<span data-ttu-id="96c8e-132">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="96c8e-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="96c8e-133">To polecenie cmdlet umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="96c8e-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96c8e-134">-Name</span></span>
<span data-ttu-id="96c8e-135">Określa nazwę konfiguracji adresu IP frontonu do dodania.</span><span class="sxs-lookup"><span data-stu-id="96c8e-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="96c8e-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="96c8e-136">-PrivateIpAddress</span></span>
<span data-ttu-id="96c8e-137">Określa prywatny adres IP, który ma być skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="96c8e-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="96c8e-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="96c8e-139">Prywatny adres IP konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="96c8e-139">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="96c8e-140">-PublicIpAddress</span></span>
<span data-ttu-id="96c8e-141">Określa publiczny adres IP, który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="96c8e-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="96c8e-142">-PublicIpAddressId</span></span>
<span data-ttu-id="96c8e-143">Określa identyfikator publicznego adresu IP, w którym ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="96c8e-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96c8e-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="96c8e-145">Określa obiekt prefiksu publicznego adresu IP, który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="96c8e-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="96c8e-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="96c8e-147">Określa identyfikator publicznego obiektu prefiksu adresu IP, który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="96c8e-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-148">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="96c8e-148">-Subnet</span></span>
<span data-ttu-id="96c8e-149">Określa obiekt podsieci, do którego ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="96c8e-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="96c8e-150">-SubnetId</span></span>
<span data-ttu-id="96c8e-151">Określa identyfikator podsieci, do której ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="96c8e-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="96c8e-152">-Zone</span></span>
<span data-ttu-id="96c8e-153">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="96c8e-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c8e-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96c8e-154">-Confirm</span></span>
<span data-ttu-id="96c8e-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c8e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c8e-156">-WhatIf</span></span>
<span data-ttu-id="96c8e-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96c8e-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96c8e-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96c8e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c8e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c8e-159">CommonParameters</span></span>
<span data-ttu-id="96c8e-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c8e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c8e-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c8e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c8e-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96c8e-162">INPUTS</span></span>

### <span data-ttu-id="96c8e-163">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96c8e-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="96c8e-164">System. String</span><span class="sxs-lookup"><span data-stu-id="96c8e-164">System.String</span></span>

### <span data-ttu-id="96c8e-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="96c8e-165">System.String[]</span></span>

### <span data-ttu-id="96c8e-166">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="96c8e-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="96c8e-167">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="96c8e-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="96c8e-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96c8e-168">OUTPUTS</span></span>

### <span data-ttu-id="96c8e-169">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96c8e-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="96c8e-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96c8e-170">NOTES</span></span>

## <span data-ttu-id="96c8e-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96c8e-171">RELATED LINKS</span></span>

[<span data-ttu-id="96c8e-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="96c8e-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96c8e-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="96c8e-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="96c8e-175">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="96c8e-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="96c8e-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="96c8e-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


