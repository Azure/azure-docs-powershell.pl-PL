---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179547"
---
# <span data-ttu-id="b6439-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b6439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6439-102">SYNOPSIS</span></span>
<span data-ttu-id="b6439-103">Usuwa regułę routingu żądania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6439-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="b6439-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6439-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6439-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6439-105">DESCRIPTION</span></span>
<span data-ttu-id="b6439-106">Polecenie **cmdlet Remove-AzApplicationGatewayRequestRoutingRule** usuwa regułę routingu żądania z bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="b6439-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="b6439-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6439-107">EXAMPLES</span></span>

### <span data-ttu-id="b6439-108">Przykład 1. Usuwanie reguły routingu żądania z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6439-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="b6439-109">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6439-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6439-110">Drugie polecenie usuwa regułę routingu żądania o nazwie Rule02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b6439-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b6439-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6439-111">PARAMETERS</span></span>

### <span data-ttu-id="b6439-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6439-112">-ApplicationGateway</span></span>
<span data-ttu-id="b6439-113">Określa bramę aplikacji, z której ma być usuwana reguła routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="b6439-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="b6439-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6439-114">-DefaultProfile</span></span>
<span data-ttu-id="b6439-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6439-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6439-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6439-116">-Name</span></span>
<span data-ttu-id="b6439-117">Określa nazwę reguły routingu żądania, dla której usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6439-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6439-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6439-118">CommonParameters</span></span>
<span data-ttu-id="b6439-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6439-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6439-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6439-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6439-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6439-121">INPUTS</span></span>

### <span data-ttu-id="b6439-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6439-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6439-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6439-123">OUTPUTS</span></span>

### <span data-ttu-id="b6439-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b6439-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6439-125">NOTES</span></span>

## <span data-ttu-id="b6439-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6439-126">RELATED LINKS</span></span>

[<span data-ttu-id="b6439-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6439-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6439-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6439-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6439-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


