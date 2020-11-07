---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 429390258a793939742ba61792855c2c43ac044a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717735"
---
# <span data-ttu-id="b0900-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0900-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b0900-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0900-102">SYNOPSIS</span></span>
<span data-ttu-id="b0900-103">Dodaje konfigurację frontonu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0900-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0900-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0900-104">SYNTAX</span></span>

### <span data-ttu-id="b0900-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0900-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0900-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b0900-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0900-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b0900-107">DESCRIPTION</span></span>
<span data-ttu-id="b0900-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayFrontendIPConfig** umożliwia dodanie konfiguracji frontonu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0900-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="b0900-109">Brama Application Gateway obsługuje dwa typy konfiguracji frontonu IP:</span><span class="sxs-lookup"><span data-stu-id="b0900-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="b0900-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="b0900-110">Public IP addresses</span></span>
- <span data-ttu-id="b0900-111">Prywatne adresy IP przy użyciu wewnętrznego równoważenia obciążenia (ILB)</span><span class="sxs-lookup"><span data-stu-id="b0900-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="b0900-112">Brama Application Gateway może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="b0900-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="b0900-113">Dodaj publiczny adres IP i prywatny adres IP jako oddzielne zewnętrzne adresy IP.</span><span class="sxs-lookup"><span data-stu-id="b0900-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="b0900-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0900-114">EXAMPLES</span></span>

### <span data-ttu-id="b0900-115">Przykład 1: Dodawanie publicznego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="b0900-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="b0900-116">Pierwsze polecenie tworzy obiekt publicznego adresu IP i zapisuje go w zmiennej $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b0900-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="b0900-117">Drugie polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b0900-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b0900-118">Trzecie polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontEndIp01 dla bramy w $AppGw przy użyciu adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b0900-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="b0900-119">Przykład 2: dodanie statycznego prywatnego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="b0900-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="b0900-120">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="b0900-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b0900-121">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b0900-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b0900-122">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b0900-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b0900-123">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="b0900-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="b0900-124">Przykład 3: dodanie dynamicznego prywatnego adresu IP jako frontonu IP</span><span class="sxs-lookup"><span data-stu-id="b0900-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="b0900-125">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="b0900-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b0900-126">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b0900-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b0900-127">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b0900-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b0900-128">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="b0900-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="b0900-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0900-129">PARAMETERS</span></span>

### <span data-ttu-id="b0900-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0900-130">-ApplicationGateway</span></span>
<span data-ttu-id="b0900-131">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b0900-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b0900-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0900-132">-DefaultProfile</span></span>
<span data-ttu-id="b0900-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0900-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0900-134">-Name</span></span>
<span data-ttu-id="b0900-135">Określa nazwę konfiguracji adresu IP frontonu do dodania.</span><span class="sxs-lookup"><span data-stu-id="b0900-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="b0900-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="b0900-136">-PrivateIPAddress</span></span>
<span data-ttu-id="b0900-137">Określa prywatny adres IP, który ma zostać dodany jako fronton IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0900-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="b0900-138">Jeśli jest określony, ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0900-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="b0900-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b0900-139">-PublicIPAddress</span></span>
<span data-ttu-id="b0900-140">Określa publiczny adres IP, który to polecenie cmdlet dodaje jako adres IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0900-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="b0900-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="b0900-141">-PublicIPAddressId</span></span>
<span data-ttu-id="b0900-142">Określa identyfikator publicznego adresu IP, który jest dodawany przez to polecenie cmdlet jako adres IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b0900-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="b0900-143">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="b0900-143">-Subnet</span></span>
<span data-ttu-id="b0900-144">Określa podsieć, którą to polecenie cmdlet dodaje jako konfigurację frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="b0900-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="b0900-145">Określenie tego parametru oznacza, że brama Application Gateway obsługuje prywatną konfigurację IP opartą na konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b0900-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="b0900-146">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0900-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b0900-147">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b0900-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b0900-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b0900-148">-SubnetId</span></span>
<span data-ttu-id="b0900-149">Określa identyfikator podsieci, który jest dodawany przez ten aplet polecenia jako konfigurację frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="b0900-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="b0900-150">Przekazanie podsieci oznacza prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="b0900-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="b0900-151">Jeśli parametr *PrivateIPAddresss* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b0900-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b0900-152">W przeciwnym razie dowolny z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b0900-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="b0900-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0900-153">CommonParameters</span></span>
<span data-ttu-id="b0900-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0900-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0900-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0900-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0900-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0900-156">INPUTS</span></span>

### <span data-ttu-id="b0900-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b0900-157">System.String</span></span>

## <span data-ttu-id="b0900-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0900-158">OUTPUTS</span></span>

### <span data-ttu-id="b0900-159">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0900-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b0900-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0900-160">NOTES</span></span>

## <span data-ttu-id="b0900-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0900-161">RELATED LINKS</span></span>

[<span data-ttu-id="b0900-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0900-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0900-163">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0900-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0900-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0900-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0900-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0900-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


