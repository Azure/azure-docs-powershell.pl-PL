---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190002"
---
# <span data-ttu-id="eb21a-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb21a-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="eb21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb21a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb21a-103">Dodaje konfigurację adresu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="eb21a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb21a-104">SYNTAX</span></span>

### <span data-ttu-id="eb21a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb21a-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb21a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="eb21a-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb21a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb21a-107">DESCRIPTION</span></span>
<span data-ttu-id="eb21a-108">Polecenie **cmdlet Add-AzApplicationGatewayIPConfiguration** dodaje konfigurację adresu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="eb21a-109">Konfiguracje adresów IP zawierają podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="eb21a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb21a-110">EXAMPLES</span></span>

### <span data-ttu-id="eb21a-111">Przykład 1. Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="eb21a-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="eb21a-112">Pierwsze polecenie otrzymuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="eb21a-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="eb21a-113">Drugie polecenie otrzymuje podsieci przy użyciu wcześniej utworzonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eb21a-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="eb21a-114">Trzecie polecenie pobiera bramę aplikacji i przechowuje ją w zmiennej $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eb21a-115">Czwarte polecenie dodaje konfigurację protokołu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="eb21a-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="eb21a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb21a-116">PARAMETERS</span></span>

### <span data-ttu-id="eb21a-117">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb21a-117">-ApplicationGateway</span></span>
<span data-ttu-id="eb21a-118">Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="eb21a-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="eb21a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb21a-119">-DefaultProfile</span></span>
<span data-ttu-id="eb21a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb21a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb21a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eb21a-121">-Name</span></span>
<span data-ttu-id="eb21a-122">Określa nazwę konfiguracji protokołu IP do dodania.</span><span class="sxs-lookup"><span data-stu-id="eb21a-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="eb21a-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="eb21a-123">-Subnet</span></span>
<span data-ttu-id="eb21a-124">Określa podsieci.</span><span class="sxs-lookup"><span data-stu-id="eb21a-124">Specifies a subnet.</span></span>
<span data-ttu-id="eb21a-125">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="eb21a-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="eb21a-126">-SubnetId</span></span>
<span data-ttu-id="eb21a-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="eb21a-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="eb21a-128">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eb21a-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="eb21a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb21a-129">CommonParameters</span></span>
<span data-ttu-id="eb21a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb21a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb21a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb21a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb21a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb21a-132">INPUTS</span></span>

### <span data-ttu-id="eb21a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb21a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb21a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb21a-134">OUTPUTS</span></span>

### <span data-ttu-id="eb21a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb21a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb21a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb21a-136">NOTES</span></span>

## <span data-ttu-id="eb21a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb21a-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb21a-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb21a-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="eb21a-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb21a-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="eb21a-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb21a-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="eb21a-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb21a-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


