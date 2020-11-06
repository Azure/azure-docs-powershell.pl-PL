---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541620"
---
# <span data-ttu-id="bcb1b-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="bcb1b-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="bcb1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb1b-103">Pobiera konta, które nie są skojarzone z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="bcb1b-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcb1b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bcb1b-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb1b-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsLinkTargets** zawiera listę istniejących kont, które nie są skojarzone z subskrypcją platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb1b-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="bcb1b-107">Aby połączyć nowy obszar roboczy z istniejącym kontem, użyj identyfikatora klienta zwróconego przez tę operację we właściwości identyfikator klienta w nowym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bcb1b-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="bcb1b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcb1b-108">EXAMPLES</span></span>

### <span data-ttu-id="bcb1b-109">Przykład 1: uzyskiwanie niepołączonych kont</span><span class="sxs-lookup"><span data-stu-id="bcb1b-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="bcb1b-110">To polecenie uzyskuje niepołączone konta, których właścicielem jest identyfikator rozmówcy.</span><span class="sxs-lookup"><span data-stu-id="bcb1b-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="bcb1b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcb1b-111">PARAMETERS</span></span>

### <span data-ttu-id="bcb1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb1b-112">-DefaultProfile</span></span>
<span data-ttu-id="bcb1b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bcb1b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcb1b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb1b-114">CommonParameters</span></span>
<span data-ttu-id="bcb1b-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb1b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb1b-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb1b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb1b-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcb1b-117">INPUTS</span></span>

### <span data-ttu-id="bcb1b-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bcb1b-118">None</span></span>

## <span data-ttu-id="bcb1b-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcb1b-119">OUTPUTS</span></span>

### <span data-ttu-id="bcb1b-120">Microsoft. Azure. Commands. OperationalInsights. models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="bcb1b-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="bcb1b-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcb1b-121">NOTES</span></span>

## <span data-ttu-id="bcb1b-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcb1b-122">RELATED LINKS</span></span>

[<span data-ttu-id="bcb1b-123">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="bcb1b-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


