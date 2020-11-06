---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e5bbe82276cb356da1e5a66c45145c7daa1d8769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545007"
---
# <span data-ttu-id="7f722-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="7f722-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f722-102">SYNOPSIS</span></span>
<span data-ttu-id="7f722-103">Modyfikuje konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7f722-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f722-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f722-104">SYNTAX</span></span>

### <span data-ttu-id="7f722-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f722-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f722-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f722-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f722-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7f722-107">DESCRIPTION</span></span>
<span data-ttu-id="7f722-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayFrontendIPConfig** umożliwia zaktualizowanie konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7f722-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="7f722-109">Brama Application Gateway obsługuje dwa typy zewnętrznych adresów IP:</span><span class="sxs-lookup"><span data-stu-id="7f722-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="7f722-110">Publiczne adresy IP</span><span class="sxs-lookup"><span data-stu-id="7f722-110">Public IP addresses</span></span>
- <span data-ttu-id="7f722-111">Prywatne adresy IP, dla których konfiguracja używa wewnętrznego równoważenia obciążenia (ILB) Brama aplikacji może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="7f722-112">Publiczny adres IP i prywatny adres IP należy dodać oddzielnie jako adresy IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7f722-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="7f722-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f722-113">EXAMPLES</span></span>

### <span data-ttu-id="7f722-114">Przykład 1: Ustawianie publicznego adresu IP jako adresu IP frontonu bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7f722-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="7f722-115">Pierwsze polecenie tworzy obiekt publicznego adresu IP i zapisuje go w zmiennej $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="7f722-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="7f722-116">Drugie polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7f722-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f722-117">Trzecie polecenie aktualizuje konfigurację IP frontonu o nazwie FrontEndIp01 dla bramy w $AppGw przy użyciu adresu przechowywanego w $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="7f722-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="7f722-118">Przykład 2: Ustawianie statycznego prywatnego adresu IP jako adresu IP frontonu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7f722-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="7f722-119">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="7f722-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="7f722-120">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7f722-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7f722-121">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7f722-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f722-122">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="7f722-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="7f722-123">Przykład 3: Ustawianie dynamicznego prywatnego adresu IP jako frontonu IP bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7f722-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="7f722-124">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="7f722-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="7f722-125">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7f722-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7f722-126">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7f722-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f722-127">Czwarte polecenie dodaje konfigurację adresu IP frontonu o nazwie FrontendIP02 przy użyciu $Subnet z drugiego polecenia.</span><span class="sxs-lookup"><span data-stu-id="7f722-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="7f722-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f722-128">PARAMETERS</span></span>

### <span data-ttu-id="7f722-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f722-129">-ApplicationGateway</span></span>
<span data-ttu-id="7f722-130">Określa obiekt bramy aplikacji, w którym ma zostać zmodyfikowana konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f722-131">-DefaultProfile</span></span>
<span data-ttu-id="7f722-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f722-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f722-133">-Name</span></span>
<span data-ttu-id="7f722-134">Określa nazwę konfiguracji adresu IP frontonu, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="7f722-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7f722-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="7f722-135">-PrivateIPAddress</span></span>
<span data-ttu-id="7f722-136">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-136">Specifies the private IP address.</span></span>
<span data-ttu-id="7f722-137">Jeśli jest określony, ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="7f722-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="7f722-138">-PublicIPAddress</span></span>
<span data-ttu-id="7f722-139">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-139">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="7f722-140">-PublicIPAddressId</span></span>
<span data-ttu-id="7f722-141">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-141">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-142">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="7f722-142">-Subnet</span></span>
<span data-ttu-id="7f722-143">Określa podsieć, którą Brama applicationowa używa.</span><span class="sxs-lookup"><span data-stu-id="7f722-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="7f722-144">Określ ten parametr, jeśli brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="7f722-145">Jeśli adres *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="7f722-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="7f722-146">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f722-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7f722-147">-SubnetId</span></span>
<span data-ttu-id="7f722-148">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="7f722-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="7f722-149">Określ ten parametr, jeśli brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="7f722-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="7f722-150">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="7f722-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="7f722-151">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f722-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f722-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f722-152">CommonParameters</span></span>
<span data-ttu-id="7f722-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f722-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f722-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f722-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f722-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f722-155">INPUTS</span></span>

### <span data-ttu-id="7f722-156">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f722-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7f722-157">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f722-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7f722-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f722-158">OUTPUTS</span></span>

### <span data-ttu-id="7f722-159">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f722-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f722-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f722-160">NOTES</span></span>

## <span data-ttu-id="7f722-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f722-161">RELATED LINKS</span></span>

[<span data-ttu-id="7f722-162">Dodaj-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7f722-163">Dodaj-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7f722-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7f722-165">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7f722-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7f722-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


