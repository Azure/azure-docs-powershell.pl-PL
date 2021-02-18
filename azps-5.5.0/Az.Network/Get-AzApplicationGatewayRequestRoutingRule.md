---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184755"
---
# <span data-ttu-id="818c7-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="818c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="818c7-102">SYNOPSIS</span></span>
<span data-ttu-id="818c7-103">Pobiera regułę routingu żądania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="818c7-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="818c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="818c7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="818c7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="818c7-105">DESCRIPTION</span></span>
<span data-ttu-id="818c7-106">Polecenie **cmdlet Get-AzApplicationGatewayRequestRoutingRule** pobiera regułę routingu żądania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="818c7-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="818c7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="818c7-107">EXAMPLES</span></span>

### <span data-ttu-id="818c7-108">Przykład 1. Uzyskiwanie reguły routingu dla określonego żądania</span><span class="sxs-lookup"><span data-stu-id="818c7-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="818c7-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="818c7-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="818c7-110">Drugie polecenie pobiera regułę routingu żądania o nazwie Rule01 z bramy aplikacji przechowywaną w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="818c7-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="818c7-111">Przykład 2. Uzyskiwanie listy reguł routingu żądań</span><span class="sxs-lookup"><span data-stu-id="818c7-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="818c7-112">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="818c7-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="818c7-113">Drugie polecenie otrzymuje listę reguł routingu żądań z bramy aplikacji przechowywanych w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="818c7-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="818c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="818c7-114">PARAMETERS</span></span>

### <span data-ttu-id="818c7-115">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="818c7-115">-ApplicationGateway</span></span>
<span data-ttu-id="818c7-116">Określa obiekt bramy aplikacji zawierający regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="818c7-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="818c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818c7-117">-DefaultProfile</span></span>
<span data-ttu-id="818c7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="818c7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="818c7-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="818c7-119">-Name</span></span>
<span data-ttu-id="818c7-120">Określa nazwę reguły routingu żądania, którą otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="818c7-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="818c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818c7-121">CommonParameters</span></span>
<span data-ttu-id="818c7-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="818c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818c7-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="818c7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818c7-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="818c7-124">INPUTS</span></span>

### <span data-ttu-id="818c7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="818c7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="818c7-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="818c7-126">OUTPUTS</span></span>

### <span data-ttu-id="818c7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="818c7-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="818c7-128">NOTES</span></span>

## <span data-ttu-id="818c7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="818c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="818c7-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="818c7-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="818c7-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="818c7-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="818c7-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


