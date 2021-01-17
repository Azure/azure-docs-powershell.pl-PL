---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359200"
---
# <span data-ttu-id="729e7-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="729e7-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="729e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="729e7-102">SYNOPSIS</span></span>
<span data-ttu-id="729e7-103">Tworzy konfigurację frontonu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="729e7-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="729e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="729e7-104">SYNTAX</span></span>

### <span data-ttu-id="729e7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="729e7-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="729e7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="729e7-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="729e7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="729e7-107">DESCRIPTION</span></span>
<span data-ttu-id="729e7-108">Polecenie cmdlet **New-AzApplicationGatewayFrontendIPConfig** tworzy konfigurację frontonu IP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="729e7-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="729e7-109">Brama Application Gateway obsługuje dwa typy konfiguracji frontonu IP:</span><span class="sxs-lookup"><span data-stu-id="729e7-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="729e7-110">Publiczne adresy IP — prywatne adresy IP przy użyciu wewnętrznego równoważenia obciążenia (ILB).</span><span class="sxs-lookup"><span data-stu-id="729e7-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="729e7-111">Brama Application Gateway może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="729e7-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="729e7-112">Publiczny adres IP i prywatny adres IP należy dodać oddzielnie jako adresy IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="729e7-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="729e7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="729e7-113">EXAMPLES</span></span>

### <span data-ttu-id="729e7-114">Przykład 1. Tworzenie konfiguracji frontonu IP przy użyciu obiektu publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="729e7-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="729e7-115">Pierwsze polecenie powoduje utworzenie publicznego obiektu zasobu IP i zapisanie go w zmiennej $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="729e7-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="729e7-116">Drugie polecenie używa $PublicIP w celu utworzenia nowej konfiguracji adresu IP frontonu o nazwie FrontEndIP01 i zapisywania jej w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="729e7-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="729e7-117">Przykład 2. Tworzenie statycznego prywatnego adresu IP jako adresu IP frontonu</span><span class="sxs-lookup"><span data-stu-id="729e7-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="729e7-118">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="729e7-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="729e7-119">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="729e7-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="729e7-120">Trzecie polecenie tworzy konfigurację frontonu IP o nazwie FrontEndIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1, a następnie zapisuje ją w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="729e7-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="729e7-121">Przykład 3: Tworzenie dynamicznego prywatnego adresu IP jako adresu IP frontonu</span><span class="sxs-lookup"><span data-stu-id="729e7-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="729e7-122">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="729e7-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="729e7-123">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="729e7-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="729e7-124">Trzecie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontEndIP03 przy użyciu $Subnet z drugiego polecenia i zapisuje ją w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="729e7-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="729e7-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="729e7-125">PARAMETERS</span></span>

### <span data-ttu-id="729e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729e7-126">-DefaultProfile</span></span>
<span data-ttu-id="729e7-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="729e7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="729e7-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="729e7-128">-Name</span></span>
<span data-ttu-id="729e7-129">Określa nazwę konfiguracji adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="729e7-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="729e7-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="729e7-130">-PrivateIPAddress</span></span>
<span data-ttu-id="729e7-131">Określa prywatny adres IP, który jest skojarzony z tym poleceniem z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="729e7-132">Tę wartość można określić tylko wtedy, gdy określono podsieć.</span><span class="sxs-lookup"><span data-stu-id="729e7-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="729e7-133">Ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="729e7-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="729e7-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="729e7-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="729e7-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="729e7-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="729e7-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="729e7-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="729e7-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="729e7-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="729e7-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="729e7-138">-PublicIPAddress</span></span>
<span data-ttu-id="729e7-139">Określa publiczny obiekt adresu IP, który jest skojarzony z tym poleceniem, z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="729e7-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="729e7-140">-PublicIPAddressId</span></span>
<span data-ttu-id="729e7-141">Określa publiczny identyfikator IP, który jest skojarzony z frontonowym adresem IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="729e7-142">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="729e7-142">-Subnet</span></span>
<span data-ttu-id="729e7-143">Określa obiekt podsieci, który jest skojarzony z tym poleceniem cmdlet z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="729e7-144">Jeśli określisz ten parametr, oznacza to, że brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="729e7-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="729e7-145">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do podsieci określonej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="729e7-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="729e7-146">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="729e7-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="729e7-147">-SubnetId</span></span>
<span data-ttu-id="729e7-148">Określa identyfikator podsieci, który jest skojarzony z tym poleceniem cmdlet z konfiguracją frontonu IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="729e7-149">Jeśli określisz parametr *podsieci* , oznacza to, że brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="729e7-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="729e7-150">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do podsieci określonej przez *podsieć*.</span><span class="sxs-lookup"><span data-stu-id="729e7-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="729e7-151">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="729e7-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="729e7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729e7-152">CommonParameters</span></span>
<span data-ttu-id="729e7-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729e7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729e7-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="729e7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729e7-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="729e7-155">INPUTS</span></span>

### <span data-ttu-id="729e7-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="729e7-156">None</span></span>

## <span data-ttu-id="729e7-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="729e7-157">OUTPUTS</span></span>

### <span data-ttu-id="729e7-158">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="729e7-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="729e7-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="729e7-159">NOTES</span></span>

## <span data-ttu-id="729e7-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="729e7-160">RELATED LINKS</span></span>

[<span data-ttu-id="729e7-161">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="729e7-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="729e7-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="729e7-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="729e7-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="729e7-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="729e7-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="729e7-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


