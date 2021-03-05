---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994064"
---
# <span data-ttu-id="986d2-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="986d2-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="986d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986d2-102">SYNOPSIS</span></span>
<span data-ttu-id="986d2-103">Pobiera sku bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="986d2-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="986d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="986d2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="986d2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="986d2-105">DESCRIPTION</span></span>
<span data-ttu-id="986d2-106">Polecenie **cmdlet Get-AzApplicationGatewaySku** pobiera jednostkę przechowywania akcji (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="986d2-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="986d2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="986d2-107">EXAMPLES</span></span>

### <span data-ttu-id="986d2-108">Przykład 1. Uzyskiwanie sKU bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="986d2-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="986d2-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="986d2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="986d2-110">Drugie polecenie pobiera sKU bramy aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="986d2-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="986d2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="986d2-111">PARAMETERS</span></span>

### <span data-ttu-id="986d2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="986d2-112">-ApplicationGateway</span></span>
<span data-ttu-id="986d2-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="986d2-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="986d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986d2-114">-DefaultProfile</span></span>
<span data-ttu-id="986d2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="986d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="986d2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986d2-116">CommonParameters</span></span>
<span data-ttu-id="986d2-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986d2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986d2-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="986d2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986d2-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="986d2-119">INPUTS</span></span>

### <span data-ttu-id="986d2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="986d2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="986d2-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="986d2-121">OUTPUTS</span></span>

### <span data-ttu-id="986d2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="986d2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="986d2-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="986d2-123">NOTES</span></span>

## <span data-ttu-id="986d2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="986d2-124">RELATED LINKS</span></span>

[<span data-ttu-id="986d2-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="986d2-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="986d2-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="986d2-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


