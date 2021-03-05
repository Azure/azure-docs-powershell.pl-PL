---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: b914e87729e97bb6b8af9ec59605290e0cc025bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978362"
---
# <span data-ttu-id="d4b12-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4b12-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="d4b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b12-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b12-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d4b12-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d4b12-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4b12-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4b12-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4b12-105">DESCRIPTION</span></span>
<span data-ttu-id="d4b12-106">Polecenie **cmdlet Get-AzApplicationGatewayAvailableWafRuleSet** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d4b12-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d4b12-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4b12-107">EXAMPLES</span></span>

### <span data-ttu-id="d4b12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4b12-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="d4b12-109">Te polecenia zwracają wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d4b12-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="d4b12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4b12-110">PARAMETERS</span></span>

### <span data-ttu-id="d4b12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b12-111">-DefaultProfile</span></span>
<span data-ttu-id="d4b12-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b12-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b12-113">CommonParameters</span></span>
<span data-ttu-id="d4b12-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b12-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b12-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4b12-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b12-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4b12-116">INPUTS</span></span>

### <span data-ttu-id="d4b12-117">Brak</span><span class="sxs-lookup"><span data-stu-id="d4b12-117">None</span></span>

## <span data-ttu-id="d4b12-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4b12-118">OUTPUTS</span></span>

### <span data-ttu-id="d4b12-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="d4b12-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="d4b12-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4b12-120">NOTES</span></span>
<span data-ttu-id="d4b12-121">**List-AzApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="d4b12-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="d4b12-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4b12-122">RELATED LINKS</span></span>
