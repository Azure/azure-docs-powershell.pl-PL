---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956785"
---
# <span data-ttu-id="1ca48-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="1ca48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ca48-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca48-103">Modyfikuje konfigurację frontoronowego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="1ca48-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ca48-104">SYNTAX</span></span>

### <span data-ttu-id="1ca48-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ca48-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ca48-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1ca48-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ca48-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ca48-107">DESCRIPTION</span></span>
<span data-ttu-id="1ca48-108">Polecenie **cmdlet Set-AzApplicationGatewayFrontendIPConfig** aktualizuje konfigurację frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="1ca48-109">Brama aplikacji obsługuje dwa typy adresów IP frontoronu:</span><span class="sxs-lookup"><span data-stu-id="1ca48-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="1ca48-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="1ca48-110">Public IP addresses</span></span>
- <span data-ttu-id="1ca48-111">Prywatne adresy IP, dla których w konfiguracji jest używane wewnętrzne równoważenie obciążenia (ILB, Internal Load Balancing) Brama aplikacji może mieć co najwyżej jeden publiczny adres IP i jeden prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="1ca48-112">Publiczny adres IP i prywatny adres IP powinny być dodawane oddzielnie jako frontowe adresy IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="1ca48-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ca48-113">EXAMPLES</span></span>

### <span data-ttu-id="1ca48-114">Przykład 1. Ustawianie publicznego adresu IP jako przedniego adresu IP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ca48-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="1ca48-115">Pierwsze polecenie tworzy publiczny obiekt adresu IP i przechowuje go w $PublicIp adresie.</span><span class="sxs-lookup"><span data-stu-id="1ca48-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="1ca48-116">Drugie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ca48-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ca48-117">Trzecie polecenie aktualizuje konfigurację frontoronu IP o nazwie FrontEndIp01 dla bramy w programie $AppGw przy użyciu adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="1ca48-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="1ca48-118">Przykład 2. Ustawianie statycznego prywatnego adresu IP jako przedniego adresu IP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ca48-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="1ca48-119">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ca48-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="1ca48-120">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="1ca48-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="1ca48-121">Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="1ca48-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ca48-122">Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="1ca48-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="1ca48-123">Przykład 3. Ustawianie dynamicznego prywatnego adresu IP jako przedniego adresu IP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ca48-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="1ca48-124">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ca48-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="1ca48-125">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="1ca48-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="1ca48-126">Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="1ca48-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ca48-127">Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="1ca48-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="1ca48-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ca48-128">PARAMETERS</span></span>

### <span data-ttu-id="1ca48-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca48-129">-ApplicationGateway</span></span>
<span data-ttu-id="1ca48-130">Określa obiekt bramy aplikacji, w którym ma być modyfikowana konfiguracja frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="1ca48-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca48-131">-DefaultProfile</span></span>
<span data-ttu-id="1ca48-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca48-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ca48-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1ca48-133">-Name</span></span>
<span data-ttu-id="1ca48-134">Określa nazwę konfiguracji frontoronu IP, która jest zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ca48-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1ca48-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="1ca48-135">-PrivateIPAddress</span></span>
<span data-ttu-id="1ca48-136">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-136">Specifies the private IP address.</span></span>
<span data-ttu-id="1ca48-137">Jeśli jest określony, ten adres IP jest przydzielany statycznie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ca48-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="1ca48-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ca48-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="1ca48-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ca48-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="1ca48-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1ca48-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="1ca48-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1ca48-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="1ca48-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="1ca48-142">-PublicIPAddress</span></span>
<span data-ttu-id="1ca48-143">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="1ca48-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1ca48-144">-PublicIPAddressId</span></span>
<span data-ttu-id="1ca48-145">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="1ca48-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="1ca48-146">-Subnet</span></span>
<span data-ttu-id="1ca48-147">Określa podsieć używaną przez bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ca48-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="1ca48-148">Określ ten parametr, jeśli brama korzysta z prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="1ca48-149">Jeśli określono *adres PrivateIPAddress,* powinien on należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ca48-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="1ca48-150">Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ca48-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1ca48-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1ca48-151">-SubnetId</span></span>
<span data-ttu-id="1ca48-152">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ca48-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="1ca48-153">Określ ten parametr, jeśli brama korzysta z prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="1ca48-154">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ca48-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="1ca48-155">Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ca48-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1ca48-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca48-156">CommonParameters</span></span>
<span data-ttu-id="1ca48-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca48-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca48-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ca48-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca48-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ca48-159">INPUTS</span></span>

### <span data-ttu-id="1ca48-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca48-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ca48-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ca48-161">OUTPUTS</span></span>

### <span data-ttu-id="1ca48-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ca48-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ca48-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ca48-163">NOTES</span></span>

## <span data-ttu-id="1ca48-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ca48-164">RELATED LINKS</span></span>

[<span data-ttu-id="1ca48-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1ca48-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1ca48-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1ca48-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1ca48-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1ca48-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


