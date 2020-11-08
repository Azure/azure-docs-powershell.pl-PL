---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052548"
---
# <span data-ttu-id="ed671-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed671-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="ed671-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed671-102">SYNOPSIS</span></span>
<span data-ttu-id="ed671-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ed671-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ed671-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed671-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed671-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed671-105">DESCRIPTION</span></span>
<span data-ttu-id="ed671-106">Polecenie cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ed671-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ed671-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed671-107">EXAMPLES</span></span>

### <span data-ttu-id="ed671-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed671-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="ed671-109">To polecenie zwraca wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ed671-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="ed671-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed671-110">PARAMETERS</span></span>

### <span data-ttu-id="ed671-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed671-111">-DefaultProfile</span></span>
<span data-ttu-id="ed671-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed671-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed671-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed671-113">CommonParameters</span></span>
<span data-ttu-id="ed671-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed671-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed671-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed671-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed671-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed671-116">INPUTS</span></span>

### <span data-ttu-id="ed671-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ed671-117">None</span></span>

## <span data-ttu-id="ed671-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed671-118">OUTPUTS</span></span>

### <span data-ttu-id="ed671-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="ed671-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="ed671-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed671-120">NOTES</span></span>
<span data-ttu-id="ed671-121">**Lista — AzApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="ed671-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="ed671-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed671-122">RELATED LINKS</span></span>
