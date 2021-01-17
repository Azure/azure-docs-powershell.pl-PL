---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322798"
---
# <span data-ttu-id="7178e-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="7178e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7178e-102">SYNOPSIS</span></span>
<span data-ttu-id="7178e-103">Pobiera zestaw reguł ponownej edycji bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7178e-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="7178e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7178e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7178e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7178e-105">DESCRIPTION</span></span>
<span data-ttu-id="7178e-106">Pobiera zestaw reguł ponownej edycji bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7178e-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="7178e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7178e-107">EXAMPLES</span></span>

### <span data-ttu-id="7178e-108">Przykład 1: uzyskiwanie określonego zestawu reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="7178e-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="7178e-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7178e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7178e-110">Drugie polecenie pobiera zestaw reguł "ponowne wpisywanie o nazwie RuleSet01" od bramy aplikacji zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7178e-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7178e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7178e-111">PARAMETERS</span></span>

### <span data-ttu-id="7178e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7178e-112">-ApplicationGateway</span></span>
<span data-ttu-id="7178e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7178e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7178e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7178e-114">-DefaultProfile</span></span>
<span data-ttu-id="7178e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7178e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7178e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7178e-116">-Name</span></span>
<span data-ttu-id="7178e-117">Nazwa bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="7178e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7178e-118">CommonParameters</span></span>
<span data-ttu-id="7178e-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7178e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7178e-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7178e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7178e-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7178e-121">INPUTS</span></span>

### <span data-ttu-id="7178e-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7178e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7178e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7178e-123">OUTPUTS</span></span>

### <span data-ttu-id="7178e-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="7178e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7178e-125">NOTES</span></span>

## <span data-ttu-id="7178e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7178e-126">RELATED LINKS</span></span>

[<span data-ttu-id="7178e-127">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7178e-128">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7178e-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7178e-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7178e-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7178e-131">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7178e-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7178e-132">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7178e-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="7178e-133">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7178e-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
