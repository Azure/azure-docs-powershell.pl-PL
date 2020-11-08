---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061490"
---
# <span data-ttu-id="db312-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="db312-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="db312-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db312-102">SYNOPSIS</span></span>
<span data-ttu-id="db312-103">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="db312-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db312-104">SYNTAX</span></span>

### <span data-ttu-id="db312-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db312-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="db312-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="db312-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="db312-107">Opis</span><span class="sxs-lookup"><span data-stu-id="db312-107">DESCRIPTION</span></span>
<span data-ttu-id="db312-108">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="db312-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db312-109">EXAMPLES</span></span>

### <span data-ttu-id="db312-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db312-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="db312-111">Aktualizuje subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="db312-111">Updates a subscription.</span></span>

## <span data-ttu-id="db312-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db312-112">PARAMETERS</span></span>

### <span data-ttu-id="db312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db312-113">-DefaultProfile</span></span>
<span data-ttu-id="db312-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db312-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db312-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db312-115">-DisplayName</span></span>
<span data-ttu-id="db312-116">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-117">-ID</span><span class="sxs-lookup"><span data-stu-id="db312-117">-Id</span></span>
<span data-ttu-id="db312-118">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="db312-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="db312-119">-OfferId</span></span>
<span data-ttu-id="db312-120">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="db312-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-121">-State</span><span class="sxs-lookup"><span data-stu-id="db312-121">-State</span></span>
<span data-ttu-id="db312-122">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="db312-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="db312-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="db312-124">Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="db312-124">List of supported operations.</span></span>
<span data-ttu-id="db312-125">Aby skonstruować, zobacz sekcję notatki dla właściwości SUBSCRIPTIONDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="db312-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="db312-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="db312-126">-SubscriptionId</span></span>
<span data-ttu-id="db312-127">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-128">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="db312-128">-TenantId</span></span>
<span data-ttu-id="db312-129">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="db312-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db312-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db312-130">-Confirm</span></span>
<span data-ttu-id="db312-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db312-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db312-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db312-132">-WhatIf</span></span>
<span data-ttu-id="db312-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db312-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db312-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db312-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db312-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db312-135">CommonParameters</span></span>
<span data-ttu-id="db312-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db312-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db312-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db312-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db312-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db312-138">INPUTS</span></span>

### <span data-ttu-id="db312-139">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="db312-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="db312-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db312-140">OUTPUTS</span></span>

### <span data-ttu-id="db312-141">Microsoft. Azure. PowerShell. cmdlets. Subscription. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="db312-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="db312-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db312-142">NOTES</span></span>

<span data-ttu-id="db312-143">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="db312-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db312-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db312-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="db312-145">SUBSCRIPTIONDEFINITION <ISubscription> : Lista obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="db312-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="db312-146">`[DisplayName <String>]`: Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="db312-147">`[Id <String>]`: W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="db312-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="db312-148">`[OfferId <String>]`: Identyfikator oferty w zakresie dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="db312-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="db312-149">`[State <SubscriptionState?>]`: Stan subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="db312-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db312-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="db312-151">`[TenantId <String>]`: Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="db312-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="db312-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db312-152">RELATED LINKS</span></span>

