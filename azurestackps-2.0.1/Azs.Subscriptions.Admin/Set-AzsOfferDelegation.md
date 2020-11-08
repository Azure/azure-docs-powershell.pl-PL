---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054302"
---
# <span data-ttu-id="d934e-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d934e-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="d934e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d934e-102">SYNOPSIS</span></span>
<span data-ttu-id="d934e-103">Utwórz lub Zaktualizuj delegowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="d934e-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d934e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d934e-104">SYNTAX</span></span>

### <span data-ttu-id="d934e-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d934e-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d934e-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="d934e-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d934e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d934e-107">DESCRIPTION</span></span>
<span data-ttu-id="d934e-108">Utwórz lub Zaktualizuj delegowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="d934e-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="d934e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d934e-109">EXAMPLES</span></span>

### <span data-ttu-id="d934e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d934e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="d934e-111">Umożliwia zaktualizowanie delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="d934e-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="d934e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d934e-112">PARAMETERS</span></span>

### <span data-ttu-id="d934e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d934e-113">-DefaultProfile</span></span>
<span data-ttu-id="d934e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d934e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d934e-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d934e-115">-Location</span></span>
<span data-ttu-id="d934e-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d934e-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d934e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d934e-117">-Name</span></span>
<span data-ttu-id="d934e-118">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="d934e-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="d934e-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="d934e-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="d934e-120">Oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="d934e-120">Offer delegation.</span></span>
<span data-ttu-id="d934e-121">Aby skonstruować, zobacz sekcję notatki dla właściwości OFFERDELEGATIONDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d934e-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d934e-122">-Offername</span><span class="sxs-lookup"><span data-stu-id="d934e-122">-OfferName</span></span>
<span data-ttu-id="d934e-123">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="d934e-123">Name of an offer.</span></span>

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

### <span data-ttu-id="d934e-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d934e-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="d934e-125">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="d934e-125">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="d934e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d934e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d934e-127">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="d934e-127">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d934e-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d934e-128">-SubscriptionId</span></span>
<span data-ttu-id="d934e-129">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d934e-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d934e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d934e-130">-Confirm</span></span>
<span data-ttu-id="d934e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d934e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d934e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d934e-132">-WhatIf</span></span>
<span data-ttu-id="d934e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d934e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d934e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d934e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d934e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d934e-135">CommonParameters</span></span>
<span data-ttu-id="d934e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d934e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d934e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d934e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d934e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d934e-138">INPUTS</span></span>

### <span data-ttu-id="d934e-139">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d934e-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="d934e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d934e-140">OUTPUTS</span></span>

### <span data-ttu-id="d934e-141">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d934e-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="d934e-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d934e-142">ALIASES</span></span>

## <span data-ttu-id="d934e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d934e-143">NOTES</span></span>

<span data-ttu-id="d934e-144">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d934e-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d934e-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d934e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d934e-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : oferuj delegowanie.</span><span class="sxs-lookup"><span data-stu-id="d934e-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="d934e-147">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d934e-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="d934e-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="d934e-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="d934e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d934e-149">RELATED LINKS</span></span>

