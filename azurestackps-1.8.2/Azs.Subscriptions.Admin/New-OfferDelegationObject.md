---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055719"
---
# <span data-ttu-id="1bf33-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="1bf33-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="1bf33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bf33-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf33-103">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="1bf33-103">Offer delegation.</span></span>

## <span data-ttu-id="1bf33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bf33-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1bf33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1bf33-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf33-106">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="1bf33-106">Offer delegation.</span></span>

## <span data-ttu-id="1bf33-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bf33-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf33-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1bf33-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1bf33-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1bf33-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1bf33-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bf33-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf33-111">-ID</span><span class="sxs-lookup"><span data-stu-id="1bf33-111">-Id</span></span>
<span data-ttu-id="1bf33-112">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="1bf33-112">URI of the resource.</span></span>

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

### <span data-ttu-id="1bf33-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1bf33-113">-Location</span></span>
<span data-ttu-id="1bf33-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1bf33-114">Location of the resource.</span></span>

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

### <span data-ttu-id="1bf33-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bf33-115">-Name</span></span>
<span data-ttu-id="1bf33-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1bf33-116">Name of the resource.</span></span>

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

### <span data-ttu-id="1bf33-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1bf33-117">-SubscriptionId</span></span>
<span data-ttu-id="1bf33-118">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="1bf33-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="1bf33-119">-Tagi</span><span class="sxs-lookup"><span data-stu-id="1bf33-119">-Tags</span></span>
<span data-ttu-id="1bf33-120">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="1bf33-120">List of key-value pairs.</span></span>

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

### <span data-ttu-id="1bf33-121">-Type</span><span class="sxs-lookup"><span data-stu-id="1bf33-121">-Type</span></span>
<span data-ttu-id="1bf33-122">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="1bf33-122">Type of resource.</span></span>

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

### <span data-ttu-id="1bf33-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf33-123">CommonParameters</span></span>
<span data-ttu-id="1bf33-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf33-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf33-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf33-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf33-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bf33-126">INPUTS</span></span>

## <span data-ttu-id="1bf33-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bf33-127">OUTPUTS</span></span>

## <span data-ttu-id="1bf33-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bf33-128">NOTES</span></span>

## <span data-ttu-id="1bf33-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bf33-129">RELATED LINKS</span></span>

