---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57e195f1d42b4d1df26344133c10d7c0d40e1f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704791"
---
# <span data-ttu-id="a5d5b-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="a5d5b-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="a5d5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d5b-103">Pobierz listę ofert delegowanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a5d5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5d5b-104">SYNTAX</span></span>

### <span data-ttu-id="a5d5b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a5d5b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d5b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a5d5b-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="a5d5b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a5d5b-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a5d5b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5d5b-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d5b-109">Pobierz listę ofert delegowanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a5d5b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5d5b-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d5b-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5d5b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a5d5b-112">Pobierz listę ofert delegowanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a5d5b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5d5b-113">PARAMETERS</span></span>

### <span data-ttu-id="a5d5b-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="a5d5b-114">-DelegatedProviderId</span></span>
<span data-ttu-id="a5d5b-115">Identyfikator DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d5b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5d5b-116">-Name</span></span>
<span data-ttu-id="a5d5b-117">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-117">Name of an offer.</span></span>

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

### <span data-ttu-id="a5d5b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d5b-118">-ResourceId</span></span>
<span data-ttu-id="a5d5b-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d5b-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="a5d5b-120">-Skip</span></span>
<span data-ttu-id="a5d5b-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d5b-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="a5d5b-122">-Top</span></span>
<span data-ttu-id="a5d5b-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a5d5b-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d5b-125">CommonParameters</span></span>
<span data-ttu-id="a5d5b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d5b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d5b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d5b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5d5b-128">INPUTS</span></span>

## <span data-ttu-id="a5d5b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5d5b-129">OUTPUTS</span></span>

### <span data-ttu-id="a5d5b-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="a5d5b-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="a5d5b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5d5b-131">NOTES</span></span>

## <span data-ttu-id="a5d5b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5d5b-132">RELATED LINKS</span></span>

