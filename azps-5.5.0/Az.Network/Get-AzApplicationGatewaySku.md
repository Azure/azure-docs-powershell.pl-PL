---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189826"
---
# <span data-ttu-id="d8609-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d8609-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="d8609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8609-102">SYNOPSIS</span></span>
<span data-ttu-id="d8609-103">Pobiera sku bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d8609-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="d8609-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8609-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8609-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8609-105">DESCRIPTION</span></span>
<span data-ttu-id="d8609-106">Polecenie **cmdlet Get-AzApplicationGatewaySku** pobiera jednostkę przechowywania akcji (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d8609-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="d8609-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8609-107">EXAMPLES</span></span>

### <span data-ttu-id="d8609-108">Przykład 1. Uzyskiwanie sKU bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d8609-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="d8609-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d8609-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d8609-110">Drugie polecenie pobiera sku bramy aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="d8609-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="d8609-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8609-111">PARAMETERS</span></span>

### <span data-ttu-id="d8609-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8609-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8609-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d8609-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="d8609-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8609-114">-DefaultProfile</span></span>
<span data-ttu-id="d8609-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8609-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8609-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8609-116">CommonParameters</span></span>
<span data-ttu-id="d8609-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8609-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8609-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8609-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8609-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8609-119">INPUTS</span></span>

### <span data-ttu-id="d8609-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8609-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8609-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8609-121">OUTPUTS</span></span>

### <span data-ttu-id="d8609-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d8609-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="d8609-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8609-123">NOTES</span></span>

## <span data-ttu-id="d8609-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8609-124">RELATED LINKS</span></span>

[<span data-ttu-id="d8609-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d8609-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="d8609-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d8609-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


