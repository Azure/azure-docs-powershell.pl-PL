---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f415da1d6f9bb086d796c0c1bf191282c2880a09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710706"
---
# <span data-ttu-id="a6f54-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a6f54-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="a6f54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6f54-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f54-103">Przenoszenie subskrypcji między delegowanymi ofertami dostawców.</span><span class="sxs-lookup"><span data-stu-id="a6f54-103">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="a6f54-104">Proces ten przeprowadza tylko ponowne znakowanie, ale nie spowoduje zmiany podstawowych ofert, planów, przydziałów dla abonamentów.</span><span class="sxs-lookup"><span data-stu-id="a6f54-104">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="a6f54-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6f54-105">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="a6f54-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a6f54-106">DESCRIPTION</span></span>
<span data-ttu-id="a6f54-107">Przenoszenie subskrypcji między delegowanymi ofertami dostawców.</span><span class="sxs-lookup"><span data-stu-id="a6f54-107">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="a6f54-108">Proces ten przeprowadza tylko ponowne znakowanie, ale nie spowoduje zmiany podstawowych ofert, planów, przydziałów dla abonamentów.</span><span class="sxs-lookup"><span data-stu-id="a6f54-108">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="a6f54-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6f54-109">EXAMPLES</span></span>

### <span data-ttu-id="a6f54-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6f54-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="a6f54-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-ResourceID "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="a6f54-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="a6f54-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6f54-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="a6f54-113">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ" O1 "" | gdzie {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | SELECT-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="a6f54-113">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="a6f54-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6f54-114">PARAMETERS</span></span>

### <span data-ttu-id="a6f54-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6f54-115">-AsJob</span></span>
<span data-ttu-id="a6f54-116">Określa, czy operacja przenoszenia ma być wykonywana jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="a6f54-116">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="a6f54-117">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="a6f54-117">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="a6f54-118">Określa w pełni kwalifikowane delegowane dostawcy, do których to polecenie cmdlet przeniesie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="a6f54-118">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="a6f54-119">NULL, jeśli abonamenty mają być przenoszone z powrotem do domyślnego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="a6f54-119">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="a6f54-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6f54-120">-ResourceId</span></span>
<span data-ttu-id="a6f54-121">Określa tablicę identyfikatorów zasobów abonamentu, które są przenoszone w pełni kwalifikowanego polecenia.</span><span class="sxs-lookup"><span data-stu-id="a6f54-121">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="a6f54-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f54-122">CommonParameters</span></span>
<span data-ttu-id="a6f54-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f54-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f54-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f54-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f54-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6f54-125">INPUTS</span></span>

## <span data-ttu-id="a6f54-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6f54-126">OUTPUTS</span></span>

## <span data-ttu-id="a6f54-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6f54-127">NOTES</span></span>

## <span data-ttu-id="a6f54-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6f54-128">RELATED LINKS</span></span>

