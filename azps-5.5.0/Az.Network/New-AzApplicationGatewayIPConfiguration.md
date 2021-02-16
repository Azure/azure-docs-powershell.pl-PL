---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179730"
---
# <span data-ttu-id="5b595-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5b595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b595-102">SYNOPSIS</span></span>
<span data-ttu-id="5b595-103">Tworzy konfigurację adresu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="5b595-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b595-104">SYNTAX</span></span>

### <span data-ttu-id="5b595-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b595-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b595-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5b595-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b595-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b595-107">DESCRIPTION</span></span>
<span data-ttu-id="5b595-108">Polecenie **cmdlet New-AzApplicationGatewayIPConfiguration** tworzy konfigurację adresu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="5b595-109">Konfiguracja adresu IP zawiera podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="5b595-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b595-110">EXAMPLES</span></span>

### <span data-ttu-id="5b595-111">Przykład 1. Tworzenie konfiguracji protokołu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="5b595-112">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5b595-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="5b595-113">Drugie polecenie pobiera konfigurację podsieci dla podsieci, do której należy sieć wirtualna w poprzednim poleceniu, i przechowuje je w zmiennej $Subnet sieci.</span><span class="sxs-lookup"><span data-stu-id="5b595-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5b595-114">Trzecie polecenie tworzy konfigurację protokołu IP przy użyciu $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5b595-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="5b595-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b595-115">PARAMETERS</span></span>

### <span data-ttu-id="5b595-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b595-116">-DefaultProfile</span></span>
<span data-ttu-id="5b595-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b595-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b595-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5b595-118">-Name</span></span>
<span data-ttu-id="5b595-119">Określa nazwę konfiguracji protokołu IP do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="5b595-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="5b595-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="5b595-120">-Subnet</span></span>
<span data-ttu-id="5b595-121">Określa obiekt podsieci.</span><span class="sxs-lookup"><span data-stu-id="5b595-121">Specifies the subnet object.</span></span>
<span data-ttu-id="5b595-122">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="5b595-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5b595-123">-SubnetId</span></span>
<span data-ttu-id="5b595-124">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="5b595-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="5b595-125">Jest to podsieci, w której wdrożonoby bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b595-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="5b595-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b595-126">CommonParameters</span></span>
<span data-ttu-id="5b595-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b595-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b595-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b595-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b595-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b595-129">INPUTS</span></span>

### <span data-ttu-id="5b595-130">Brak</span><span class="sxs-lookup"><span data-stu-id="5b595-130">None</span></span>

## <span data-ttu-id="5b595-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b595-131">OUTPUTS</span></span>

### <span data-ttu-id="5b595-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5b595-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b595-133">NOTES</span></span>

## <span data-ttu-id="5b595-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b595-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b595-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5b595-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5b595-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5b595-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b595-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


