---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889210"
---
# <span data-ttu-id="83006-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="83006-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="83006-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83006-102">SYNOPSIS</span></span>
<span data-ttu-id="83006-103">Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="83006-103">List of supported operations.</span></span>

## <span data-ttu-id="83006-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83006-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="83006-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83006-105">DESCRIPTION</span></span>
<span data-ttu-id="83006-106">Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="83006-106">List of supported operations.</span></span>

## <span data-ttu-id="83006-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83006-107">EXAMPLES</span></span>

### <span data-ttu-id="83006-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83006-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="83006-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="83006-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="83006-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83006-110">PARAMETERS</span></span>

### <span data-ttu-id="83006-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83006-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="83006-112">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="83006-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="83006-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="83006-113">-DisplayName</span></span>
<span data-ttu-id="83006-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83006-114">Subscription name.</span></span>

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

### <span data-ttu-id="83006-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="83006-115">-ExternalReferenceId</span></span>
<span data-ttu-id="83006-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="83006-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-117">-ID</span><span class="sxs-lookup"><span data-stu-id="83006-117">-Id</span></span>
<span data-ttu-id="83006-118">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="83006-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83006-119">-Name</span></span>
<span data-ttu-id="83006-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="83006-120">Name of the resource.</span></span>

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

### <span data-ttu-id="83006-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="83006-121">-OfferId</span></span>
<span data-ttu-id="83006-122">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="83006-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-123">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="83006-123">-Owner</span></span>
<span data-ttu-id="83006-124">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83006-124">Subscription owner.</span></span>

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

### <span data-ttu-id="83006-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="83006-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="83006-126">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="83006-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-127">-State</span><span class="sxs-lookup"><span data-stu-id="83006-127">-State</span></span>
<span data-ttu-id="83006-128">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="83006-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="83006-129">-SubscriptionId</span></span>
<span data-ttu-id="83006-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83006-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="83006-131">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="83006-131">-TenantId</span></span>
<span data-ttu-id="83006-132">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="83006-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="83006-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83006-133">CommonParameters</span></span>
<span data-ttu-id="83006-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83006-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83006-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83006-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83006-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83006-136">INPUTS</span></span>

## <span data-ttu-id="83006-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83006-137">OUTPUTS</span></span>

## <span data-ttu-id="83006-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83006-138">NOTES</span></span>

## <span data-ttu-id="83006-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83006-139">RELATED LINKS</span></span>

