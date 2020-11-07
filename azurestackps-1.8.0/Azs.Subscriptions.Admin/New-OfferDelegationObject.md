---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889214"
---
# <span data-ttu-id="36cbf-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="36cbf-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="36cbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="36cbf-103">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="36cbf-103">Offer delegation.</span></span>

## <span data-ttu-id="36cbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36cbf-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="36cbf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="36cbf-106">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="36cbf-106">Offer delegation.</span></span>

## <span data-ttu-id="36cbf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36cbf-107">EXAMPLES</span></span>

### <span data-ttu-id="36cbf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36cbf-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="36cbf-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="36cbf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="36cbf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36cbf-110">PARAMETERS</span></span>

### <span data-ttu-id="36cbf-111">-ID</span><span class="sxs-lookup"><span data-stu-id="36cbf-111">-Id</span></span>
<span data-ttu-id="36cbf-112">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="36cbf-112">URI of the resource.</span></span>

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

### <span data-ttu-id="36cbf-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36cbf-113">-Location</span></span>
<span data-ttu-id="36cbf-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="36cbf-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cbf-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36cbf-115">-Name</span></span>
<span data-ttu-id="36cbf-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="36cbf-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cbf-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="36cbf-117">-SubscriptionId</span></span>
<span data-ttu-id="36cbf-118">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="36cbf-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cbf-119">-Tagi</span><span class="sxs-lookup"><span data-stu-id="36cbf-119">-Tags</span></span>
<span data-ttu-id="36cbf-120">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="36cbf-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cbf-121">-Type</span><span class="sxs-lookup"><span data-stu-id="36cbf-121">-Type</span></span>
<span data-ttu-id="36cbf-122">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="36cbf-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36cbf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cbf-123">CommonParameters</span></span>
<span data-ttu-id="36cbf-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cbf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cbf-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cbf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cbf-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36cbf-126">INPUTS</span></span>

## <span data-ttu-id="36cbf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36cbf-127">OUTPUTS</span></span>

## <span data-ttu-id="36cbf-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36cbf-128">NOTES</span></span>

## <span data-ttu-id="36cbf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36cbf-129">RELATED LINKS</span></span>

