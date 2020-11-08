---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231748"
---
# <span data-ttu-id="e1e6e-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e1e6e-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e1e6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e6e-103">Dodaje konfigurację frontonu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="e1e6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1e6e-104">SYNTAX</span></span>

### <span data-ttu-id="e1e6e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1e6e-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e6e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e1e6e-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e6e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e1e6e-107">DESCRIPTION</span></span>
<span data-ttu-id="e1e6e-108">Polecenie cmdlet **Add-AzApplicationGatewayFrontendIPConfig** umożliwia dodanie konfiguracji frontonu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="e1e6e-109">Brama Application Gateway obsługuje dwa typy konfiguracji frontonu IP:</span><span class="sxs-lookup"><span data-stu-id="e1e6e-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="e1e6e-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="e1e6e-110">Public IP addresses</span></span>
- <span data-ttu-id="e1e6e-111">Prywatne adresy IP przy użyciu wewnętrznego równoważenia obciążenia (ILB) Brama Application Gateway może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="e1e6e-112">Dodaj publiczny adres IP i prywatny adres IP jako oddzielne zewnętrzne adresy IP.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="e1e6e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1e6e-113">EXAMPLES</span></span>

### <span data-ttu-id="e1e6e-114">Przykład 1: Dodawanie publicznego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="e1e6e-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="e1e6e-115">Pierwsze polecenie tworzy obiekt publicznego adresu IP i zapisuje go w zmiennej $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="e1e6e-116">Drugie polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1e6e-117">Trzecie polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontEndIp01 dla bramy w $AppGw przy użyciu adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="e1e6e-118">Przykład 2: dodanie statycznego prywatnego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="e1e6e-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="e1e6e-119">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e1e6e-120">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e1e6e-121">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1e6e-122">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="e1e6e-123">Przykład 3: dodanie dynamicznego prywatnego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="e1e6e-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="e1e6e-124">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e1e6e-125">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e1e6e-126">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1e6e-127">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="e1e6e-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1e6e-128">PARAMETERS</span></span>

### <span data-ttu-id="e1e6e-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e6e-129">-ApplicationGateway</span></span>
<span data-ttu-id="e1e6e-130">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e6e-131">-DefaultProfile</span></span>
<span data-ttu-id="e1e6e-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1e6e-133">-Name</span></span>
<span data-ttu-id="e1e6e-134">Określa nazwę konfiguracji adresu IP frontonu do dodania.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="e1e6e-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e1e6e-135">-PrivateIPAddress</span></span>
<span data-ttu-id="e1e6e-136">Określa prywatny adres IP, który ma zostać dodany jako fronton IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="e1e6e-137">Jeśli jest określony, ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1e6e-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="e1e6e-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1e6e-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e1e6e-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="e1e6e-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e1e6e-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="e1e6e-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="e1e6e-142">-PublicIPAddress</span></span>
<span data-ttu-id="e1e6e-143">Określa publiczny adres IP, który to polecenie cmdlet dodaje jako adres IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e1e6e-144">-PublicIPAddressId</span></span>
<span data-ttu-id="e1e6e-145">Określa identyfikator publicznego adresu IP, który jest dodawany przez to polecenie cmdlet jako adres IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="e1e6e-146">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="e1e6e-146">-Subnet</span></span>
<span data-ttu-id="e1e6e-147">Określa podsieć, którą to polecenie cmdlet dodaje jako konfigurację frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="e1e6e-148">Określenie tego parametru oznacza, że brama Application Gateway obsługuje prywatną konfigurację IP opartą na konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="e1e6e-149">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e1e6e-150">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e6e-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e1e6e-151">-SubnetId</span></span>
<span data-ttu-id="e1e6e-152">Określa identyfikator podsieci, który jest dodawany przez ten aplet polecenia jako konfigurację frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="e1e6e-153">Przekazanie podsieci oznacza prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="e1e6e-154">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="e1e6e-155">W przeciwnym razie dowolny z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="e1e6e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e6e-156">CommonParameters</span></span>
<span data-ttu-id="e1e6e-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e6e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e6e-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1e6e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e6e-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1e6e-159">INPUTS</span></span>

### <span data-ttu-id="e1e6e-160">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e6e-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1e6e-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1e6e-161">OUTPUTS</span></span>

### <span data-ttu-id="e1e6e-162">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1e6e-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1e6e-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1e6e-163">NOTES</span></span>

## <span data-ttu-id="e1e6e-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1e6e-164">RELATED LINKS</span></span>

[<span data-ttu-id="e1e6e-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e1e6e-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e1e6e-166">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e1e6e-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e1e6e-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e1e6e-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e1e6e-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e1e6e-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


