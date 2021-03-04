---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 17661a05a970a9661543220c35b122638ddbc524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982618"
---
# <span data-ttu-id="57ca0-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57ca0-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="57ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="57ca0-103">Dodaje konfigurację adresu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="57ca0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57ca0-104">SYNTAX</span></span>

### <span data-ttu-id="57ca0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="57ca0-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ca0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="57ca0-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ca0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="57ca0-107">DESCRIPTION</span></span>
<span data-ttu-id="57ca0-108">Polecenie **cmdlet Add-AzApplicationGatewayIPConfiguration** dodaje konfigurację adresu IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="57ca0-109">Konfiguracje adresów IP zawierają podsieci, w której jest wdrożona brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="57ca0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57ca0-110">EXAMPLES</span></span>

### <span data-ttu-id="57ca0-111">Przykład 1. Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="57ca0-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="57ca0-112">Pierwsze polecenie otrzymuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="57ca0-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="57ca0-113">Drugie polecenie otrzymuje podsieci przy użyciu wcześniej utworzonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57ca0-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="57ca0-114">Trzecie polecenie pobiera bramę aplikacji i przechowuje ją w zmiennej $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="57ca0-115">Czwarte polecenie dodaje konfigurację protokołu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="57ca0-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="57ca0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57ca0-116">PARAMETERS</span></span>

### <span data-ttu-id="57ca0-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57ca0-117">-ApplicationGateway</span></span>
<span data-ttu-id="57ca0-118">Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="57ca0-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="57ca0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ca0-119">-DefaultProfile</span></span>
<span data-ttu-id="57ca0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57ca0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ca0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57ca0-121">-Name</span></span>
<span data-ttu-id="57ca0-122">Określa nazwę konfiguracji protokołu IP do dodania.</span><span class="sxs-lookup"><span data-stu-id="57ca0-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="57ca0-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="57ca0-123">-Subnet</span></span>
<span data-ttu-id="57ca0-124">Określa podsieci.</span><span class="sxs-lookup"><span data-stu-id="57ca0-124">Specifies a subnet.</span></span>
<span data-ttu-id="57ca0-125">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="57ca0-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="57ca0-126">-SubnetId</span></span>
<span data-ttu-id="57ca0-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="57ca0-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="57ca0-128">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ca0-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="57ca0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ca0-129">CommonParameters</span></span>
<span data-ttu-id="57ca0-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ca0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ca0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ca0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ca0-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ca0-132">INPUTS</span></span>

### <span data-ttu-id="57ca0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57ca0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57ca0-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ca0-134">OUTPUTS</span></span>

### <span data-ttu-id="57ca0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57ca0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57ca0-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57ca0-136">NOTES</span></span>

## <span data-ttu-id="57ca0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ca0-137">RELATED LINKS</span></span>

[<span data-ttu-id="57ca0-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57ca0-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="57ca0-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57ca0-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="57ca0-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57ca0-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="57ca0-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57ca0-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


