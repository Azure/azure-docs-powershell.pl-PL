---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049307"
---
# <span data-ttu-id="e3b28-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e3b28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3b28-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b28-103">Usuwa zestaw reguł ponownej edycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e3b28-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="e3b28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3b28-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3b28-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b28-106">Polecenie cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** umożliwia usunięcie zestawu reguł ponownego zapisu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b28-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="e3b28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3b28-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3b28-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="e3b28-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e3b28-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e3b28-110">Drugie polecenie usuwa zestaw reguł "ponowne wpisywanie o nazwie RuleSet02" od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e3b28-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e3b28-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3b28-111">PARAMETERS</span></span>

### <span data-ttu-id="e3b28-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3b28-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3b28-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3b28-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e3b28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b28-114">-DefaultProfile</span></span>
<span data-ttu-id="e3b28-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b28-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3b28-116">-Name</span></span>
<span data-ttu-id="e3b28-117">Nazwa bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e3b28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b28-118">CommonParameters</span></span>
<span data-ttu-id="e3b28-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b28-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b28-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b28-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3b28-121">INPUTS</span></span>

### <span data-ttu-id="e3b28-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3b28-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3b28-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3b28-123">OUTPUTS</span></span>

### <span data-ttu-id="e3b28-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3b28-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3b28-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3b28-125">NOTES</span></span>

## <span data-ttu-id="e3b28-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3b28-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3b28-127">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b28-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b28-129">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b28-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b28-131">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e3b28-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e3b28-132">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e3b28-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e3b28-133">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3b28-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
