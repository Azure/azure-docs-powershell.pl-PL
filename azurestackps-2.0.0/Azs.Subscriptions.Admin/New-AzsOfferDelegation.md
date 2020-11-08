---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054063"
---
# <span data-ttu-id="d8c94-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d8c94-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="d8c94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8c94-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c94-103">Utwórz lub Zaktualizuj delegowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="d8c94-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d8c94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8c94-104">SYNTAX</span></span>

### <span data-ttu-id="d8c94-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8c94-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8c94-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="d8c94-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8c94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d8c94-107">DESCRIPTION</span></span>
<span data-ttu-id="d8c94-108">Utwórz lub Zaktualizuj delegowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="d8c94-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d8c94-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8c94-109">EXAMPLES</span></span>

### <span data-ttu-id="d8c94-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8c94-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="d8c94-111">Utwórz nową delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="d8c94-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="d8c94-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8c94-112">PARAMETERS</span></span>

### <span data-ttu-id="d8c94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c94-113">-DefaultProfile</span></span>
<span data-ttu-id="d8c94-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8c94-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8c94-115">-Location</span></span>
<span data-ttu-id="d8c94-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d8c94-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c94-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8c94-117">-Name</span></span>
<span data-ttu-id="d8c94-118">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="d8c94-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="d8c94-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="d8c94-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="d8c94-120">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="d8c94-120">Offer delegation.</span></span>
<span data-ttu-id="d8c94-121">Aby skonstruować, zobacz sekcję notatki dla właściwości OFFERDELEGATIONDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d8c94-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d8c94-122">-Offername</span><span class="sxs-lookup"><span data-stu-id="d8c94-122">-OfferName</span></span>
<span data-ttu-id="d8c94-123">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="d8c94-123">Name of an offer.</span></span>

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

### <span data-ttu-id="d8c94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c94-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8c94-125">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="d8c94-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d8c94-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d8c94-126">-SubscriptionId</span></span>
<span data-ttu-id="d8c94-127">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d8c94-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c94-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8c94-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="d8c94-129">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="d8c94-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c94-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8c94-130">-Confirm</span></span>
<span data-ttu-id="d8c94-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c94-132">-WhatIf</span></span>
<span data-ttu-id="d8c94-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c94-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8c94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c94-135">CommonParameters</span></span>
<span data-ttu-id="d8c94-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c94-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8c94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c94-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8c94-138">INPUTS</span></span>

### <span data-ttu-id="d8c94-139">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d8c94-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="d8c94-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8c94-140">OUTPUTS</span></span>

### <span data-ttu-id="d8c94-141">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d8c94-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="d8c94-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d8c94-142">ALIASES</span></span>

## <span data-ttu-id="d8c94-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8c94-143">NOTES</span></span>

<span data-ttu-id="d8c94-144">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d8c94-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8c94-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8c94-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d8c94-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="d8c94-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="d8c94-147">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d8c94-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="d8c94-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="d8c94-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="d8c94-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8c94-149">RELATED LINKS</span></span>

