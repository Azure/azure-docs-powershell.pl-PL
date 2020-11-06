---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 013831c6b7b05a1da520744df9823076d95ccf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554041"
---
# <span data-ttu-id="2dabf-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2dabf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dabf-102">SYNOPSIS</span></span>
<span data-ttu-id="2dabf-103">Modyfikuje konfigurację IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2dabf-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dabf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dabf-104">SYNTAX</span></span>

### <span data-ttu-id="2dabf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2dabf-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dabf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2dabf-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dabf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2dabf-107">DESCRIPTION</span></span>
<span data-ttu-id="2dabf-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayIPConfiguration** modyfikuje konfigurację adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2dabf-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="2dabf-109">Konfiguracja IP zawiera podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2dabf-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="2dabf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dabf-110">EXAMPLES</span></span>

### <span data-ttu-id="2dabf-111">Przykład 1: Ustawianie stanu celu konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="2dabf-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="2dabf-112">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $VNet.</span><span class="sxs-lookup"><span data-stu-id="2dabf-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2dabf-113">Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01 przy użyciu $VNet i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2dabf-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2dabf-114">Trzecie polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2dabf-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2dabf-115">Z poleceniem one ustawia konfigurację IP bramy Application Gateway przechowywaną w $AppGw do konfiguracji podsieci przechowywanej w $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2dabf-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="2dabf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dabf-116">PARAMETERS</span></span>

### <span data-ttu-id="2dabf-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2dabf-117">-ApplicationGateway</span></span>
<span data-ttu-id="2dabf-118">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="2dabf-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="2dabf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dabf-119">-DefaultProfile</span></span>
<span data-ttu-id="2dabf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dabf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dabf-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2dabf-121">-Name</span></span>
<span data-ttu-id="2dabf-122">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2dabf-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="2dabf-123">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="2dabf-123">-Subnet</span></span>
<span data-ttu-id="2dabf-124">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="2dabf-124">Specifies the subnet.</span></span>
<span data-ttu-id="2dabf-125">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2dabf-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2dabf-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2dabf-126">-SubnetId</span></span>
<span data-ttu-id="2dabf-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="2dabf-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="2dabf-128">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2dabf-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2dabf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dabf-129">CommonParameters</span></span>
<span data-ttu-id="2dabf-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dabf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dabf-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dabf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dabf-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dabf-132">INPUTS</span></span>

### <span data-ttu-id="2dabf-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2dabf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="2dabf-134">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2dabf-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="2dabf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dabf-135">OUTPUTS</span></span>

### <span data-ttu-id="2dabf-136">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2dabf-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2dabf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dabf-137">NOTES</span></span>

## <span data-ttu-id="2dabf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dabf-138">RELATED LINKS</span></span>

[<span data-ttu-id="2dabf-139">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2dabf-140">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-140">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2dabf-141">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-141">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2dabf-142">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-142">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2dabf-143">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dabf-143">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


