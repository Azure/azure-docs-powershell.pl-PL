---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061492"
---
# <span data-ttu-id="1182e-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="1182e-101">New-AzsSubscription</span></span>

## <span data-ttu-id="1182e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1182e-102">SYNOPSIS</span></span>
<span data-ttu-id="1182e-103">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1182e-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="1182e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1182e-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1182e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1182e-105">DESCRIPTION</span></span>
<span data-ttu-id="1182e-106">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1182e-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="1182e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1182e-107">EXAMPLES</span></span>

### <span data-ttu-id="1182e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1182e-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="1182e-109">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1182e-109">Create a subscription.</span></span>

## <span data-ttu-id="1182e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1182e-110">PARAMETERS</span></span>

### <span data-ttu-id="1182e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1182e-111">-DefaultProfile</span></span>
<span data-ttu-id="1182e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1182e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1182e-113">-DisplayName</span></span>
<span data-ttu-id="1182e-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1182e-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="1182e-115">-Id</span></span>
<span data-ttu-id="1182e-116">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="1182e-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="1182e-117">-OfferId</span></span>
<span data-ttu-id="1182e-118">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="1182e-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-119">-State</span><span class="sxs-lookup"><span data-stu-id="1182e-119">-State</span></span>
<span data-ttu-id="1182e-120">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1182e-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1182e-121">-SubscriptionId</span></span>
<span data-ttu-id="1182e-122">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1182e-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-123">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="1182e-123">-TenantId</span></span>
<span data-ttu-id="1182e-124">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="1182e-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1182e-125">-Confirm</span></span>
<span data-ttu-id="1182e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1182e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1182e-127">-WhatIf</span></span>
<span data-ttu-id="1182e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1182e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1182e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1182e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1182e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1182e-130">CommonParameters</span></span>
<span data-ttu-id="1182e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1182e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1182e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1182e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1182e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1182e-133">INPUTS</span></span>

## <span data-ttu-id="1182e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1182e-134">OUTPUTS</span></span>

### <span data-ttu-id="1182e-135">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="1182e-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="1182e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1182e-136">NOTES</span></span>

## <span data-ttu-id="1182e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1182e-137">RELATED LINKS</span></span>

