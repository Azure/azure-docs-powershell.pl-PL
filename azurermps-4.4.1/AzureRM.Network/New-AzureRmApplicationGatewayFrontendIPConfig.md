---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6f5edd934e7239c8d4bb5083e5b4881fff79f489
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719278"
---
# <span data-ttu-id="ea90a-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ea90a-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ea90a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea90a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea90a-103">Tworzy konfigurację frontonu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea90a-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea90a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea90a-104">SYNTAX</span></span>

### <span data-ttu-id="ea90a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea90a-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea90a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ea90a-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea90a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea90a-107">DESCRIPTION</span></span>
<span data-ttu-id="ea90a-108">Polecenie cmdlet **New-AzureRmApplicationGatewayFrontendIPConfig** tworzy fronton IP configuraton dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea90a-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="ea90a-109">Brama Application Gateway obsługuje dwa typy konfiguracji frontonu IP:</span><span class="sxs-lookup"><span data-stu-id="ea90a-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="ea90a-110">Publiczne adresy IP — prywatne adresy IP przy użyciu wewnętrznego równoważenia obciążenia (ILB).</span><span class="sxs-lookup"><span data-stu-id="ea90a-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="ea90a-111">Brama Application Gateway może mieć co najwyżej jednego publicznego adresu IP i jednego prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ea90a-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="ea90a-112">Publiczny adres IP i prywatny adres IP należy dodać oddzielnie jako adresy IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="ea90a-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="ea90a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea90a-113">EXAMPLES</span></span>

### <span data-ttu-id="ea90a-114">Przykład 1. Tworzenie konfiguracji frontonu IP przy użyciu obiektu publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="ea90a-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="ea90a-115">Pierwsze polecenie powoduje utworzenie publicznego obiektu zasobu IP i zapisanie go w zmiennej $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="ea90a-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="ea90a-116">Drugie polecenie używa $PublicIP w celu utworzenia nowej konfiguracji adresu IP frontonu o nazwie FrontEndIP01 i zapisywania jej w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ea90a-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ea90a-117">Przykład 2. Tworzenie statycznego prywatnego adresu IP jako adresu IP frontonu</span><span class="sxs-lookup"><span data-stu-id="ea90a-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="ea90a-118">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="ea90a-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ea90a-119">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ea90a-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ea90a-120">Trzecie polecenie tworzy konfigurację frontonu IP o nazwie FrontEndIP02 przy użyciu $Subnet z drugiego polecenia i prywatnego adresu IP 10.0.1.1, a następnie zapisuje ją w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ea90a-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ea90a-121">Przykład 3: Tworzenie dynamicznego prywatnego adresu IP jako adresu IP frontonu</span><span class="sxs-lookup"><span data-stu-id="ea90a-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="ea90a-122">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="ea90a-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ea90a-123">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet z pierwszego polecenia i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ea90a-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ea90a-124">Trzecie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontEndIP03 przy użyciu $Subnet z drugiego polecenia i zapisuje ją w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ea90a-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="ea90a-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea90a-125">PARAMETERS</span></span>

### <span data-ttu-id="ea90a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea90a-126">-Name</span></span>
<span data-ttu-id="ea90a-127">Określa nazwę konfiguracji adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea90a-127">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ea90a-128">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ea90a-128">-PrivateIPAddress</span></span>
<span data-ttu-id="ea90a-129">Określa prywatny adres IP, który jest skojarzony z tym poleceniem z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-129">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ea90a-130">Tę wartość można określić tylko wtedy, gdy określono podsieć.</span><span class="sxs-lookup"><span data-stu-id="ea90a-130">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="ea90a-131">Ten adres IP jest statycznie przydzielony z podsieci.</span><span class="sxs-lookup"><span data-stu-id="ea90a-131">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="ea90a-132">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ea90a-132">-PublicIPAddress</span></span>
<span data-ttu-id="ea90a-133">Określa publiczny obiekt adresu IP, który jest skojarzony z tym poleceniem, z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-133">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ea90a-134">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ea90a-134">-PublicIPAddressId</span></span>
<span data-ttu-id="ea90a-135">Określa publiczny identyfikator IP, który jest skojarzony z frontonowym adresem IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-135">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="ea90a-136">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="ea90a-136">-Subnet</span></span>
<span data-ttu-id="ea90a-137">Określa obiekt podsieci, który jest skojarzony z tym poleceniem cmdlet z adresem IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-137">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ea90a-138">Jeśli określisz ten parametr, oznacza to, że brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ea90a-138">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ea90a-139">Jeśli parametr *PrivateIPAddresss* jest określony, powinien należeć do podsieci określonej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ea90a-139">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="ea90a-140">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-140">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ea90a-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ea90a-141">-SubnetId</span></span>
<span data-ttu-id="ea90a-142">Określa identyfikator podsieci, który jest skojarzony z tym poleceniem cmdlet z konfiguracją frontonu IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-142">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="ea90a-143">Jeśli określisz parametr *podsieci* , oznacza to, że brama używa prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ea90a-143">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ea90a-144">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do podsieci określonej przez *podsieć*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-144">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="ea90a-145">Jeśli nie podano *PrivateIPAddress* , każdy z adresów IP z tej podsieci jest dynamicznie wybierany jako frontonowy adres IP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea90a-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ea90a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea90a-146">-DefaultProfile</span></span>
<span data-ttu-id="ea90a-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea90a-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea90a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea90a-148">CommonParameters</span></span>
<span data-ttu-id="ea90a-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea90a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea90a-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea90a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea90a-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea90a-151">INPUTS</span></span>

### <span data-ttu-id="ea90a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ea90a-152">System.String</span></span>

## <span data-ttu-id="ea90a-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea90a-153">OUTPUTS</span></span>

### <span data-ttu-id="ea90a-154">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea90a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="ea90a-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea90a-155">NOTES</span></span>

## <span data-ttu-id="ea90a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea90a-156">RELATED LINKS</span></span>

[<span data-ttu-id="ea90a-157">Dodaj-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ea90a-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ea90a-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ea90a-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ea90a-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ea90a-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ea90a-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ea90a-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

