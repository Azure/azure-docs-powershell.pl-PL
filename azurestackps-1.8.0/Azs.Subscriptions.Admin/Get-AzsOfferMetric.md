---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889254"
---
# <span data-ttu-id="c493e-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="c493e-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="c493e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c493e-102">SYNOPSIS</span></span>
<span data-ttu-id="c493e-103">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="c493e-103">Get the offer metrics.</span></span>

## <span data-ttu-id="c493e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c493e-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="c493e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c493e-105">DESCRIPTION</span></span>
<span data-ttu-id="c493e-106">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="c493e-106">Get the offer metrics.</span></span>

## <span data-ttu-id="c493e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c493e-107">EXAMPLES</span></span>

### <span data-ttu-id="c493e-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c493e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="c493e-109">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="c493e-109">Get the offer metrics.</span></span>

## <span data-ttu-id="c493e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c493e-110">PARAMETERS</span></span>

### <span data-ttu-id="c493e-111">-Offername</span><span class="sxs-lookup"><span data-stu-id="c493e-111">-OfferName</span></span>
<span data-ttu-id="c493e-112">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="c493e-112">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c493e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c493e-113">-ResourceGroupName</span></span>
<span data-ttu-id="c493e-114">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="c493e-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c493e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c493e-115">CommonParameters</span></span>
<span data-ttu-id="c493e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c493e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c493e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c493e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c493e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c493e-118">INPUTS</span></span>

## <span data-ttu-id="c493e-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c493e-119">OUTPUTS</span></span>

### <span data-ttu-id="c493e-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="c493e-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="c493e-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c493e-121">NOTES</span></span>

## <span data-ttu-id="c493e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c493e-122">RELATED LINKS</span></span>

