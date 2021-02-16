---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193971"
---
# <span data-ttu-id="f129f-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f129f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f129f-102">SYNOPSIS</span></span>
<span data-ttu-id="f129f-103">Dodaje konfigurację frontoronu IP do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f129f-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="f129f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f129f-104">SYNTAX</span></span>

### <span data-ttu-id="f129f-105">SetByResourceSubnet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f129f-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f129f-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f129f-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f129f-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f129f-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f129f-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f129f-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f129f-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f129f-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f129f-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f129f-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f129f-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="f129f-111">DESCRIPTION</span></span>
<span data-ttu-id="f129f-112">Polecenie **cmdlet Add-AzLoadBalancerFrontendIpConfig** dodaje konfigurację front end IP do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f129f-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f129f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f129f-113">EXAMPLES</span></span>

### <span data-ttu-id="f129f-114">Przykład 1. Dodawanie konfiguracji frontoronu ip z dynamicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f129f-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="f129f-115">Pierwsze polecenie pobiera wirtualną sieć Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie MySubnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f129f-116">Następnie polecenie przechowuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f129f-117">Drugie polecenie pobiera równoważenie obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig,** które dodaje konfigurację front end IP do równoważenia obciążenia z dynamicznym prywatnym adresem IP z podsieci przechowywanej w zmiennej o nazwie $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="f129f-118">Przykład 2. Dodawanie konfiguracji frontoronu ip ze statycznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f129f-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="f129f-119">Pierwsze polecenie pobiera wirtualną sieć Azure o nazwie MyVnet i przekazuje wynik za pomocą potoku do polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** w celu uzyskania podsieci o nazwie MySubnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f129f-120">Następnie polecenie przechowuje wynik w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f129f-121">Drugie polecenie pobiera równoważenie obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig,** które dodaje konfigurację front-end IP do równoważenia obciążenia ze statycznym prywatnym adresem IP ze statycznej podsieci przechowywanej w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f129f-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="f129f-122">Przykład 3. Dodawanie konfiguracji frontoronu ip z publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f129f-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="f129f-123">Pierwsze polecenie pobiera publiczny adres IP platformy Azure o nazwie MyPub i przechowuje wynik w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f129f-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="f129f-124">Drugie polecenie pobiera równoważenie obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig,** które dodaje konfigurację front-end IP do równoważenia obciążenia, a publiczny adres IP jest przechowywany w zmiennej o nazwie $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f129f-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="f129f-125">Przykład 4. Dodawanie konfiguracji frontoronu IP z publicznym prefiksem IP</span><span class="sxs-lookup"><span data-stu-id="f129f-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="f129f-126">Pierwsze polecenie otrzymuje publiczny prefiks IP platformy Azure o nazwie MyPubPrefix i przechowuje wynik w zmiennej o nazwie $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="f129f-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="f129f-127">Drugie polecenie pobiera równoważenie obciążenia o nazwie MyLB i przekazuje wynik do polecenia cmdlet **Add-AzLoadBalancerFrontendIpConfig,** które dodaje konfigurację front-end IP do równoważenia obciążenia, a publiczny prefiks IP jest przechowywany w zmiennej o nazwie $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="f129f-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="f129f-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f129f-128">PARAMETERS</span></span>

### <span data-ttu-id="f129f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f129f-129">-DefaultProfile</span></span>
<span data-ttu-id="f129f-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f129f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f129f-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f129f-131">-LoadBalancer</span></span>
<span data-ttu-id="f129f-132">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="f129f-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f129f-133">To polecenie cmdlet dodaje konfigurację frontoronu IP do równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f129f-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f129f-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f129f-134">-Name</span></span>
<span data-ttu-id="f129f-135">Określa nazwę konfiguracji frontoronu IP do dodania.</span><span class="sxs-lookup"><span data-stu-id="f129f-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="f129f-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f129f-136">-PrivateIpAddress</span></span>
<span data-ttu-id="f129f-137">Określa prywatny adres IP do skojarzenia z konfiguracją frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f129f-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f129f-139">Wersja konfiguracji adresu IP dla prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-139">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="f129f-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f129f-140">-PublicIpAddress</span></span>
<span data-ttu-id="f129f-141">Określa publiczny adres IP do skojarzenia z konfiguracją frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f129f-142">-PublicIpAddressId</span></span>
<span data-ttu-id="f129f-143">Określa identyfikator publicznego adresu IP, w którym należy dodać konfigurację frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f129f-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="f129f-145">Określa publiczny obiekt prefiksu adresu IP do skojarzenia z konfiguracją frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="f129f-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="f129f-147">Określa identyfikator obiektu prefiksu publicznego adresu IP do skojarzenia z konfiguracją frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="f129f-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-148">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f129f-148">-Subnet</span></span>
<span data-ttu-id="f129f-149">Określa obiekt podsieci, w którym ma być dodawania konfiguracji frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="f129f-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f129f-150">-SubnetId</span></span>
<span data-ttu-id="f129f-151">Określa identyfikator podsieci, w której ma być dodawania konfiguracji frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="f129f-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f129f-152">— Strefa</span><span class="sxs-lookup"><span data-stu-id="f129f-152">-Zone</span></span>
<span data-ttu-id="f129f-153">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="f129f-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f129f-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f129f-154">-Confirm</span></span>
<span data-ttu-id="f129f-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f129f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f129f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f129f-156">-WhatIf</span></span>
<span data-ttu-id="f129f-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f129f-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f129f-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f129f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f129f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f129f-159">CommonParameters</span></span>
<span data-ttu-id="f129f-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f129f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f129f-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f129f-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f129f-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f129f-162">INPUTS</span></span>

### <span data-ttu-id="f129f-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f129f-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f129f-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f129f-164">System.String</span></span>

### <span data-ttu-id="f129f-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f129f-165">System.String[]</span></span>

### <span data-ttu-id="f129f-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f129f-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f129f-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f129f-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f129f-168">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f129f-168">OUTPUTS</span></span>

### <span data-ttu-id="f129f-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f129f-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f129f-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f129f-170">NOTES</span></span>

## <span data-ttu-id="f129f-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f129f-171">RELATED LINKS</span></span>

[<span data-ttu-id="f129f-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f129f-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f129f-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f129f-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f129f-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f129f-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f129f-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f129f-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


