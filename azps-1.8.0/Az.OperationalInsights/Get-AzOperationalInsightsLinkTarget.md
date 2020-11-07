---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710907"
---
# <span data-ttu-id="f0e4e-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="f0e4e-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="f0e4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e4e-103">Pobiera konta, które nie są skojarzone z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="f0e4e-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="f0e4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0e4e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0e4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e4e-106">Polecenie cmdlet **Get-AzOperationalInsightsLinkTarget** zawiera listę istniejących kont, które nie są skojarzone z subskrypcją platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e4e-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="f0e4e-107">Aby połączyć nowy obszar roboczy z istniejącym kontem, użyj identyfikatora klienta zwróconego przez tę operację we właściwości identyfikator klienta w nowym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f0e4e-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="f0e4e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0e4e-108">EXAMPLES</span></span>

### <span data-ttu-id="f0e4e-109">Przykład 1: uzyskiwanie niepołączonych kont</span><span class="sxs-lookup"><span data-stu-id="f0e4e-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="f0e4e-110">To polecenie uzyskuje niepołączone konta, których właścicielem jest identyfikator rozmówcy.</span><span class="sxs-lookup"><span data-stu-id="f0e4e-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="f0e4e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0e4e-111">PARAMETERS</span></span>

### <span data-ttu-id="f0e4e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e4e-112">-DefaultProfile</span></span>
<span data-ttu-id="f0e4e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f0e4e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0e4e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e4e-114">CommonParameters</span></span>
<span data-ttu-id="f0e4e-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e4e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e4e-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e4e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e4e-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0e4e-117">INPUTS</span></span>

### <span data-ttu-id="f0e4e-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f0e4e-118">None</span></span>

## <span data-ttu-id="f0e4e-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0e4e-119">OUTPUTS</span></span>

### <span data-ttu-id="f0e4e-120">Microsoft. Azure. Commands. OperationalInsights. models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="f0e4e-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="f0e4e-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0e4e-121">NOTES</span></span>

## <span data-ttu-id="f0e4e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0e4e-122">RELATED LINKS</span></span>

[<span data-ttu-id="f0e4e-123">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="f0e4e-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

