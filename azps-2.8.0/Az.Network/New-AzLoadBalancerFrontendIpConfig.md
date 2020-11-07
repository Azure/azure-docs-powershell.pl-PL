---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: dc28df7630cbb2c9e239fe31f99ad3361e5c1f54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869915"
---
# <span data-ttu-id="d76a3-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d76a3-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d76a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d76a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d76a3-103">Tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d76a3-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="d76a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d76a3-104">SYNTAX</span></span>

### <span data-ttu-id="d76a3-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d76a3-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76a3-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="d76a3-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76a3-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76a3-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76a3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d76a3-109">DESCRIPTION</span></span>
<span data-ttu-id="d76a3-110">Polecenie cmdlet **New-AzLoadBalancerFrontendIpConfig** tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a3-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d76a3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d76a3-111">EXAMPLES</span></span>

### <span data-ttu-id="d76a3-112">Przykład 1. Tworzenie zewnętrznej konfiguracji adresów IP dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="d76a3-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="d76a3-113">Pierwsze polecenie tworzy dynamiczny publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="d76a3-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="d76a3-114">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip.</span><span class="sxs-lookup"><span data-stu-id="d76a3-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="d76a3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d76a3-115">PARAMETERS</span></span>

### <span data-ttu-id="d76a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76a3-116">-DefaultProfile</span></span>
<span data-ttu-id="d76a3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d76a3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d76a3-118">-Name</span></span>
<span data-ttu-id="d76a3-119">Określa konfigurację adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76a3-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d76a3-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-120">-PrivateIpAddress</span></span>
<span data-ttu-id="d76a3-121">Określa prywatny adres IP modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d76a3-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="d76a3-122">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="d76a3-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="d76a3-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d76a3-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d76a3-124">Prywatny adres IP konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="d76a3-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="d76a3-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-125">-PublicIpAddress</span></span>
<span data-ttu-id="d76a3-126">Określa obiekt **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="d76a3-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d76a3-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d76a3-127">-PublicIpAddressId</span></span>
<span data-ttu-id="d76a3-128">Określa identyfikator obiektu **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="d76a3-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d76a3-129">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="d76a3-129">-Subnet</span></span>
<span data-ttu-id="d76a3-130">Określa obiekt **podsieci** , w którym ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="d76a3-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d76a3-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d76a3-131">-SubnetId</span></span>
<span data-ttu-id="d76a3-132">Określa identyfikator podsieci, w której ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="d76a3-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d76a3-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="d76a3-133">-Zone</span></span>
<span data-ttu-id="d76a3-134">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="d76a3-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="d76a3-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d76a3-135">-Confirm</span></span>
<span data-ttu-id="d76a3-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76a3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76a3-137">-WhatIf</span></span>
<span data-ttu-id="d76a3-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76a3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d76a3-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d76a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76a3-140">CommonParameters</span></span>
<span data-ttu-id="d76a3-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76a3-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76a3-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76a3-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d76a3-143">INPUTS</span></span>

### <span data-ttu-id="d76a3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d76a3-144">System.String</span></span>

### <span data-ttu-id="d76a3-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="d76a3-145">System.String[]</span></span>

### <span data-ttu-id="d76a3-146">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d76a3-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="d76a3-147">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d76a3-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d76a3-148">OUTPUTS</span></span>

### <span data-ttu-id="d76a3-149">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d76a3-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d76a3-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d76a3-150">NOTES</span></span>

## <span data-ttu-id="d76a3-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d76a3-151">RELATED LINKS</span></span>

[<span data-ttu-id="d76a3-152">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d76a3-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d76a3-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d76a3-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d76a3-154">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76a3-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d76a3-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d76a3-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d76a3-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d76a3-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


