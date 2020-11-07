---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898402"
---
# <span data-ttu-id="13d37-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="13d37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13d37-102">SYNOPSIS</span></span>
<span data-ttu-id="13d37-103">Pobiera pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13d37-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13d37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13d37-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d37-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13d37-105">DESCRIPTION</span></span>

## <span data-ttu-id="13d37-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13d37-106">EXAMPLES</span></span>

### <span data-ttu-id="13d37-107">Przykład 1: uzyskiwanie określonej puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="13d37-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="13d37-108">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="13d37-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13d37-109">Drugie polecenie pobiera pulę adresów zaplecza skojarzoną z $AppGw o nazwie Pool01 i zapisuje ją w zmiennej $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="13d37-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="13d37-110">Przykład 2: uzyskiwanie listy puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="13d37-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="13d37-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="13d37-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13d37-112">Drugie polecenie pobiera listę pul adresów zaplecza skojarzonych z $AppGw i zapisuje listę w zmiennej $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="13d37-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="13d37-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13d37-113">PARAMETERS</span></span>

### <span data-ttu-id="13d37-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13d37-114">-ApplicationGateway</span></span>
<span data-ttu-id="13d37-115">Polecenie cmdlet **Get-AzureRmApplicationGatewayBackendAddressPool** pobiera pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13d37-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d37-116">-DefaultProfile</span></span>
<span data-ttu-id="13d37-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13d37-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d37-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13d37-118">-Name</span></span>
<span data-ttu-id="13d37-119">Określa nazwę puli adresów zaplecza, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d37-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d37-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d37-120">CommonParameters</span></span>
<span data-ttu-id="13d37-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13d37-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d37-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d37-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d37-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13d37-123">INPUTS</span></span>

### <span data-ttu-id="13d37-124">System. String</span><span class="sxs-lookup"><span data-stu-id="13d37-124">System.String</span></span>

## <span data-ttu-id="13d37-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13d37-125">OUTPUTS</span></span>

### <span data-ttu-id="13d37-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="13d37-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13d37-127">NOTES</span></span>

## <span data-ttu-id="13d37-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13d37-128">RELATED LINKS</span></span>

[<span data-ttu-id="13d37-129">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="13d37-130">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="13d37-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="13d37-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13d37-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


