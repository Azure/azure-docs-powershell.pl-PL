---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012602"
---
# <span data-ttu-id="6fb22-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="6fb22-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="6fb22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb22-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb22-103">Lista confluent marketplace umów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6fb22-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="6fb22-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fb22-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fb22-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fb22-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb22-106">Lista confluent marketplace umów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6fb22-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="6fb22-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fb22-107">EXAMPLES</span></span>

### <span data-ttu-id="6fb22-108">Przykład 1. Lista wszystkich umowy dotyczącej witryny Confluent Marketplace w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6fb22-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="6fb22-109">To polecenie zawiera listę wszystkich umów na sklep confluent w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6fb22-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="6fb22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fb22-110">PARAMETERS</span></span>

### <span data-ttu-id="6fb22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb22-111">-DefaultProfile</span></span>
<span data-ttu-id="6fb22-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb22-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb22-113">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fb22-113">-SubscriptionId</span></span>
<span data-ttu-id="6fb22-114">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="6fb22-114">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb22-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb22-115">CommonParameters</span></span>
<span data-ttu-id="6fb22-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb22-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb22-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fb22-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb22-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fb22-118">INPUTS</span></span>

## <span data-ttu-id="6fb22-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fb22-119">OUTPUTS</span></span>

### <span data-ttu-id="6fb22-120">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="6fb22-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="6fb22-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fb22-121">NOTES</span></span>

<span data-ttu-id="6fb22-122">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6fb22-122">ALIASES</span></span>

## <span data-ttu-id="6fb22-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fb22-123">RELATED LINKS</span></span>

