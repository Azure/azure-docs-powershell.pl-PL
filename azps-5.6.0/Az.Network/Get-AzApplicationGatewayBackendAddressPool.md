---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 458788041ce833cacb30616a7aa8268ed485c65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978321"
---
# <span data-ttu-id="b16fc-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b16fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b16fc-103">Pobiera pulę adresów końcowych dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b16fc-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="b16fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b16fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b16fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b16fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b16fc-106">Polecenie **cmdlet Get-AzApplicationGatewayBackendAddressPool pobiera** jedną lub więcej konfiguracji puli adresów zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b16fc-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="b16fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b16fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b16fc-108">Przykład 1. Uzyskiwanie określonej puli serwerów back-end</span><span class="sxs-lookup"><span data-stu-id="b16fc-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b16fc-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="b16fc-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b16fc-110">Drugie polecenie pobiera pulę adresów końcowych skojarzoną z programem $AppGw o nazwie Pool01 i przechowuje ją w $BackendPool zmienną.</span><span class="sxs-lookup"><span data-stu-id="b16fc-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="b16fc-111">Przykład 2. Uzyskiwanie listy puli serwerów back-end</span><span class="sxs-lookup"><span data-stu-id="b16fc-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="b16fc-112">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="b16fc-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b16fc-113">Drugie polecenie pobiera listę puli adresów back-end skojarzonych z programem $AppGw i zapisuje listę w zmiennej $BackendPools adresowej.</span><span class="sxs-lookup"><span data-stu-id="b16fc-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="b16fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b16fc-114">PARAMETERS</span></span>

### <span data-ttu-id="b16fc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b16fc-115">-ApplicationGateway</span></span>
<span data-ttu-id="b16fc-116">Polecenie **cmdlet Get-AzApplicationGatewayBackendAddressPool** pobiera pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b16fc-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="b16fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16fc-117">-DefaultProfile</span></span>
<span data-ttu-id="b16fc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b16fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16fc-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b16fc-119">-Name</span></span>
<span data-ttu-id="b16fc-120">Określa nazwę puli adresów back-end, która będzie pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b16fc-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b16fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16fc-121">CommonParameters</span></span>
<span data-ttu-id="b16fc-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16fc-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b16fc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16fc-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b16fc-124">INPUTS</span></span>

### <span data-ttu-id="b16fc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b16fc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b16fc-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b16fc-126">OUTPUTS</span></span>

### <span data-ttu-id="b16fc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b16fc-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b16fc-128">NOTES</span></span>

## <span data-ttu-id="b16fc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b16fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="b16fc-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b16fc-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b16fc-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b16fc-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b16fc-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


