---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003482"
---
# <span data-ttu-id="dc326-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="dc326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc326-102">SYNOPSIS</span></span>
<span data-ttu-id="dc326-103">Modyfikuje konfigurację protokołu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc326-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="dc326-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc326-104">SYNTAX</span></span>

### <span data-ttu-id="dc326-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc326-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc326-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dc326-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc326-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc326-107">DESCRIPTION</span></span>
<span data-ttu-id="dc326-108">Polecenie **cmdlet Set-AzApplicationGatewayIPConfiguration** modyfikuje konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="dc326-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="dc326-109">Konfiguracja adresu IP zawiera podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc326-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="dc326-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc326-110">EXAMPLES</span></span>

### <span data-ttu-id="dc326-111">Przykład 1. Aktualizowanie konfiguracji protokołu IP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="dc326-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="dc326-112">Pierwsze polecenie pobiera sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $VNet zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc326-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="dc326-113">Drugie polecenie pobiera konfigurację podsieci o nazwie Podsieci01 przy użyciu $VNet i przechowuje je w $Subnet sieci.</span><span class="sxs-lookup"><span data-stu-id="dc326-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="dc326-114">Trzecie polecenie otrzymuje bramę aplikacji o nazwie ApplicationGateway01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc326-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dc326-115">To polecenie ustawia konfigurację adresów IP bramy aplikacji przechowywaną w programie $AppGw na konfigurację podsieci przechowywaną w $Subnet.</span><span class="sxs-lookup"><span data-stu-id="dc326-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="dc326-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc326-116">PARAMETERS</span></span>

### <span data-ttu-id="dc326-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc326-117">-ApplicationGateway</span></span>
<span data-ttu-id="dc326-118">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet skojarzy konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="dc326-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="dc326-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc326-119">-DefaultProfile</span></span>
<span data-ttu-id="dc326-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc326-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc326-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc326-121">-Name</span></span>
<span data-ttu-id="dc326-122">Określa nazwę konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="dc326-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="dc326-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dc326-123">-Subnet</span></span>
<span data-ttu-id="dc326-124">Określa podsieci.</span><span class="sxs-lookup"><span data-stu-id="dc326-124">Specifies the subnet.</span></span>
<span data-ttu-id="dc326-125">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc326-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="dc326-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dc326-126">-SubnetId</span></span>
<span data-ttu-id="dc326-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="dc326-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="dc326-128">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc326-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="dc326-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc326-129">CommonParameters</span></span>
<span data-ttu-id="dc326-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc326-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc326-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc326-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc326-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc326-132">INPUTS</span></span>

### <span data-ttu-id="dc326-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc326-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc326-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc326-134">OUTPUTS</span></span>

### <span data-ttu-id="dc326-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc326-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc326-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc326-136">NOTES</span></span>

## <span data-ttu-id="dc326-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc326-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc326-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc326-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc326-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc326-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc326-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc326-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


