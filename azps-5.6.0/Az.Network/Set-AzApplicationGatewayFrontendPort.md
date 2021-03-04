---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956762"
---
# <span data-ttu-id="2374c-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2374c-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="2374c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2374c-102">SYNOPSIS</span></span>
<span data-ttu-id="2374c-103">Modyfikuje port frontonie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2374c-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="2374c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2374c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2374c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2374c-105">DESCRIPTION</span></span>
<span data-ttu-id="2374c-106">Polecenie **cmdlet Set-AzApplicationGatewayFrontendPort** modyfikuje port frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2374c-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="2374c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2374c-107">EXAMPLES</span></span>

### <span data-ttu-id="2374c-108">Przykład 1. Ustawianie portu frontoronu bramy aplikacji na wartość 80</span><span class="sxs-lookup"><span data-stu-id="2374c-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="2374c-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="2374c-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2374c-110">Drugie polecenie modyfikuje bramę w programie $AppGw w celu użycia portu 80 dla portu frontoronu o nazwie FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="2374c-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="2374c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2374c-111">PARAMETERS</span></span>

### <span data-ttu-id="2374c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2374c-112">-ApplicationGateway</span></span>
<span data-ttu-id="2374c-113">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet skojarzy port frontoronu.</span><span class="sxs-lookup"><span data-stu-id="2374c-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="2374c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2374c-114">-DefaultProfile</span></span>
<span data-ttu-id="2374c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2374c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2374c-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2374c-116">-Name</span></span>
<span data-ttu-id="2374c-117">Określa nazwę portu frontoronu, który ma być modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="2374c-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="2374c-118">— Port</span><span class="sxs-lookup"><span data-stu-id="2374c-118">-Port</span></span>
<span data-ttu-id="2374c-119">Określa numer portu, który ma być numer portu frontonie.</span><span class="sxs-lookup"><span data-stu-id="2374c-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2374c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2374c-120">CommonParameters</span></span>
<span data-ttu-id="2374c-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2374c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2374c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2374c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2374c-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2374c-123">INPUTS</span></span>

### <span data-ttu-id="2374c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2374c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2374c-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2374c-125">OUTPUTS</span></span>

### <span data-ttu-id="2374c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2374c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2374c-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2374c-127">NOTES</span></span>

## <span data-ttu-id="2374c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2374c-128">RELATED LINKS</span></span>

[<span data-ttu-id="2374c-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2374c-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2374c-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2374c-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2374c-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2374c-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2374c-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2374c-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
