---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527882"
---
# <span data-ttu-id="f0736-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f0736-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0736-102">SYNOPSIS</span></span>
<span data-ttu-id="f0736-103">Umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f0736-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0736-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0736-104">SYNTAX</span></span>

### <span data-ttu-id="f0736-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0736-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0736-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f0736-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0736-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0736-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0736-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0736-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0736-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f0736-109">DESCRIPTION</span></span>
<span data-ttu-id="f0736-110">Polecenie cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0736-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f0736-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0736-111">EXAMPLES</span></span>

### <span data-ttu-id="f0736-112">Przykład 1 Dodawanie konfiguracji frontonu IP z dynamicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f0736-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f0736-113">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="f0736-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f0736-114">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f0736-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f0736-115">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia o dynamicznym prywatnym adresie IP z podsieci przechowywanej w zmiennej o nazwie $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="f0736-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="f0736-116">Przykład 2 Dodawanie konfiguracji frontonu IP ze statycznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f0736-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f0736-117">Pierwsze polecenie uzyskuje sieć wirtualną Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie Moja podsieć.</span><span class="sxs-lookup"><span data-stu-id="f0736-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f0736-118">Polecenie zapisuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f0736-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f0736-119">Drugie polecenie uzyskuje moduł równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia ze statycznym prywatnym adresem IP z podsieci przechowywanej w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f0736-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="f0736-120">Przykład 3 Dodawanie konfiguracji frontonu IP przy użyciu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="f0736-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f0736-121">Pierwsze polecenie uzyskuje publiczny adres IP usługi Azure o nazwie MyPub i zapisuje wynik w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f0736-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="f0736-122">Drugie polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** , które dodaje konfigurację frontonu IP do modułu równoważenia obciążenia z publicznym adresem IP przechowywanym w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f0736-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="f0736-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0736-123">PARAMETERS</span></span>

### <span data-ttu-id="f0736-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0736-124">-DefaultProfile</span></span>
<span data-ttu-id="f0736-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0736-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0736-126">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f0736-126">-LoadBalancer</span></span>
<span data-ttu-id="f0736-127">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="f0736-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f0736-128">To polecenie cmdlet umożliwia dodanie konfiguracji frontonu IP do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f0736-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0736-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0736-129">-Name</span></span>
<span data-ttu-id="f0736-130">Określa nazwę konfiguracji adresu IP frontonu do dodania.</span><span class="sxs-lookup"><span data-stu-id="f0736-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="f0736-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0736-131">-PrivateIpAddress</span></span>
<span data-ttu-id="f0736-132">Określa prywatny adres IP, który ma być skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="f0736-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f0736-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0736-133">-PublicIpAddress</span></span>
<span data-ttu-id="f0736-134">Określa publiczny adres IP, który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="f0736-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f0736-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f0736-135">-PublicIpAddressId</span></span>
<span data-ttu-id="f0736-136">Specifes identyfikator publicznego adresu IP, w którym ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="f0736-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f0736-137">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="f0736-137">-Subnet</span></span>
<span data-ttu-id="f0736-138">Określa obiekt podsieci, do którego ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="f0736-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f0736-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f0736-139">-SubnetId</span></span>
<span data-ttu-id="f0736-140">Określa identyfikator podsieci, do której ma zostać dodana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="f0736-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f0736-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="f0736-141">-Zone</span></span>
<span data-ttu-id="f0736-142">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="f0736-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f0736-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0736-143">-Confirm</span></span>
<span data-ttu-id="f0736-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0736-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0736-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0736-145">-WhatIf</span></span>
<span data-ttu-id="f0736-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0736-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0736-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0736-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0736-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0736-148">CommonParameters</span></span>
<span data-ttu-id="f0736-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0736-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0736-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0736-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0736-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0736-151">INPUTS</span></span>

### <span data-ttu-id="f0736-152">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0736-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="f0736-153">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0736-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="f0736-154">System. Collections. Generic. list \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f0736-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f0736-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0736-155">OUTPUTS</span></span>

### <span data-ttu-id="f0736-156">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0736-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0736-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0736-157">NOTES</span></span>

## <span data-ttu-id="f0736-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0736-158">RELATED LINKS</span></span>

[<span data-ttu-id="f0736-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f0736-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f0736-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="f0736-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f0736-162">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f0736-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f0736-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0736-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


