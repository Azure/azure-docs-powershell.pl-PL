---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710662"
---
# <span data-ttu-id="83284-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="83284-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="83284-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83284-102">SYNOPSIS</span></span>
<span data-ttu-id="83284-103">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="83284-103">Get the offer metrics.</span></span>

## <span data-ttu-id="83284-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83284-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="83284-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83284-105">DESCRIPTION</span></span>
<span data-ttu-id="83284-106">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="83284-106">Get the offer metrics.</span></span>

## <span data-ttu-id="83284-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83284-107">EXAMPLES</span></span>

### <span data-ttu-id="83284-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83284-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="83284-109">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="83284-109">Get the offer metrics.</span></span>

## <span data-ttu-id="83284-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83284-110">PARAMETERS</span></span>

### <span data-ttu-id="83284-111">-Offername</span><span class="sxs-lookup"><span data-stu-id="83284-111">-OfferName</span></span>
<span data-ttu-id="83284-112">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="83284-112">Name of an offer.</span></span>

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

### <span data-ttu-id="83284-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83284-113">-ResourceGroupName</span></span>
<span data-ttu-id="83284-114">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="83284-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="83284-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83284-115">CommonParameters</span></span>
<span data-ttu-id="83284-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83284-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83284-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83284-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83284-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83284-118">INPUTS</span></span>

## <span data-ttu-id="83284-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83284-119">OUTPUTS</span></span>

### <span data-ttu-id="83284-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="83284-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="83284-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83284-121">NOTES</span></span>

## <span data-ttu-id="83284-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83284-122">RELATED LINKS</span></span>

