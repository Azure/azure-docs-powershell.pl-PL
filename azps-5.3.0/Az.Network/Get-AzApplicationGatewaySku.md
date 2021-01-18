---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499550"
---
# <span data-ttu-id="211f5-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="211f5-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="211f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="211f5-102">SYNOPSIS</span></span>
<span data-ttu-id="211f5-103">Pobiera jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="211f5-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="211f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="211f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="211f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="211f5-105">DESCRIPTION</span></span>
<span data-ttu-id="211f5-106">Polecenie cmdlet **Get-AzApplicationGatewaySku** pobiera jednostkę SKU (Stocking Unit) bramy Application.</span><span class="sxs-lookup"><span data-stu-id="211f5-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="211f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="211f5-107">EXAMPLES</span></span>

### <span data-ttu-id="211f5-108">Przykład 1: uzyskiwanie jednostki SKU bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="211f5-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="211f5-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="211f5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="211f5-110">Drugie polecenie pobiera jednostkę SKU bramy Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="211f5-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="211f5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="211f5-111">PARAMETERS</span></span>

### <span data-ttu-id="211f5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="211f5-112">-ApplicationGateway</span></span>
<span data-ttu-id="211f5-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="211f5-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="211f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211f5-114">-DefaultProfile</span></span>
<span data-ttu-id="211f5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="211f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211f5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211f5-116">CommonParameters</span></span>
<span data-ttu-id="211f5-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211f5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211f5-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211f5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211f5-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="211f5-119">INPUTS</span></span>

### <span data-ttu-id="211f5-120">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="211f5-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="211f5-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="211f5-121">OUTPUTS</span></span>

### <span data-ttu-id="211f5-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="211f5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="211f5-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="211f5-123">NOTES</span></span>

## <span data-ttu-id="211f5-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="211f5-124">RELATED LINKS</span></span>

[<span data-ttu-id="211f5-125">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="211f5-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="211f5-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="211f5-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


