---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523878"
---
# <span data-ttu-id="4ce92-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="4ce92-101">Get-AzsOffer</span></span>

## <span data-ttu-id="4ce92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ce92-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce92-103">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-103">Get the list of public offers.</span></span>

## <span data-ttu-id="4ce92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ce92-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4ce92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ce92-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce92-106">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-106">Get the list of public offers.</span></span>

## <span data-ttu-id="4ce92-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ce92-107">EXAMPLES</span></span>

### <span data-ttu-id="4ce92-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ce92-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="4ce92-109">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-109">Get the list of public offers.</span></span>

## <span data-ttu-id="4ce92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ce92-110">PARAMETERS</span></span>

### <span data-ttu-id="4ce92-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="4ce92-111">-Skip</span></span>
<span data-ttu-id="4ce92-112">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="4ce92-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce92-113">-Początek</span><span class="sxs-lookup"><span data-stu-id="4ce92-113">-Top</span></span>
<span data-ttu-id="4ce92-114">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="4ce92-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4ce92-115">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="4ce92-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce92-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce92-116">CommonParameters</span></span>
<span data-ttu-id="4ce92-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce92-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce92-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce92-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce92-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce92-119">INPUTS</span></span>

## <span data-ttu-id="4ce92-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ce92-120">OUTPUTS</span></span>

### <span data-ttu-id="4ce92-121">Microsoft. AzureStack. Management. Subscription. MODELES. Offer</span><span class="sxs-lookup"><span data-stu-id="4ce92-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="4ce92-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ce92-122">NOTES</span></span>

## <span data-ttu-id="4ce92-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ce92-123">RELATED LINKS</span></span>
