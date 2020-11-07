---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889806"
---
# <span data-ttu-id="16d68-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="16d68-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="16d68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16d68-102">SYNOPSIS</span></span>
<span data-ttu-id="16d68-103">Pobierz listę ofert dla określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="16d68-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="16d68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16d68-104">SYNTAX</span></span>

### <span data-ttu-id="16d68-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="16d68-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="16d68-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="16d68-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="16d68-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16d68-107">DESCRIPTION</span></span>
<span data-ttu-id="16d68-108">Pobierz listę ofert dla określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="16d68-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="16d68-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16d68-109">EXAMPLES</span></span>

### <span data-ttu-id="16d68-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="16d68-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="16d68-111">Pobierz listę ofert dla określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="16d68-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="16d68-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16d68-112">PARAMETERS</span></span>

### <span data-ttu-id="16d68-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="16d68-113">-OfferName</span></span>
<span data-ttu-id="16d68-114">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="16d68-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d68-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="16d68-115">-DelegatedProviderId</span></span>
<span data-ttu-id="16d68-116">Identyfikator delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="16d68-116">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d68-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="16d68-117">-Skip</span></span>
<span data-ttu-id="16d68-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="16d68-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d68-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="16d68-119">-Top</span></span>
<span data-ttu-id="16d68-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="16d68-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="16d68-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="16d68-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d68-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d68-122">CommonParameters</span></span>
<span data-ttu-id="16d68-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d68-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d68-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d68-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d68-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16d68-125">INPUTS</span></span>

## <span data-ttu-id="16d68-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16d68-126">OUTPUTS</span></span>

### <span data-ttu-id="16d68-127">Microsoft. AzureStack. Management. Subscription. MODELES. Offer</span><span class="sxs-lookup"><span data-stu-id="16d68-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="16d68-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16d68-128">NOTES</span></span>

## <span data-ttu-id="16d68-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16d68-129">RELATED LINKS</span></span>
