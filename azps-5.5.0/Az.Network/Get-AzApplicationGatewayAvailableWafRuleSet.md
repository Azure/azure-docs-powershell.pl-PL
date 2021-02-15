---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189874"
---
# <span data-ttu-id="2bc92-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="2bc92-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="2bc92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bc92-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc92-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2bc92-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="2bc92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2bc92-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc92-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2bc92-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc92-106">Polecenie **cmdlet Get-AzApplicationGatewayAvailableWafRuleSet** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2bc92-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="2bc92-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2bc92-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc92-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bc92-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="2bc92-109">Te polecenia zwracają wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2bc92-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="2bc92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bc92-110">PARAMETERS</span></span>

### <span data-ttu-id="2bc92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc92-111">-DefaultProfile</span></span>
<span data-ttu-id="2bc92-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc92-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc92-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc92-113">CommonParameters</span></span>
<span data-ttu-id="2bc92-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc92-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc92-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bc92-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc92-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bc92-116">INPUTS</span></span>

### <span data-ttu-id="2bc92-117">Brak</span><span class="sxs-lookup"><span data-stu-id="2bc92-117">None</span></span>

## <span data-ttu-id="2bc92-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bc92-118">OUTPUTS</span></span>

### <span data-ttu-id="2bc92-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="2bc92-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="2bc92-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2bc92-120">NOTES</span></span>
<span data-ttu-id="2bc92-121">**List-AzApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="2bc92-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="2bc92-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bc92-122">RELATED LINKS</span></span>
