---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 32e8671267efddd94252e592de45cb014b5dd0de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967978"
---
# <span data-ttu-id="fb8fd-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb8fd-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fb8fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8fd-103">Dodaje konfigurację frontoronu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="fb8fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb8fd-104">SYNTAX</span></span>

### <span data-ttu-id="fb8fd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb8fd-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb8fd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fb8fd-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb8fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb8fd-107">DESCRIPTION</span></span>
<span data-ttu-id="fb8fd-108">Polecenie **cmdlet Add-AzApplicationGatewayFrontendIPConfig** dodaje konfigurację frontoronu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="fb8fd-109">Brama aplikacji obsługuje dwa typy konfiguracji frontoronu IP:</span><span class="sxs-lookup"><span data-stu-id="fb8fd-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="fb8fd-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="fb8fd-110">Public IP addresses</span></span>
- <span data-ttu-id="fb8fd-111">Prywatne adresy IP używające wewnętrznego równoważenia obciążenia (ILB) Brama aplikacji może mieć co najwyżej jeden publiczny adres IP i jeden prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="fb8fd-112">Dodaj publiczny adres IP i prywatny adres IP jako osobne front frontowe adresy IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="fb8fd-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb8fd-113">EXAMPLES</span></span>

### <span data-ttu-id="fb8fd-114">Przykład 1. Dodawanie publicznego adresu IP jako adresu IP frontoronu</span><span class="sxs-lookup"><span data-stu-id="fb8fd-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="fb8fd-115">Pierwsze polecenie tworzy publiczny obiekt adresu IP i przechowuje go w $PublicIp adresie.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="fb8fd-116">Drugie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fb8fd-117">Trzecie polecenie dodaje konfigurację frontoronu IP o nazwie FrontEndIp01, dla bramy w programie $AppGw, używając adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="fb8fd-118">Przykład 2. Dodawanie statycznego prywatnego adresu IP jako adresu IP frontoronu</span><span class="sxs-lookup"><span data-stu-id="fb8fd-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="fb8fd-119">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fb8fd-120">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fb8fd-121">Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fb8fd-122">Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="fb8fd-123">Przykład 3. Dodawanie dynamicznego prywatnego adresu IP jako adresu IP frontoronu</span><span class="sxs-lookup"><span data-stu-id="fb8fd-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="fb8fd-124">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fb8fd-125">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fb8fd-126">Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fb8fd-127">Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="fb8fd-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb8fd-128">PARAMETERS</span></span>

### <span data-ttu-id="fb8fd-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb8fd-129">-ApplicationGateway</span></span>
<span data-ttu-id="fb8fd-130">Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="fb8fd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8fd-131">-DefaultProfile</span></span>
<span data-ttu-id="fb8fd-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8fd-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb8fd-133">-Name</span></span>
<span data-ttu-id="fb8fd-134">Określa nazwę konfiguracji frontoronu IP do dodania.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="fb8fd-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="fb8fd-135">-PrivateIPAddress</span></span>
<span data-ttu-id="fb8fd-136">Określa prywatny adres IP do dodania jako fronto endowy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="fb8fd-137">Jeśli jest określony, ten adres IP jest przydzielany statycznie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="fb8fd-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb8fd-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="fb8fd-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb8fd-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="fb8fd-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fb8fd-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="fb8fd-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fb8fd-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="fb8fd-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="fb8fd-142">-PublicIPAddress</span></span>
<span data-ttu-id="fb8fd-143">Określa publiczny adres IP, który to polecenie cmdlet dodaje jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="fb8fd-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fb8fd-144">-PublicIPAddressId</span></span>
<span data-ttu-id="fb8fd-145">Określa identyfikator publicznego adresu IP, który to polecenie cmdlet dodaje jako adres IP frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="fb8fd-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="fb8fd-146">-Subnet</span></span>
<span data-ttu-id="fb8fd-147">Określa podsieci, którą to polecenie cmdlet dodaje jako konfigurację frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="fb8fd-148">Określenie tego parametru oznacza, że brama aplikacji obsługuje prywatną konfigurację opartą na adresie IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="fb8fd-149">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="fb8fd-150">Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fb8fd-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fb8fd-151">-SubnetId</span></span>
<span data-ttu-id="fb8fd-152">Określa identyfikator podsieci, którą to polecenie cmdlet dodaje jako konfigurację frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="fb8fd-153">Przechodząca podsieci oznacza prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="fb8fd-154">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="fb8fd-155">W przeciwnym razie jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="fb8fd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8fd-156">CommonParameters</span></span>
<span data-ttu-id="fb8fd-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8fd-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb8fd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8fd-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb8fd-159">INPUTS</span></span>

### <span data-ttu-id="fb8fd-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb8fd-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb8fd-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb8fd-161">OUTPUTS</span></span>

### <span data-ttu-id="fb8fd-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb8fd-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb8fd-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb8fd-163">NOTES</span></span>

## <span data-ttu-id="fb8fd-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb8fd-164">RELATED LINKS</span></span>

[<span data-ttu-id="fb8fd-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb8fd-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb8fd-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb8fd-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb8fd-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb8fd-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb8fd-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb8fd-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


