---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012570"
---
# <span data-ttu-id="19e21-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="19e21-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="19e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19e21-102">SYNOPSIS</span></span>
<span data-ttu-id="19e21-103">Tworzenie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="19e21-103">Create Organization resource</span></span>

## <span data-ttu-id="19e21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19e21-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="19e21-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="19e21-105">DESCRIPTION</span></span>
<span data-ttu-id="19e21-106">Tworzenie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="19e21-106">Create Organization resource</span></span>

## <span data-ttu-id="19e21-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19e21-107">EXAMPLES</span></span>

### <span data-ttu-id="19e21-108">Przykład 1. Tworzenie organizacji confluent</span><span class="sxs-lookup"><span data-stu-id="19e21-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="19e21-109">To polecenie tworzy organizację confluent.</span><span class="sxs-lookup"><span data-stu-id="19e21-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="19e21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19e21-110">PARAMETERS</span></span>

### <span data-ttu-id="19e21-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="19e21-111">-AsJob</span></span>
<span data-ttu-id="19e21-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="19e21-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e21-113">-DefaultProfile</span></span>
<span data-ttu-id="19e21-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19e21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e21-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="19e21-115">-Location</span></span>
<span data-ttu-id="19e21-116">Lokalizacja zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="19e21-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="19e21-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19e21-117">-Name</span></span>
<span data-ttu-id="19e21-118">Nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="19e21-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e21-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19e21-119">-NoWait</span></span>
<span data-ttu-id="19e21-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="19e21-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e21-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="19e21-121">-OfferDetailId</span></span>
<span data-ttu-id="19e21-122">Identyfikator oferty</span><span class="sxs-lookup"><span data-stu-id="19e21-122">Offer Id</span></span>

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

### <span data-ttu-id="19e21-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="19e21-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="19e21-124">Identyfikator planu oferty</span><span class="sxs-lookup"><span data-stu-id="19e21-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="19e21-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="19e21-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="19e21-126">Nazwa planu oferty</span><span class="sxs-lookup"><span data-stu-id="19e21-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="19e21-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="19e21-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="19e21-128">Identyfikator wydawcy</span><span class="sxs-lookup"><span data-stu-id="19e21-128">Publisher Id</span></span>

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

### <span data-ttu-id="19e21-129">- OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="19e21-129">-OfferDetailStatus</span></span>
<span data-ttu-id="19e21-130">Stan oferty SaaS</span><span class="sxs-lookup"><span data-stu-id="19e21-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e21-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="19e21-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="19e21-132">Jednostka okresu planu oferty</span><span class="sxs-lookup"><span data-stu-id="19e21-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="19e21-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e21-133">-ResourceGroupName</span></span>
<span data-ttu-id="19e21-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="19e21-134">Resource group name</span></span>

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

### <span data-ttu-id="19e21-135">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19e21-135">-SubscriptionId</span></span>
<span data-ttu-id="19e21-136">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="19e21-136">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="19e21-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="19e21-137">-Tag</span></span>
<span data-ttu-id="19e21-138">Tagi zasobów organizacji</span><span class="sxs-lookup"><span data-stu-id="19e21-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e21-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19e21-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="19e21-140">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="19e21-140">Email address</span></span>

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

### <span data-ttu-id="19e21-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="19e21-141">-UserDetailFirstName</span></span>
<span data-ttu-id="19e21-142">Imię</span><span class="sxs-lookup"><span data-stu-id="19e21-142">First name</span></span>

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

### <span data-ttu-id="19e21-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="19e21-143">-UserDetailLastName</span></span>
<span data-ttu-id="19e21-144">Nazwisko</span><span class="sxs-lookup"><span data-stu-id="19e21-144">Last name</span></span>

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

### <span data-ttu-id="19e21-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19e21-145">-Confirm</span></span>
<span data-ttu-id="19e21-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19e21-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e21-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e21-147">-WhatIf</span></span>
<span data-ttu-id="19e21-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e21-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e21-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19e21-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e21-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e21-150">CommonParameters</span></span>
<span data-ttu-id="19e21-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e21-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e21-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19e21-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e21-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19e21-153">INPUTS</span></span>

## <span data-ttu-id="19e21-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19e21-154">OUTPUTS</span></span>

### <span data-ttu-id="19e21-155">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="19e21-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="19e21-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19e21-156">NOTES</span></span>

<span data-ttu-id="19e21-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="19e21-157">ALIASES</span></span>

## <span data-ttu-id="19e21-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19e21-158">RELATED LINKS</span></span>

