---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378758"
---
# <span data-ttu-id="43e1b-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="43e1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="43e1b-103">Modyfikuje konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="43e1b-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="43e1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43e1b-104">SYNTAX</span></span>

### <span data-ttu-id="43e1b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43e1b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43e1b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="43e1b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43e1b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="43e1b-107">DESCRIPTION</span></span>
<span data-ttu-id="43e1b-108">Polecenie cmdlet **Set-AzApplicationGatewayFrontendIPConfig** umożliwia zaktualizowanie konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="43e1b-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="43e1b-109">Brama Application Gateway obsługuje dwa typy zewnętrznych adresów IP:</span><span class="sxs-lookup"><span data-stu-id="43e1b-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="43e1b-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="43e1b-110">Public IP addresses</span></span>
- <span data-ttu-id="43e1b-111">Prywatne adresy IP, dla których konfiguracja używa wewnętrznego równoważenia obciążenia (ILB) Brama aplikacji może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="43e1b-112">Publiczny adres IP i prywatny adres IP należy dodać oddzielnie jako adresy IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="43e1b-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="43e1b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43e1b-113">EXAMPLES</span></span>

### <span data-ttu-id="43e1b-114">Przykład 1: Ustawianie publicznego adresu IP jako adresu IP frontonu bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="43e1b-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="43e1b-115">Pierwsze polecenie tworzy obiekt publicznego adresu IP i zapisuje go w zmiennej $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="43e1b-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="43e1b-116">Drugie polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="43e1b-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="43e1b-117">Trzecie polecenie aktualizuje konfigurację IP frontonu o nazwie FrontEndIp01 dla bramy w $AppGw przy użyciu adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="43e1b-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="43e1b-118">Przykład 2: Ustawianie statycznego prywatnego adresu IP jako adresu IP frontonu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="43e1b-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="43e1b-119">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="43e1b-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="43e1b-120">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="43e1b-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="43e1b-121">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="43e1b-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="43e1b-122">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="43e1b-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="43e1b-123">Przykład 3: Ustawianie dynamicznego prywatnego adresu IP jako frontonu IP bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="43e1b-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="43e1b-124">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="43e1b-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="43e1b-125">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="43e1b-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="43e1b-126">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="43e1b-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="43e1b-127">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="43e1b-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="43e1b-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43e1b-128">PARAMETERS</span></span>

### <span data-ttu-id="43e1b-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43e1b-129">-ApplicationGateway</span></span>
<span data-ttu-id="43e1b-130">Określa obiekt bramy aplikacji, w którym ma zostać zmodyfikowana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="43e1b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e1b-131">-DefaultProfile</span></span>
<span data-ttu-id="43e1b-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43e1b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43e1b-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43e1b-133">-Name</span></span>
<span data-ttu-id="43e1b-134">Określa nazwę konfiguracji adresu IP frontonu, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="43e1b-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="43e1b-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="43e1b-135">-PrivateIPAddress</span></span>
<span data-ttu-id="43e1b-136">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-136">Specifies the private IP address.</span></span>
<span data-ttu-id="43e1b-137">Jeśli jest określony, ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="43e1b-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="43e1b-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="43e1b-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="43e1b-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="43e1b-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="43e1b-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="43e1b-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="43e1b-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="43e1b-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="43e1b-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="43e1b-142">-PublicIPAddress</span></span>
<span data-ttu-id="43e1b-143">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="43e1b-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="43e1b-144">-PublicIPAddressId</span></span>
<span data-ttu-id="43e1b-145">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="43e1b-146">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="43e1b-146">-Subnet</span></span>
<span data-ttu-id="43e1b-147">Określa podsieć, którą Brama applicationowa używa.</span><span class="sxs-lookup"><span data-stu-id="43e1b-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="43e1b-148">Określ ten parametr, jeśli brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="43e1b-149">Jeśli adres *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="43e1b-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="43e1b-150">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="43e1b-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="43e1b-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="43e1b-151">-SubnetId</span></span>
<span data-ttu-id="43e1b-152">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="43e1b-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="43e1b-153">Określ ten parametr, jeśli brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="43e1b-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="43e1b-154">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="43e1b-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="43e1b-155">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="43e1b-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="43e1b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e1b-156">CommonParameters</span></span>
<span data-ttu-id="43e1b-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e1b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e1b-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43e1b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e1b-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43e1b-159">INPUTS</span></span>

### <span data-ttu-id="43e1b-160">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43e1b-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="43e1b-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43e1b-161">OUTPUTS</span></span>

### <span data-ttu-id="43e1b-162">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43e1b-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="43e1b-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43e1b-163">NOTES</span></span>

## <span data-ttu-id="43e1b-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43e1b-164">RELATED LINKS</span></span>

[<span data-ttu-id="43e1b-165">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="43e1b-166">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="43e1b-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="43e1b-168">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="43e1b-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="43e1b-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


