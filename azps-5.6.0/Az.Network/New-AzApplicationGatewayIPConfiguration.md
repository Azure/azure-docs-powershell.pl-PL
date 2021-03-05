---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 6399843edfc8ee806693e0ddfee77952438f2d35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993812"
---
# <span data-ttu-id="4ede8-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4ede8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ede8-102">SYNOPSIS</span></span>
<span data-ttu-id="4ede8-103">Tworzy konfigurację adresu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="4ede8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ede8-104">SYNTAX</span></span>

### <span data-ttu-id="4ede8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ede8-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ede8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4ede8-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ede8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ede8-107">DESCRIPTION</span></span>
<span data-ttu-id="4ede8-108">Polecenie **cmdlet New-AzApplicationGatewayIPConfiguration** tworzy konfigurację protokołu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="4ede8-109">Konfiguracja adresu IP zawiera podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="4ede8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ede8-110">EXAMPLES</span></span>

### <span data-ttu-id="4ede8-111">Przykład 1. Tworzenie konfiguracji protokołu IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="4ede8-112">Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4ede8-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="4ede8-113">Drugie polecenie pobiera konfigurację podsieci dla podsieci, do której należy sieć wirtualna w poprzednim poleceniu, i przechowuje je w zmiennej $Subnet sieci.</span><span class="sxs-lookup"><span data-stu-id="4ede8-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4ede8-114">Trzecie polecenie tworzy konfigurację protokołu IP przy użyciu $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4ede8-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="4ede8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ede8-115">PARAMETERS</span></span>

### <span data-ttu-id="4ede8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ede8-116">-DefaultProfile</span></span>
<span data-ttu-id="4ede8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ede8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ede8-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ede8-118">-Name</span></span>
<span data-ttu-id="4ede8-119">Określa nazwę konfiguracji protokołu IP do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4ede8-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="4ede8-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4ede8-120">-Subnet</span></span>
<span data-ttu-id="4ede8-121">Określa obiekt podsieci.</span><span class="sxs-lookup"><span data-stu-id="4ede8-121">Specifies the subnet object.</span></span>
<span data-ttu-id="4ede8-122">Jest to podsieci, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4ede8-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4ede8-123">-SubnetId</span></span>
<span data-ttu-id="4ede8-124">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="4ede8-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="4ede8-125">Jest to podsieci, w której wdrożonoby bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ede8-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="4ede8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ede8-126">CommonParameters</span></span>
<span data-ttu-id="4ede8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ede8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ede8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ede8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ede8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ede8-129">INPUTS</span></span>

### <span data-ttu-id="4ede8-130">Brak</span><span class="sxs-lookup"><span data-stu-id="4ede8-130">None</span></span>

## <span data-ttu-id="4ede8-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ede8-131">OUTPUTS</span></span>

### <span data-ttu-id="4ede8-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4ede8-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ede8-133">NOTES</span></span>

## <span data-ttu-id="4ede8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ede8-134">RELATED LINKS</span></span>

[<span data-ttu-id="4ede8-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ede8-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ede8-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ede8-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ede8-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


