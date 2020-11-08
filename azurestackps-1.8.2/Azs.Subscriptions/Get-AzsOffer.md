---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055727"
---
# <span data-ttu-id="dc42e-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="dc42e-101">Get-AzsOffer</span></span>

## <span data-ttu-id="dc42e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc42e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc42e-103">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="dc42e-103">Get the list of public offers.</span></span>

## <span data-ttu-id="dc42e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc42e-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="dc42e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc42e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc42e-106">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="dc42e-106">Get the list of public offers.</span></span>

## <span data-ttu-id="dc42e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc42e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc42e-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="dc42e-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="dc42e-109">Zapoznaj się z listą ofert publicznych.</span><span class="sxs-lookup"><span data-stu-id="dc42e-109">Get the list of public offers.</span></span>

## <span data-ttu-id="dc42e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc42e-110">PARAMETERS</span></span>

### <span data-ttu-id="dc42e-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="dc42e-111">-Skip</span></span>
<span data-ttu-id="dc42e-112">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dc42e-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dc42e-113">-Początek</span><span class="sxs-lookup"><span data-stu-id="dc42e-113">-Top</span></span>
<span data-ttu-id="dc42e-114">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dc42e-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dc42e-115">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="dc42e-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dc42e-116">-Provider</span><span class="sxs-lookup"><span data-stu-id="dc42e-116">-Provider</span></span>
<span data-ttu-id="dc42e-117">Parametr opcjonalny określający nazwę delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="dc42e-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="dc42e-118">Ten parametr nie jest używany i będzie przestarzały w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="dc42e-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc42e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc42e-119">CommonParameters</span></span>
<span data-ttu-id="dc42e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc42e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc42e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc42e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc42e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc42e-122">INPUTS</span></span>

## <span data-ttu-id="dc42e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc42e-123">OUTPUTS</span></span>

### <span data-ttu-id="dc42e-124">Microsoft. AzureStack. Management. Subscription. MODELES. Offer</span><span class="sxs-lookup"><span data-stu-id="dc42e-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="dc42e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc42e-125">NOTES</span></span>

## <span data-ttu-id="dc42e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc42e-126">RELATED LINKS</span></span>
