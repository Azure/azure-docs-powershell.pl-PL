---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889486"
---
# <span data-ttu-id="2d76a-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="2d76a-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="2d76a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d76a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d76a-103">Sprawdzanie, czy subskrypcje użytkowników mogą być przenoszone między ofertami delegowanych dostawców.</span><span class="sxs-lookup"><span data-stu-id="2d76a-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="2d76a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d76a-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="2d76a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d76a-105">DESCRIPTION</span></span>
<span data-ttu-id="2d76a-106">Sprawdzanie, czy subskrypcje użytkowników mogą być przenoszone między ofertami delegowanych dostawców.</span><span class="sxs-lookup"><span data-stu-id="2d76a-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="2d76a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d76a-107">EXAMPLES</span></span>

### <span data-ttu-id="2d76a-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d76a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="2d76a-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-ResourceID "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="2d76a-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="2d76a-110">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d76a-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="2d76a-111">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ" O1 "" | SELECT-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="2d76a-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="2d76a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d76a-112">PARAMETERS</span></span>

### <span data-ttu-id="2d76a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d76a-113">-AsJob</span></span>
<span data-ttu-id="2d76a-114">Określa, czy operacja przenoszenia ma być wykonywana jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="2d76a-114">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76a-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="2d76a-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="2d76a-116">Określa w pełni kwalifikowane delegowane dostawcy, do których to polecenie cmdlet przeniesie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="2d76a-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="2d76a-117">NULL, jeśli abonamenty mają być przenoszone z powrotem do domyślnego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2d76a-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d76a-118">-ResourceId</span></span>
<span data-ttu-id="2d76a-119">Określa tablicę identyfikatorów zasobów abonamentu, które są przenoszone w pełni kwalifikowanego polecenia.</span><span class="sxs-lookup"><span data-stu-id="2d76a-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d76a-120">CommonParameters</span></span>
<span data-ttu-id="2d76a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d76a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d76a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d76a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d76a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d76a-123">INPUTS</span></span>

## <span data-ttu-id="2d76a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d76a-124">OUTPUTS</span></span>

## <span data-ttu-id="2d76a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d76a-125">NOTES</span></span>

## <span data-ttu-id="2d76a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d76a-126">RELATED LINKS</span></span>

