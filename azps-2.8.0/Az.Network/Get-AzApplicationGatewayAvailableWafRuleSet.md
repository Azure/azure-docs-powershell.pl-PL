---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870295"
---
# <span data-ttu-id="18a2d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="18a2d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="18a2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="18a2d-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="18a2d-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="18a2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18a2d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a2d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="18a2d-106">Polecenie cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="18a2d-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="18a2d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="18a2d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18a2d-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="18a2d-109">To polecenie zwraca wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="18a2d-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="18a2d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18a2d-110">PARAMETERS</span></span>

### <span data-ttu-id="18a2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a2d-111">-DefaultProfile</span></span>
<span data-ttu-id="18a2d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18a2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18a2d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a2d-113">CommonParameters</span></span>
<span data-ttu-id="18a2d-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a2d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a2d-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a2d-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a2d-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a2d-116">INPUTS</span></span>

### <span data-ttu-id="18a2d-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18a2d-117">None</span></span>

## <span data-ttu-id="18a2d-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18a2d-118">OUTPUTS</span></span>

### <span data-ttu-id="18a2d-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="18a2d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="18a2d-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18a2d-120">NOTES</span></span>
<span data-ttu-id="18a2d-121">**Lista — AzApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="18a2d-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="18a2d-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18a2d-122">RELATED LINKS</span></span>
