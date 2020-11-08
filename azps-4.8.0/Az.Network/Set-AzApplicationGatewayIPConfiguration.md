---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063326"
---
# <span data-ttu-id="cc085-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="cc085-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc085-102">SYNOPSIS</span></span>
<span data-ttu-id="cc085-103">Modyfikuje konfigurację IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc085-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="cc085-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc085-104">SYNTAX</span></span>

### <span data-ttu-id="cc085-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc085-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc085-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cc085-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc085-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc085-107">DESCRIPTION</span></span>
<span data-ttu-id="cc085-108">Polecenie cmdlet **Set-AzApplicationGatewayIPConfiguration** modyfikuje konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="cc085-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="cc085-109">Konfiguracja IP zawiera podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc085-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="cc085-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc085-110">EXAMPLES</span></span>

### <span data-ttu-id="cc085-111">Przykład 1: aktualizowanie konfiguracji adresów IP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cc085-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="cc085-112">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="cc085-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="cc085-113">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="cc085-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="cc085-114">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cc085-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cc085-115">Z poleceniem one ustawia konfigurację IP bramy Application Gateway przechowywaną w $AppGw do konfiguracji podsieci przechowywanej w $Subnet.</span><span class="sxs-lookup"><span data-stu-id="cc085-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="cc085-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc085-116">PARAMETERS</span></span>

### <span data-ttu-id="cc085-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc085-117">-ApplicationGateway</span></span>
<span data-ttu-id="cc085-118">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="cc085-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="cc085-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc085-119">-DefaultProfile</span></span>
<span data-ttu-id="cc085-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc085-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc085-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc085-121">-Name</span></span>
<span data-ttu-id="cc085-122">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="cc085-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="cc085-123">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="cc085-123">-Subnet</span></span>
<span data-ttu-id="cc085-124">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="cc085-124">Specifies the subnet.</span></span>
<span data-ttu-id="cc085-125">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc085-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="cc085-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc085-126">-SubnetId</span></span>
<span data-ttu-id="cc085-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="cc085-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="cc085-128">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc085-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="cc085-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc085-129">CommonParameters</span></span>
<span data-ttu-id="cc085-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc085-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc085-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc085-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc085-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc085-132">INPUTS</span></span>

### <span data-ttu-id="cc085-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc085-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc085-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc085-134">OUTPUTS</span></span>

### <span data-ttu-id="cc085-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc085-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc085-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc085-136">NOTES</span></span>

## <span data-ttu-id="cc085-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc085-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc085-138">Dodaj-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cc085-139">Dodaj-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cc085-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cc085-141">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cc085-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc085-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


