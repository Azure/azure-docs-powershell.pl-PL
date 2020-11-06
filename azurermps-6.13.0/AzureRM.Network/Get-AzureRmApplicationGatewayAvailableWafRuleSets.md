---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: d5e65b90c818102f2cb61997f0e5ff08640d6395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527865"
---
# <span data-ttu-id="c77d8-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="c77d8-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="c77d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c77d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c77d8-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c77d8-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c77d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c77d8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c77d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c77d8-105">DESCRIPTION</span></span>
<span data-ttu-id="c77d8-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c77d8-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="c77d8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c77d8-107">EXAMPLES</span></span>

### <span data-ttu-id="c77d8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c77d8-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="c77d8-109">To polecenie zwraca wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c77d8-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="c77d8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c77d8-110">PARAMETERS</span></span>

### <span data-ttu-id="c77d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77d8-111">-DefaultProfile</span></span>
<span data-ttu-id="c77d8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c77d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c77d8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77d8-113">CommonParameters</span></span>
<span data-ttu-id="c77d8-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c77d8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77d8-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c77d8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77d8-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c77d8-116">INPUTS</span></span>

### <span data-ttu-id="c77d8-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c77d8-117">None</span></span>

## <span data-ttu-id="c77d8-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c77d8-118">OUTPUTS</span></span>

### <span data-ttu-id="c77d8-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="c77d8-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="c77d8-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c77d8-120">NOTES</span></span>
<span data-ttu-id="c77d8-121">**Lista — AzureRmApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="c77d8-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="c77d8-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c77d8-122">RELATED LINKS</span></span>
