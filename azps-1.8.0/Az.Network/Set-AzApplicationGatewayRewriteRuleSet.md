---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709006"
---
# <span data-ttu-id="3f3ef-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="3f3ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3ef-103">Modyfikuje zestaw reguł ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="3f3ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f3ef-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f3ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="3f3ef-106">Polecenie cmdlet **Set-AzApplicationGatewayRewriteRuleSet** modyfikuje regułę rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="3f3ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="3f3ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f3ef-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="3f3ef-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3f3ef-110">Drugie polecenie modyfikuje zestaw reguł ponownej edycji dla bramy aplikacji, aby używać reguł dotyczących ponownej pisania określonych w zmiennej $rule.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="3f3ef-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f3ef-111">PARAMETERS</span></span>

### <span data-ttu-id="3f3ef-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3ef-112">-ApplicationGateway</span></span>
<span data-ttu-id="3f3ef-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3ef-113">The applicationGateway</span></span>

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

### <span data-ttu-id="3f3ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3ef-114">-DefaultProfile</span></span>
<span data-ttu-id="3f3ef-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f3ef-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f3ef-116">-Name</span></span>
<span data-ttu-id="3f3ef-117">Nazwa RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="3f3ef-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="3f3ef-118">-RewriteRule</span></span>
<span data-ttu-id="3f3ef-119">Lista reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="3f3ef-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="3f3ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3ef-120">CommonParameters</span></span>
<span data-ttu-id="3f3ef-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3ef-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3ef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3ef-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f3ef-123">INPUTS</span></span>

### <span data-ttu-id="3f3ef-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3ef-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f3ef-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f3ef-125">OUTPUTS</span></span>

### <span data-ttu-id="3f3ef-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3ef-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f3ef-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f3ef-127">NOTES</span></span>

## <span data-ttu-id="3f3ef-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f3ef-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f3ef-129">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f3ef-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f3ef-131">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f3ef-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3f3ef-133">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3f3ef-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3f3ef-134">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3f3ef-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3f3ef-135">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f3ef-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)