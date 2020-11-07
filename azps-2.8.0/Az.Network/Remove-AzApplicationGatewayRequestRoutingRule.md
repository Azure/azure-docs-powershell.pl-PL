---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd99eac2ecd36039685dde53730f250754318bc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871284"
---
# <span data-ttu-id="fc76a-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="fc76a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc76a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc76a-103">Usuwa regułę rozsyłania żądań z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc76a-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="fc76a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc76a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc76a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc76a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc76a-106">Polecenie cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** usuwa regułę rozsyłania żądań z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fc76a-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="fc76a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc76a-107">EXAMPLES</span></span>

### <span data-ttu-id="fc76a-108">Przykład 1: Usuwanie reguły rozsyłania żądań z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="fc76a-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="fc76a-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fc76a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fc76a-110">Drugie polecenie usuwa regułę rozsyłania żądań o nazwie Rule02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fc76a-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fc76a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc76a-111">PARAMETERS</span></span>

### <span data-ttu-id="fc76a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc76a-112">-ApplicationGateway</span></span>
<span data-ttu-id="fc76a-113">Określa bramę aplikacji, z której ma zostać usunięta reguła routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="fc76a-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="fc76a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc76a-114">-DefaultProfile</span></span>
<span data-ttu-id="fc76a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc76a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc76a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc76a-116">-Name</span></span>
<span data-ttu-id="fc76a-117">Określa nazwę reguły rozsyłania żądań, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc76a-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc76a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc76a-118">CommonParameters</span></span>
<span data-ttu-id="fc76a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc76a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc76a-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc76a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc76a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc76a-121">INPUTS</span></span>

### <span data-ttu-id="fc76a-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc76a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc76a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc76a-123">OUTPUTS</span></span>

### <span data-ttu-id="fc76a-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="fc76a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc76a-125">NOTES</span></span>

## <span data-ttu-id="fc76a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc76a-126">RELATED LINKS</span></span>

[<span data-ttu-id="fc76a-127">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fc76a-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fc76a-129">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fc76a-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc76a-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


