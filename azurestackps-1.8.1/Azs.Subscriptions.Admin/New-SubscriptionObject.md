---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889494"
---
# <span data-ttu-id="e22e1-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="e22e1-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="e22e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e22e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e22e1-103">Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="e22e1-103">List of supported operations.</span></span>

## <span data-ttu-id="e22e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e22e1-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e22e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e22e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e22e1-106">Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="e22e1-106">List of supported operations.</span></span>

## <span data-ttu-id="e22e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e22e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e22e1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e22e1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e22e1-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="e22e1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e22e1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e22e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e22e1-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e22e1-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e22e1-112">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="e22e1-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="e22e1-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e22e1-113">-DisplayName</span></span>
<span data-ttu-id="e22e1-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e22e1-114">Subscription name.</span></span>

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

### <span data-ttu-id="e22e1-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e22e1-115">-ExternalReferenceId</span></span>
<span data-ttu-id="e22e1-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="e22e1-116">External reference identifier.</span></span>

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

### <span data-ttu-id="e22e1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e22e1-117">-Id</span></span>
<span data-ttu-id="e22e1-118">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e22e1-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="e22e1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e22e1-119">-Name</span></span>
<span data-ttu-id="e22e1-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e22e1-120">Name of the resource.</span></span>

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

### <span data-ttu-id="e22e1-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e22e1-121">-OfferId</span></span>
<span data-ttu-id="e22e1-122">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="e22e1-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="e22e1-123">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="e22e1-123">-Owner</span></span>
<span data-ttu-id="e22e1-124">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e22e1-124">Subscription owner.</span></span>

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

### <span data-ttu-id="e22e1-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e22e1-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e22e1-126">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="e22e1-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="e22e1-127">-State</span><span class="sxs-lookup"><span data-stu-id="e22e1-127">-State</span></span>
<span data-ttu-id="e22e1-128">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e22e1-128">Subscription state.</span></span>

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

### <span data-ttu-id="e22e1-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e22e1-129">-SubscriptionId</span></span>
<span data-ttu-id="e22e1-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e22e1-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="e22e1-131">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e22e1-131">-TenantId</span></span>
<span data-ttu-id="e22e1-132">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="e22e1-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="e22e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22e1-133">CommonParameters</span></span>
<span data-ttu-id="e22e1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22e1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22e1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22e1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e22e1-136">INPUTS</span></span>

## <span data-ttu-id="e22e1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e22e1-137">OUTPUTS</span></span>

## <span data-ttu-id="e22e1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e22e1-138">NOTES</span></span>

## <span data-ttu-id="e22e1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e22e1-139">RELATED LINKS</span></span>

