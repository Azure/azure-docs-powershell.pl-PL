---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240922"
---
# <span data-ttu-id="e7771-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7771-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e7771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7771-102">SYNOPSIS</span></span>
<span data-ttu-id="e7771-103">Tworzy konfigurację fronto strony ip dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="e7771-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7771-104">SYNTAX</span></span>

### <span data-ttu-id="e7771-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7771-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7771-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e7771-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7771-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7771-107">DESCRIPTION</span></span>
<span data-ttu-id="e7771-108">Polecenie **cmdlet New-AzApplicationGatewayFrontendIPConfig** tworzy konfigurację frontoronu IP dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="e7771-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="e7771-109">Brama aplikacji obsługuje dwa typy konfiguracji frontoronu IP:</span><span class="sxs-lookup"><span data-stu-id="e7771-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="e7771-110">Publiczne adresy IP — prywatne adresy IP z użyciem wewnętrznego równoważenia obciążenia (ILB).</span><span class="sxs-lookup"><span data-stu-id="e7771-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="e7771-111">Brama aplikacji może mieć co najwyżej jeden publiczny adres IP i jeden prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="e7771-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="e7771-112">Publiczny adres IP i prywatny adres IP należy dodawać oddzielnie jako adresy IP frontoronu.</span><span class="sxs-lookup"><span data-stu-id="e7771-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="e7771-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7771-113">EXAMPLES</span></span>

### <span data-ttu-id="e7771-114">Przykład 1. Tworzenie konfiguracji frontoronu adresu IP przy użyciu obiektu publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="e7771-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="e7771-115">Pierwsze polecenie tworzy publiczny obiekt zasobu IP i przechowuje go w $PublicIP zmienną.</span><span class="sxs-lookup"><span data-stu-id="e7771-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="e7771-116">Drugie polecenie używa $PublicIP do utworzenia nowej konfiguracji frontonu ip o nazwie FrontEndIP01 i przechowuje ją w $FrontEnd frontonu.</span><span class="sxs-lookup"><span data-stu-id="e7771-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="e7771-117">Przykład 2. Tworzenie statycznego prywatnego adresu IP jako adresu IP frontoronu</span><span class="sxs-lookup"><span data-stu-id="e7771-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="e7771-118">Pierwsze polecenie pobiera sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7771-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e7771-119">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="e7771-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e7771-120">Trzecie polecenie tworzy konfigurację frontonu ip o nazwie FrontEndIP02 przy użyciu drugiego polecenia i prywatnego adresu IP 10.0.1.1, $Subnet następnie zapisuje go w zmiennej $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="e7771-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="e7771-121">Przykład 3. Tworzenie dynamicznego prywatnego adresu IP jako adresu IP frontoronu</span><span class="sxs-lookup"><span data-stu-id="e7771-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="e7771-122">Pierwsze polecenie pobiera sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7771-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="e7771-123">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="e7771-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e7771-124">Trzecie polecenie tworzy konfigurację frontonu ip o nazwie FrontEndIP03, używając $Subnet drugiego polecenia i zapisuje ją w $FrontEnd danych.</span><span class="sxs-lookup"><span data-stu-id="e7771-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="e7771-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7771-125">PARAMETERS</span></span>

### <span data-ttu-id="e7771-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7771-126">-DefaultProfile</span></span>
<span data-ttu-id="e7771-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7771-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7771-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7771-128">-Name</span></span>
<span data-ttu-id="e7771-129">Określa nazwę konfiguracji frontoronu ip, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7771-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7771-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e7771-130">-PrivateIPAddress</span></span>
<span data-ttu-id="e7771-131">Określa prywatny adres IP, który to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="e7771-132">Tę wartość można określić tylko w przypadku, gdy jest określona podsieć.</span><span class="sxs-lookup"><span data-stu-id="e7771-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="e7771-133">Ten adres IP jest przydzielany statycznie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="e7771-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="e7771-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7771-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="e7771-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7771-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="e7771-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e7771-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="e7771-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e7771-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="e7771-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="e7771-138">-PublicIPAddress</span></span>
<span data-ttu-id="e7771-139">Określa publiczny obiekt adresu IP, który to polecenie cmdlet skojarzy z frontoniem adresu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7771-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e7771-140">-PublicIPAddressId</span></span>
<span data-ttu-id="e7771-141">Określa identyfikator publicznego adresu IP, który to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="e7771-142">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e7771-142">-Subnet</span></span>
<span data-ttu-id="e7771-143">Określa obiekt podsieci, którą to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="e7771-144">Określenie tego parametru oznacza, że brama korzysta z prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="e7771-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="e7771-145">Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do podsieci określonej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e7771-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="e7771-146">Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7771-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e7771-147">-SubnetId</span></span>
<span data-ttu-id="e7771-148">Określa identyfikator podsieci, którą to polecenie cmdlet skojarzy z konfiguracją frontoronu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="e7771-149">Określenie parametru *Podsieci* oznacza, że brama korzysta z prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="e7771-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="e7771-150">Jeśli parametr *PrivateIPAddress* jest określony, powinien on należeć do podsieci określonej przez *podsieć.*</span><span class="sxs-lookup"><span data-stu-id="e7771-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="e7771-151">Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e7771-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e7771-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7771-152">CommonParameters</span></span>
<span data-ttu-id="e7771-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7771-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7771-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7771-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7771-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7771-155">INPUTS</span></span>

### <span data-ttu-id="e7771-156">Brak</span><span class="sxs-lookup"><span data-stu-id="e7771-156">None</span></span>

## <span data-ttu-id="e7771-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7771-157">OUTPUTS</span></span>

### <span data-ttu-id="e7771-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7771-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="e7771-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7771-159">NOTES</span></span>

## <span data-ttu-id="e7771-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7771-160">RELATED LINKS</span></span>

[<span data-ttu-id="e7771-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7771-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7771-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7771-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7771-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7771-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e7771-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e7771-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


