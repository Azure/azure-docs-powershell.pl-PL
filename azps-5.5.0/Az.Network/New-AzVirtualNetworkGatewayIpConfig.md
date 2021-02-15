---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202702"
---
# <span data-ttu-id="6cd56-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd56-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="6cd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd56-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd56-103">Tworzy konfigurację adresu IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6cd56-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="6cd56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cd56-104">SYNTAX</span></span>

### <span data-ttu-id="6cd56-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6cd56-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cd56-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6cd56-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cd56-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cd56-107">DESCRIPTION</span></span>
<span data-ttu-id="6cd56-108">Polecenie cmdlet **New-AzVirtualNetworkGatewayIpConfig** tworzy konfigurację przypisaną do wirtualnej bramy sieciowej z (utworzonym wcześniej) publicznym adresem IP na podstawie identyfikatora podsieci.</span><span class="sxs-lookup"><span data-stu-id="6cd56-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="6cd56-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cd56-109">EXAMPLES</span></span>

### <span data-ttu-id="6cd56-110">1. Tworzenie konfiguracji protokołu IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6cd56-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="6cd56-111">Konfiguruje wirtualną bramę sieciową z publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="6cd56-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="6cd56-112">Zmienna $myGWsubnet jest uzyskiwana za pomocą polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** w "GatewaySubnet" w obrębie sieci wirtualnej, w przypadku których zamierzasz utworzyć wirtualną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="6cd56-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="6cd56-113">Zmienna $myGWpip jest uzyskiwana za pomocą polecenia **cmdlet New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="6cd56-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="6cd56-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cd56-114">PARAMETERS</span></span>

### <span data-ttu-id="6cd56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd56-115">-DefaultProfile</span></span>
<span data-ttu-id="6cd56-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd56-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6cd56-117">-Name</span></span>
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

### <span data-ttu-id="6cd56-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6cd56-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="6cd56-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6cd56-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="6cd56-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6cd56-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="6cd56-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6cd56-121">-Subnet</span></span>
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

### <span data-ttu-id="6cd56-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6cd56-122">-SubnetId</span></span>
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

### <span data-ttu-id="6cd56-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd56-123">CommonParameters</span></span>
<span data-ttu-id="6cd56-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd56-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd56-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd56-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd56-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cd56-126">INPUTS</span></span>

### <span data-ttu-id="6cd56-127">Brak</span><span class="sxs-lookup"><span data-stu-id="6cd56-127">None</span></span>

## <span data-ttu-id="6cd56-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cd56-128">OUTPUTS</span></span>

### <span data-ttu-id="6cd56-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cd56-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="6cd56-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cd56-130">NOTES</span></span>

## <span data-ttu-id="6cd56-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cd56-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cd56-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd56-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="6cd56-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd56-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
