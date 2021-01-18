---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499605"
---
# <span data-ttu-id="40cbd-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="40cbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="40cbd-103">Pobiera pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="40cbd-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="40cbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40cbd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40cbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40cbd-105">DESCRIPTION</span></span>
<span data-ttu-id="40cbd-106">Polecenie cmdlet **Get-AzApplicationGatewayBackendAddressPool umożliwia pobranie** jednej lub większej liczby konfiguracji puli adresów zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="40cbd-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="40cbd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40cbd-107">EXAMPLES</span></span>

### <span data-ttu-id="40cbd-108">Przykład 1: uzyskiwanie określonej puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="40cbd-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="40cbd-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="40cbd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="40cbd-110">Drugie polecenie pobiera pulę adresów zaplecza skojarzoną z $AppGw o nazwie Pool01 i zapisuje ją w zmiennej $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="40cbd-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="40cbd-111">Przykład 2: uzyskiwanie listy puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="40cbd-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="40cbd-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="40cbd-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="40cbd-113">Drugie polecenie pobiera listę pul adresów zaplecza skojarzonych z $AppGw i zapisuje listę w zmiennej $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="40cbd-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="40cbd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40cbd-114">PARAMETERS</span></span>

### <span data-ttu-id="40cbd-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40cbd-115">-ApplicationGateway</span></span>
<span data-ttu-id="40cbd-116">Polecenie cmdlet **Get-AzApplicationGatewayBackendAddressPool** pobiera pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="40cbd-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="40cbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cbd-117">-DefaultProfile</span></span>
<span data-ttu-id="40cbd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40cbd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40cbd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40cbd-119">-Name</span></span>
<span data-ttu-id="40cbd-120">Określa nazwę puli adresów zaplecza, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40cbd-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="40cbd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cbd-121">CommonParameters</span></span>
<span data-ttu-id="40cbd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cbd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cbd-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40cbd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cbd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40cbd-124">INPUTS</span></span>

### <span data-ttu-id="40cbd-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40cbd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40cbd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40cbd-126">OUTPUTS</span></span>

### <span data-ttu-id="40cbd-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="40cbd-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40cbd-128">NOTES</span></span>

## <span data-ttu-id="40cbd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40cbd-129">RELATED LINKS</span></span>

[<span data-ttu-id="40cbd-130">Dodaj-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="40cbd-131">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="40cbd-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="40cbd-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40cbd-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


