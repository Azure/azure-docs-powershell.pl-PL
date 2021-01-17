---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332122"
---
# <span data-ttu-id="7ac53-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ac53-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7ac53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ac53-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac53-103">Tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ac53-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7ac53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ac53-104">SYNTAX</span></span>

### <span data-ttu-id="7ac53-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ac53-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac53-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7ac53-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac53-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac53-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac53-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7ac53-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac53-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7ac53-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac53-111">Opis</span><span class="sxs-lookup"><span data-stu-id="7ac53-111">DESCRIPTION</span></span>
<span data-ttu-id="7ac53-112">Polecenie cmdlet **New-AzLoadBalancerFrontendIpConfig** tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac53-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7ac53-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ac53-113">EXAMPLES</span></span>

### <span data-ttu-id="7ac53-114">Przykład 1. Tworzenie zewnętrznej konfiguracji adresów IP dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7ac53-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="7ac53-115">Pierwsze polecenie tworzy dynamiczny publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="7ac53-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="7ac53-116">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip.</span><span class="sxs-lookup"><span data-stu-id="7ac53-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="7ac53-117">Przykład 2: Tworzenie zewnętrznej konfiguracji adresów IP dla modułu równoważenia obciążenia przy użyciu prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="7ac53-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="7ac53-118">Pierwsze polecenie powoduje utworzenie publicznego prefiksu adresu IP o nazwie MyPublicIP w grupie zasobów o nazwie NazwaMojejZmiennej, a następnie zapisanie go w zmiennej $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="7ac53-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="7ac53-119">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego prefiksu IP w $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="7ac53-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="7ac53-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ac53-120">PARAMETERS</span></span>

### <span data-ttu-id="7ac53-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac53-121">-DefaultProfile</span></span>
<span data-ttu-id="7ac53-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac53-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac53-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ac53-123">-Name</span></span>
<span data-ttu-id="7ac53-124">Określa konfigurację adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac53-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7ac53-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-125">-PrivateIpAddress</span></span>
<span data-ttu-id="7ac53-126">Określa prywatny adres IP modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ac53-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="7ac53-127">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="7ac53-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="7ac53-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7ac53-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7ac53-129">Prywatny adres IP konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="7ac53-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-130">-PublicIpAddress</span></span>
<span data-ttu-id="7ac53-131">Określa obiekt **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7ac53-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7ac53-132">-PublicIpAddressId</span></span>
<span data-ttu-id="7ac53-133">Określa identyfikator obiektu **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7ac53-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7ac53-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="7ac53-135">Określa obiekt **PublicIpAddressPrefix** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7ac53-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="7ac53-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="7ac53-137">Określa identyfikator obiektu **PublicIpAddressPrefix** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7ac53-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-138">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="7ac53-138">-Subnet</span></span>
<span data-ttu-id="7ac53-139">Określa obiekt **podsieci** , w którym ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="7ac53-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7ac53-140">-SubnetId</span></span>
<span data-ttu-id="7ac53-141">Określa identyfikator podsieci, w której ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="7ac53-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7ac53-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="7ac53-142">-Zone</span></span>
<span data-ttu-id="7ac53-143">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="7ac53-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7ac53-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ac53-144">-Confirm</span></span>
<span data-ttu-id="7ac53-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac53-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac53-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac53-146">-WhatIf</span></span>
<span data-ttu-id="7ac53-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac53-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ac53-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ac53-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac53-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac53-149">CommonParameters</span></span>
<span data-ttu-id="7ac53-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac53-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac53-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ac53-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac53-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac53-152">INPUTS</span></span>

### <span data-ttu-id="7ac53-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac53-153">System.String</span></span>

### <span data-ttu-id="7ac53-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="7ac53-154">System.String[]</span></span>

### <span data-ttu-id="7ac53-155">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7ac53-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7ac53-156">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7ac53-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ac53-157">OUTPUTS</span></span>

### <span data-ttu-id="7ac53-158">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ac53-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7ac53-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ac53-159">NOTES</span></span>

## <span data-ttu-id="7ac53-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac53-160">RELATED LINKS</span></span>

[<span data-ttu-id="7ac53-161">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ac53-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ac53-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ac53-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ac53-163">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac53-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7ac53-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ac53-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ac53-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ac53-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


