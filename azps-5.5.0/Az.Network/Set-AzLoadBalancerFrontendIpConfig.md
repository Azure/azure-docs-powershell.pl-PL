---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179331"
---
# <span data-ttu-id="56c7b-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56c7b-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="56c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="56c7b-103">Aktualizuje konfigurację frontoronu ip dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="56c7b-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="56c7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56c7b-104">SYNTAX</span></span>

### <span data-ttu-id="56c7b-105">SetByResourceSubnet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="56c7b-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c7b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="56c7b-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c7b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="56c7b-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56c7b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="56c7b-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56c7b-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56c7b-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56c7b-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56c7b-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56c7b-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="56c7b-111">DESCRIPTION</span></span>
<span data-ttu-id="56c7b-112">Polecenie **cmdlet Set-AzLoadBalancerFrontendIpConfig** aktualizuje konfigurację frontoronu IP dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="56c7b-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="56c7b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56c7b-113">EXAMPLES</span></span>

### <span data-ttu-id="56c7b-114">Przykład 1. Modyfikowanie konfiguracji frontoronu ip urządzenia do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="56c7b-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="56c7b-115">Pierwsze polecenie pobiera wirtualną podsieci o nazwie Podsieci, a następnie zapisuje ją w $Subnet zmienną.</span><span class="sxs-lookup"><span data-stu-id="56c7b-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="56c7b-116">Drugie polecenie pobiera skojarzone z nim równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $slb ładowania.</span><span class="sxs-lookup"><span data-stu-id="56c7b-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="56c7b-117">Trzecie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku AzLoadBalancerFrontendIpConfig, co tworzy konfigurację frontoronu IP o nazwie NewFrontend dla systemu $slb.</span><span class="sxs-lookup"><span data-stu-id="56c7b-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="56c7b-118">Czwarte polecenie przekazuje równoważenie obciążenia w programie $slb do **set-AzLoadBalancerFrontendIpConfig,** który zapisuje i aktualizuje konfigurację fronto strony ip.</span><span class="sxs-lookup"><span data-stu-id="56c7b-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="56c7b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56c7b-119">PARAMETERS</span></span>

### <span data-ttu-id="56c7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c7b-120">-DefaultProfile</span></span>
<span data-ttu-id="56c7b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56c7b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c7b-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56c7b-122">-LoadBalancer</span></span>
<span data-ttu-id="56c7b-123">Określa równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="56c7b-123">Specifies a load balancer.</span></span>
<span data-ttu-id="56c7b-124">To polecenie cmdlet aktualizuje konfigurację frontoronu dla równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="56c7b-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="56c7b-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56c7b-125">-Name</span></span>
<span data-ttu-id="56c7b-126">Określa nazwę konfiguracji frontoronu ip, która ma być ustawiona.</span><span class="sxs-lookup"><span data-stu-id="56c7b-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="56c7b-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="56c7b-127">-PrivateIpAddress</span></span>
<span data-ttu-id="56c7b-128">Określa prywatny adres IP urządzenia do równoważenia obciążenia skojarzonego z konfiguracją frontonu ip, która ma być ustawiona.</span><span class="sxs-lookup"><span data-stu-id="56c7b-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="56c7b-129">Określ ten parametr tylko wtedy, gdy określisz również parametr *Podsieci.*</span><span class="sxs-lookup"><span data-stu-id="56c7b-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="56c7b-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="56c7b-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="56c7b-131">Wersja konfiguracji adresu IP dla prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="56c7b-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="56c7b-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="56c7b-132">-PublicIpAddress</span></span>
<span data-ttu-id="56c7b-133">Określa obiekt **PublicIpAddress** skojarzony z konfiguracją frontonu adresu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="56c7b-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="56c7b-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="56c7b-134">-PublicIpAddressId</span></span>
<span data-ttu-id="56c7b-135">Określa identyfikator obiektu **PublicIpAddress** skojarzonego z konfiguracją frontonu adresu IP ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c7b-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="56c7b-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="56c7b-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="56c7b-137">Określa obiekt **PublicIpAddressPrefix** do skojarzenia z konfiguracją frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="56c7b-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="56c7b-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="56c7b-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="56c7b-139">Określa identyfikator obiektu **PublicIpAddressPrefix,** który ma być kojarzony z konfiguracją frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="56c7b-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="56c7b-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="56c7b-140">-Subnet</span></span>
<span data-ttu-id="56c7b-141">Określa obiekt **podsieci,** który zawiera konfigurację frontoronu IP ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c7b-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="56c7b-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="56c7b-142">-SubnetId</span></span>
<span data-ttu-id="56c7b-143">Określa identyfikator podsieci zawierającej konfigurację frontoronu ip ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c7b-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="56c7b-144">— Strefa</span><span class="sxs-lookup"><span data-stu-id="56c7b-144">-Zone</span></span>
<span data-ttu-id="56c7b-145">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="56c7b-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="56c7b-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56c7b-146">-Confirm</span></span>
<span data-ttu-id="56c7b-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56c7b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c7b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c7b-148">-WhatIf</span></span>
<span data-ttu-id="56c7b-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c7b-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56c7b-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56c7b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c7b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c7b-151">CommonParameters</span></span>
<span data-ttu-id="56c7b-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c7b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c7b-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56c7b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c7b-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56c7b-154">INPUTS</span></span>

### <span data-ttu-id="56c7b-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56c7b-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="56c7b-156">System.String</span><span class="sxs-lookup"><span data-stu-id="56c7b-156">System.String</span></span>

### <span data-ttu-id="56c7b-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="56c7b-157">System.String[]</span></span>

### <span data-ttu-id="56c7b-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="56c7b-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="56c7b-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="56c7b-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="56c7b-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56c7b-160">OUTPUTS</span></span>

### <span data-ttu-id="56c7b-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56c7b-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="56c7b-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56c7b-162">NOTES</span></span>

## <span data-ttu-id="56c7b-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56c7b-163">RELATED LINKS</span></span>

[<span data-ttu-id="56c7b-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56c7b-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="56c7b-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56c7b-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="56c7b-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56c7b-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="56c7b-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56c7b-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="56c7b-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56c7b-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="56c7b-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56c7b-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


