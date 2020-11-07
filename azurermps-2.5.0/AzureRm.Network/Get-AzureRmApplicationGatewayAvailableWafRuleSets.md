---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898405"
---
# <span data-ttu-id="e05c9-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="e05c9-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="e05c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e05c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e05c9-103">Pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e05c9-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e05c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e05c9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e05c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e05c9-105">DESCRIPTION</span></span>
<span data-ttu-id="e05c9-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** pobiera wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e05c9-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="e05c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e05c9-107">EXAMPLES</span></span>

### <span data-ttu-id="e05c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e05c9-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="e05c9-109">To polecenie zwraca wszystkie dostępne zestawy reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e05c9-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="e05c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e05c9-110">PARAMETERS</span></span>

### <span data-ttu-id="e05c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05c9-111">-DefaultProfile</span></span>
<span data-ttu-id="e05c9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e05c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05c9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05c9-113">CommonParameters</span></span>
<span data-ttu-id="e05c9-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05c9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05c9-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05c9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05c9-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e05c9-116">INPUTS</span></span>

### <span data-ttu-id="e05c9-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e05c9-117">None</span></span>

## <span data-ttu-id="e05c9-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e05c9-118">OUTPUTS</span></span>

### <span data-ttu-id="e05c9-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="e05c9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="e05c9-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e05c9-120">NOTES</span></span>
<span data-ttu-id="e05c9-121">**Lista — AzureRmApplicationGatewayAvailableWafRuleSets** to alias polecenia cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="e05c9-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="e05c9-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e05c9-122">RELATED LINKS</span></span>

