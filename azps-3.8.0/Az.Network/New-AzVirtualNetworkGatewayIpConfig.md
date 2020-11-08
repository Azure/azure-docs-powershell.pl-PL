---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052196"
---
# <span data-ttu-id="d2870-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2870-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d2870-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2870-102">SYNOPSIS</span></span>
<span data-ttu-id="d2870-103">Tworzy konfigurację IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d2870-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="d2870-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2870-104">SYNTAX</span></span>

### <span data-ttu-id="d2870-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2870-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2870-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d2870-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2870-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2870-107">DESCRIPTION</span></span>
<span data-ttu-id="d2870-108">Polecenie cmdlet **New-AzVirtualNetworkGatewayIpConfig** tworzy konfigurację przypisaną do bramy sieci wirtualnej za pomocą (utworzonego wcześniej) publicznego adresu IP na podstawie identyfikatora podsieci.</span><span class="sxs-lookup"><span data-stu-id="d2870-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="d2870-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2870-109">EXAMPLES</span></span>

### <span data-ttu-id="d2870-110">1: Tworzenie konfiguracji adresów IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d2870-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="d2870-111">Konfiguruje wirtualną bramę sieciową z publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="d2870-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="d2870-112">Zmienna $myGWsubnet jest uzyskiwana przy użyciu polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** na "GatewaySubnet" w sieci wirtualnej, w której zamierzasz utworzyć wirtualną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="d2870-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="d2870-113">Zmienna $myGWpip jest uzyskiwana przy użyciu polecenia cmdlet **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="d2870-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="d2870-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2870-114">PARAMETERS</span></span>

### <span data-ttu-id="d2870-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2870-115">-DefaultProfile</span></span>
<span data-ttu-id="d2870-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2870-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2870-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2870-117">-Name</span></span>
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

### <span data-ttu-id="d2870-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d2870-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="d2870-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d2870-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="d2870-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d2870-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="d2870-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="d2870-121">-Subnet</span></span>
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

### <span data-ttu-id="d2870-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d2870-122">-SubnetId</span></span>
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

### <span data-ttu-id="d2870-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2870-123">CommonParameters</span></span>
<span data-ttu-id="d2870-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2870-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2870-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2870-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2870-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2870-126">INPUTS</span></span>

### <span data-ttu-id="d2870-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2870-127">None</span></span>

## <span data-ttu-id="d2870-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2870-128">OUTPUTS</span></span>

### <span data-ttu-id="d2870-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2870-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="d2870-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2870-130">NOTES</span></span>

## <span data-ttu-id="d2870-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2870-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2870-132">Dodaj-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2870-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d2870-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2870-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
