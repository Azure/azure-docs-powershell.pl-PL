---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 170ab2536eb03bc04867ad7a3c6828fff5c94749
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971914"
---
# <span data-ttu-id="0537a-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0537a-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0537a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0537a-102">SYNOPSIS</span></span>
<span data-ttu-id="0537a-103">Tworzy konfigurację frontoronu ip dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0537a-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="0537a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0537a-104">SYNTAX</span></span>

### <span data-ttu-id="0537a-105">SetByResourceSubnet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0537a-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0537a-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="0537a-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0537a-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0537a-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0537a-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0537a-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0537a-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0537a-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0537a-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="0537a-111">DESCRIPTION</span></span>
<span data-ttu-id="0537a-112">Polecenie **cmdlet New-AzLoadBalancerFrontendIpConfig** tworzy konfigurację fronto strony IP dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0537a-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0537a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0537a-113">EXAMPLES</span></span>

### <span data-ttu-id="0537a-114">Przykład 1. Tworzenie konfiguracji frontoronu ip dla równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="0537a-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="0537a-115">Pierwsze polecenie tworzy dynamiczny publiczny adres IP o nazwie MyPublicIP w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje go w zmiennej $publicip adresowej.</span><span class="sxs-lookup"><span data-stu-id="0537a-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="0537a-116">Drugie polecenie tworzy konfigurację frontoronu IP o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w u $publicip.</span><span class="sxs-lookup"><span data-stu-id="0537a-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="0537a-117">Przykład 2. Tworzenie konfiguracji frontoronu IP dla równoważenia obciążenia przy użyciu prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="0537a-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="0537a-118">Pierwsze polecenie tworzy publiczny prefiks IP o nazwie MyPublicIP o długości 28 w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje go w zmiennej $publicipprefix adresowej.</span><span class="sxs-lookup"><span data-stu-id="0537a-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="0537a-119">Drugie polecenie tworzy konfigurację frontoronu IP o nazwie FrontendIpConfig01, używając publicznego prefiksu IP w $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="0537a-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="0537a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0537a-120">PARAMETERS</span></span>

### <span data-ttu-id="0537a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0537a-121">-DefaultProfile</span></span>
<span data-ttu-id="0537a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0537a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0537a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0537a-123">-Name</span></span>
<span data-ttu-id="0537a-124">Określa konfigurację frontoletu IP, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0537a-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0537a-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-125">-PrivateIpAddress</span></span>
<span data-ttu-id="0537a-126">Określa prywatny adres IP użytkownika do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0537a-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="0537a-127">Określ ten parametr tylko wtedy, gdy określisz również parametr *Podsieci.*</span><span class="sxs-lookup"><span data-stu-id="0537a-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="0537a-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0537a-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="0537a-129">Wersja konfiguracji adresu IP dla prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="0537a-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-130">-PublicIpAddress</span></span>
<span data-ttu-id="0537a-131">Określa obiekt **PublicIpAddress,** który ma być kojarzony z konfiguracją frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0537a-132">-PublicIpAddressId</span></span>
<span data-ttu-id="0537a-133">Określa identyfikator obiektu **PublicIpAddress,** który ma być kojarzony z konfiguracją frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="0537a-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0537a-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="0537a-135">Określa obiekt **PublicIpAddressPrefix** do skojarzenia z konfiguracją frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="0537a-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="0537a-137">Określa identyfikator obiektu **PublicIpAddressPrefix,** który ma być kojarzony z konfiguracją frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0537a-138">-Subnet</span></span>
<span data-ttu-id="0537a-139">Określa obiekt **podsieci,** w którym ma być tworzyć konfigurację frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0537a-140">-SubnetId</span></span>
<span data-ttu-id="0537a-141">Określa identyfikator podsieci, w której ma być tworzyć konfigurację frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0537a-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0537a-142">— Strefa</span><span class="sxs-lookup"><span data-stu-id="0537a-142">-Zone</span></span>
<span data-ttu-id="0537a-143">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="0537a-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="0537a-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0537a-144">-Confirm</span></span>
<span data-ttu-id="0537a-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0537a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0537a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0537a-146">-WhatIf</span></span>
<span data-ttu-id="0537a-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0537a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0537a-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0537a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0537a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0537a-149">CommonParameters</span></span>
<span data-ttu-id="0537a-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0537a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0537a-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0537a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0537a-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0537a-152">INPUTS</span></span>

### <span data-ttu-id="0537a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0537a-153">System.String</span></span>

### <span data-ttu-id="0537a-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0537a-154">System.String[]</span></span>

### <span data-ttu-id="0537a-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0537a-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="0537a-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0537a-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0537a-157">OUTPUTS</span></span>

### <span data-ttu-id="0537a-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0537a-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0537a-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0537a-159">NOTES</span></span>

## <span data-ttu-id="0537a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0537a-160">RELATED LINKS</span></span>

[<span data-ttu-id="0537a-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0537a-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0537a-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0537a-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0537a-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0537a-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="0537a-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0537a-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0537a-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0537a-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


