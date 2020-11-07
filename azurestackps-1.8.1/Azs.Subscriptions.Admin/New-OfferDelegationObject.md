---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889521"
---
# <span data-ttu-id="bf644-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="bf644-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="bf644-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf644-102">SYNOPSIS</span></span>
<span data-ttu-id="bf644-103">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="bf644-103">Offer delegation.</span></span>

## <span data-ttu-id="bf644-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf644-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf644-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf644-105">DESCRIPTION</span></span>
<span data-ttu-id="bf644-106">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="bf644-106">Offer delegation.</span></span>

## <span data-ttu-id="bf644-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf644-107">EXAMPLES</span></span>

### <span data-ttu-id="bf644-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf644-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bf644-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="bf644-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bf644-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf644-110">PARAMETERS</span></span>

### <span data-ttu-id="bf644-111">-ID</span><span class="sxs-lookup"><span data-stu-id="bf644-111">-Id</span></span>
<span data-ttu-id="bf644-112">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf644-112">URI of the resource.</span></span>

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

### <span data-ttu-id="bf644-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bf644-113">-Location</span></span>
<span data-ttu-id="bf644-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf644-114">Location of the resource.</span></span>

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

### <span data-ttu-id="bf644-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf644-115">-Name</span></span>
<span data-ttu-id="bf644-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf644-116">Name of the resource.</span></span>

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

### <span data-ttu-id="bf644-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bf644-117">-SubscriptionId</span></span>
<span data-ttu-id="bf644-118">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="bf644-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="bf644-119">-Tagi</span><span class="sxs-lookup"><span data-stu-id="bf644-119">-Tags</span></span>
<span data-ttu-id="bf644-120">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="bf644-120">List of key-value pairs.</span></span>

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

### <span data-ttu-id="bf644-121">-Type</span><span class="sxs-lookup"><span data-stu-id="bf644-121">-Type</span></span>
<span data-ttu-id="bf644-122">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf644-122">Type of resource.</span></span>

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

### <span data-ttu-id="bf644-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf644-123">CommonParameters</span></span>
<span data-ttu-id="bf644-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf644-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf644-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf644-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf644-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf644-126">INPUTS</span></span>

## <span data-ttu-id="bf644-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf644-127">OUTPUTS</span></span>

## <span data-ttu-id="bf644-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf644-128">NOTES</span></span>

## <span data-ttu-id="bf644-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf644-129">RELATED LINKS</span></span>

