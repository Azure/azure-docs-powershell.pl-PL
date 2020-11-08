---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsplan
schema: 2.0.0
ms.openlocfilehash: 2e78b28705b625836d9020c5ddf1652f4bdc7a7d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054066"
---
# <span data-ttu-id="de56f-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="de56f-101">Set-AzsPlan</span></span>

## <span data-ttu-id="de56f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de56f-102">SYNOPSIS</span></span>
<span data-ttu-id="de56f-103">Utwórz lub zaktualizuj plan.</span><span class="sxs-lookup"><span data-stu-id="de56f-103">Create or update the plan.</span></span>

## <span data-ttu-id="de56f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de56f-104">SYNTAX</span></span>

### <span data-ttu-id="de56f-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de56f-105">UpdateExpanded (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>] [-PropertiesName <String>]
 [-QuotaIds <String[]>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de56f-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="de56f-106">Update</span></span>
```
Set-AzsPlan -PlanDefinition <IPlan> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de56f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de56f-107">DESCRIPTION</span></span>
<span data-ttu-id="de56f-108">Utwórz lub zaktualizuj plan.</span><span class="sxs-lookup"><span data-stu-id="de56f-108">Create or update the plan.</span></span>

## <span data-ttu-id="de56f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de56f-109">EXAMPLES</span></span>

### <span data-ttu-id="de56f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de56f-110">Example 1</span></span>
```powershell
PS C:\> $Plan = Get-AzsPlan | Select-Object -First 1
$Plan.Description = 'update plan'
$Plan | Set-AzsPlan

Description         : update plan
DisplayName         : DRPTestPlan5056-test-test-test
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056
Location            : redmond
Name                : DRPTestPlan5056
PropertiesName      : DRPTestPlan5056
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Storage.Admin/locations/redmond/quotas/Default Quota, 
                      /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Compute.Admin/locations/redmond/quotas/Default Quota}
SkuIds              : 
SubscriptionCount   : 5
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="de56f-111">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="de56f-111">Updates the specified plan</span></span>

## <span data-ttu-id="de56f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de56f-112">PARAMETERS</span></span>

### <span data-ttu-id="de56f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de56f-113">-DefaultProfile</span></span>
<span data-ttu-id="de56f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de56f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de56f-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="de56f-115">-Description</span></span>
<span data-ttu-id="de56f-116">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-116">Description of the plan.</span></span>

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

### <span data-ttu-id="de56f-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de56f-117">-DisplayName</span></span>
<span data-ttu-id="de56f-118">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="de56f-118">Display name.</span></span>

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

### <span data-ttu-id="de56f-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="de56f-119">-ExternalReferenceId</span></span>
<span data-ttu-id="de56f-120">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="de56f-120">External reference identifier.</span></span>

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

### <span data-ttu-id="de56f-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de56f-121">-Location</span></span>
<span data-ttu-id="de56f-122">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="de56f-122">Location of the resource</span></span>

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

### <span data-ttu-id="de56f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de56f-123">-Name</span></span>
<span data-ttu-id="de56f-124">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-124">Name of the plan.</span></span>

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

### <span data-ttu-id="de56f-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="de56f-125">-PlanDefinition</span></span>
<span data-ttu-id="de56f-126">Plan przedstawia pakiet przydziałów i możliwości oferowanych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="de56f-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="de56f-127">Dzierżawa może uzyskać ten plan za pośrednictwem oferty uaktualnienia jej dostępu do podstawowych usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="de56f-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="de56f-128">Aby skonstruować, zobacz sekcję notatki dla właściwości PLANDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="de56f-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="de56f-129">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="de56f-129">-PropertiesName</span></span>
<span data-ttu-id="de56f-130">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-130">Name of the plan.</span></span>

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

### <span data-ttu-id="de56f-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="de56f-131">-QuotaIds</span></span>
<span data-ttu-id="de56f-132">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="de56f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de56f-133">-ResourceGroupName</span></span>
<span data-ttu-id="de56f-134">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="de56f-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="de56f-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="de56f-135">-SkuIds</span></span>
<span data-ttu-id="de56f-136">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="de56f-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="de56f-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="de56f-137">-SubscriptionCount</span></span>
<span data-ttu-id="de56f-138">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="de56f-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="de56f-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="de56f-139">-SubscriptionId</span></span>
<span data-ttu-id="de56f-140">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="de56f-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de56f-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de56f-141">-Confirm</span></span>
<span data-ttu-id="de56f-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de56f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de56f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de56f-143">-WhatIf</span></span>
<span data-ttu-id="de56f-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de56f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de56f-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de56f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de56f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de56f-146">CommonParameters</span></span>
<span data-ttu-id="de56f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de56f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de56f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de56f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de56f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de56f-149">INPUTS</span></span>

### <span data-ttu-id="de56f-150">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="de56f-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="de56f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de56f-151">OUTPUTS</span></span>

### <span data-ttu-id="de56f-152">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="de56f-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="de56f-153">PISUJE</span><span class="sxs-lookup"><span data-stu-id="de56f-153">ALIASES</span></span>

## <span data-ttu-id="de56f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de56f-154">NOTES</span></span>

<span data-ttu-id="de56f-155">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="de56f-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de56f-156">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de56f-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="de56f-157">PLANDEFINITION <IPlan> : plan przedstawia pakiet przydziałów i możliwości oferowanych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="de56f-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="de56f-158">Dzierżawa może uzyskać ten plan za pośrednictwem oferty uaktualnienia jej dostępu do podstawowych usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="de56f-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="de56f-159">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="de56f-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="de56f-160">`[Description <String>]`: Opis planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="de56f-161">`[DisplayName <String>]`: Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="de56f-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="de56f-162">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="de56f-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="de56f-163">`[PropertiesName <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="de56f-164">`[QuotaIds <String[]>]`: Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="de56f-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="de56f-165">`[SkuIds <String[]>]`: Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="de56f-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="de56f-166">`[SubscriptionCount <Int32?>]`: Liczba subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="de56f-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="de56f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de56f-167">RELATED LINKS</span></span>

