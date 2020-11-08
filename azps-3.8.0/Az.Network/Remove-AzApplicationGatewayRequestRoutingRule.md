---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049308"
---
# <span data-ttu-id="3a4f0-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3a4f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4f0-103">Usuwa regułę rozsyłania żądań z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="3a4f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a4f0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a4f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4f0-106">Polecenie cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** usuwa regułę rozsyłania żądań z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="3a4f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="3a4f0-108">Przykład 1: Usuwanie reguły rozsyłania żądań z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3a4f0-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="3a4f0-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3a4f0-110">Drugie polecenie usuwa regułę rozsyłania żądań o nazwie Rule02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3a4f0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a4f0-111">PARAMETERS</span></span>

### <span data-ttu-id="3a4f0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a4f0-112">-ApplicationGateway</span></span>
<span data-ttu-id="3a4f0-113">Określa bramę aplikacji, z której ma zostać usunięta reguła routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="3a4f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4f0-114">-DefaultProfile</span></span>
<span data-ttu-id="3a4f0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a4f0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a4f0-116">-Name</span></span>
<span data-ttu-id="3a4f0-117">Określa nazwę reguły rozsyłania żądań, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a4f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4f0-118">CommonParameters</span></span>
<span data-ttu-id="3a4f0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4f0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4f0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4f0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a4f0-121">INPUTS</span></span>

### <span data-ttu-id="3a4f0-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a4f0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3a4f0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a4f0-123">OUTPUTS</span></span>

### <span data-ttu-id="3a4f0-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3a4f0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a4f0-125">NOTES</span></span>

## <span data-ttu-id="3a4f0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a4f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="3a4f0-127">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3a4f0-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3a4f0-129">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3a4f0-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a4f0-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


