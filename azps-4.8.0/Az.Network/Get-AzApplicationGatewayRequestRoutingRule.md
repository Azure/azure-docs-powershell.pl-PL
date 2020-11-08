---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221466"
---
# <span data-ttu-id="e8b73-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e8b73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8b73-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b73-103">Pobiera regułę routingu żądań bramy Application.</span><span class="sxs-lookup"><span data-stu-id="e8b73-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="e8b73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8b73-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8b73-105">DESCRIPTION</span></span>
<span data-ttu-id="e8b73-106">Polecenie cmdlet **Get-AzApplicationGatewayRequestRoutingRule** pobiera regułę rozsyłania żądań bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e8b73-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="e8b73-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8b73-107">EXAMPLES</span></span>

### <span data-ttu-id="e8b73-108">Przykład 1: uzyskiwanie określonej reguły routingu żądań</span><span class="sxs-lookup"><span data-stu-id="e8b73-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="e8b73-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8b73-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e8b73-110">Drugie polecenie pobiera regułę rozsyłania żądań o nazwie Rule01 od bramy aplikacji zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8b73-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="e8b73-111">Przykład 2: uzyskiwanie listy reguł rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="e8b73-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="e8b73-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8b73-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e8b73-113">Drugie polecenie pobiera listę reguł rozsyłania żądań od bramy aplikacji zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8b73-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="e8b73-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8b73-114">PARAMETERS</span></span>

### <span data-ttu-id="e8b73-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8b73-115">-ApplicationGateway</span></span>
<span data-ttu-id="e8b73-116">Określa obiekt bramy aplikacji, który zawiera regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="e8b73-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="e8b73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b73-117">-DefaultProfile</span></span>
<span data-ttu-id="e8b73-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8b73-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8b73-119">-Name</span></span>
<span data-ttu-id="e8b73-120">Określa nazwę reguły rozsyłania żądań, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8b73-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="e8b73-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b73-121">CommonParameters</span></span>
<span data-ttu-id="e8b73-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b73-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b73-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8b73-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b73-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8b73-124">INPUTS</span></span>

### <span data-ttu-id="e8b73-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8b73-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8b73-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8b73-126">OUTPUTS</span></span>

### <span data-ttu-id="e8b73-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e8b73-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8b73-128">NOTES</span></span>

## <span data-ttu-id="e8b73-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8b73-129">RELATED LINKS</span></span>

[<span data-ttu-id="e8b73-130">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8b73-131">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8b73-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8b73-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b73-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


