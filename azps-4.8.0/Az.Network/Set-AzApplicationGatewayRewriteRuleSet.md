---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063314"
---
# <span data-ttu-id="771f1-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="771f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="771f1-102">SYNOPSIS</span></span>
<span data-ttu-id="771f1-103">Modyfikuje zestaw reguł ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="771f1-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="771f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="771f1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="771f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="771f1-105">DESCRIPTION</span></span>
<span data-ttu-id="771f1-106">Polecenie cmdlet **Set-AzApplicationGatewayRewriteRuleSet** modyfikuje regułę rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="771f1-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="771f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="771f1-107">EXAMPLES</span></span>

### <span data-ttu-id="771f1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="771f1-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="771f1-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="771f1-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="771f1-110">Drugie polecenie modyfikuje zestaw reguł ponownej edycji dla bramy aplikacji, aby używać reguł dotyczących ponownej pisania określonych w zmiennej $rule.</span><span class="sxs-lookup"><span data-stu-id="771f1-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="771f1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="771f1-111">PARAMETERS</span></span>

### <span data-ttu-id="771f1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="771f1-112">-ApplicationGateway</span></span>
<span data-ttu-id="771f1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="771f1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="771f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771f1-114">-DefaultProfile</span></span>
<span data-ttu-id="771f1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="771f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="771f1-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="771f1-116">-Name</span></span>
<span data-ttu-id="771f1-117">Nazwa RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="771f1-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="771f1-118">-RewriteRule</span></span>
<span data-ttu-id="771f1-119">Lista reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="771f1-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771f1-120">CommonParameters</span></span>
<span data-ttu-id="771f1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="771f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771f1-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771f1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771f1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="771f1-123">INPUTS</span></span>

### <span data-ttu-id="771f1-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="771f1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="771f1-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="771f1-125">OUTPUTS</span></span>

### <span data-ttu-id="771f1-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="771f1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="771f1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="771f1-127">NOTES</span></span>

## <span data-ttu-id="771f1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="771f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="771f1-129">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="771f1-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="771f1-131">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="771f1-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="771f1-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="771f1-133">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="771f1-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="771f1-134">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="771f1-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="771f1-135">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="771f1-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
