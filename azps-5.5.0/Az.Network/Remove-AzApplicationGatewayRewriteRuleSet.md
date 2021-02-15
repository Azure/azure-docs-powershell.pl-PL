---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202615"
---
# <span data-ttu-id="b9df4-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b9df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9df4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9df4-103">Usuwa zestaw reguł ponownego edytguj z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9df4-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="b9df4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9df4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9df4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9df4-105">DESCRIPTION</span></span>
<span data-ttu-id="b9df4-106">Polecenie **cmdlet Remove-AzApplicationGatewayRewriteRuleSet** usuwa zestaw reguł ponownego wstawienia z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9df4-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="b9df4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9df4-107">EXAMPLES</span></span>

### <span data-ttu-id="b9df4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9df4-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="b9df4-109">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9df4-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9df4-110">Drugie polecenie usuwa zestaw reguł ponownego edytowania o nazwie RuleSet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9df4-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b9df4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9df4-111">PARAMETERS</span></span>

### <span data-ttu-id="b9df4-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9df4-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9df4-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9df4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b9df4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9df4-114">-DefaultProfile</span></span>
<span data-ttu-id="b9df4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9df4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9df4-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b9df4-116">-Name</span></span>
<span data-ttu-id="b9df4-117">Nazwa bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b9df4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9df4-118">CommonParameters</span></span>
<span data-ttu-id="b9df4-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9df4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9df4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9df4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9df4-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9df4-121">INPUTS</span></span>

### <span data-ttu-id="b9df4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9df4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9df4-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9df4-123">OUTPUTS</span></span>

### <span data-ttu-id="b9df4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9df4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9df4-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9df4-125">NOTES</span></span>

## <span data-ttu-id="b9df4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9df4-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9df4-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b9df4-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b9df4-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b9df4-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b9df4-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b9df4-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b9df4-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b9df4-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b9df4-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9df4-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
