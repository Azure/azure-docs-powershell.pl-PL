---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012561"
---
# <span data-ttu-id="74c96-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="74c96-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="74c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c96-102">SYNOPSIS</span></span>
<span data-ttu-id="74c96-103">Aktualizowanie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="74c96-103">Update Organization resource</span></span>

## <span data-ttu-id="74c96-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74c96-104">SYNTAX</span></span>

### <span data-ttu-id="74c96-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="74c96-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74c96-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="74c96-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74c96-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="74c96-107">DESCRIPTION</span></span>
<span data-ttu-id="74c96-108">Aktualizowanie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="74c96-108">Update Organization resource</span></span>

## <span data-ttu-id="74c96-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74c96-109">EXAMPLES</span></span>

### <span data-ttu-id="74c96-110">Przykład 1. Aktualizowanie organizacji confluenta według nazwy</span><span class="sxs-lookup"><span data-stu-id="74c96-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="74c96-111">To polecenie aktualizuje organizację, która się nawiązyła, według nazwy.</span><span class="sxs-lookup"><span data-stu-id="74c96-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="74c96-112">Przykład 2. Aktualizowanie organizacji sypkiej według potoku</span><span class="sxs-lookup"><span data-stu-id="74c96-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="74c96-113">To polecenie aktualizuje organizację, która się ułozyła, według potoku.</span><span class="sxs-lookup"><span data-stu-id="74c96-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="74c96-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c96-114">PARAMETERS</span></span>

### <span data-ttu-id="74c96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c96-115">-DefaultProfile</span></span>
<span data-ttu-id="74c96-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74c96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c96-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74c96-117">-InputObject</span></span>
<span data-ttu-id="74c96-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="74c96-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74c96-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74c96-119">-Name</span></span>
<span data-ttu-id="74c96-120">Nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="74c96-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c96-121">-ResourceGroupName</span></span>
<span data-ttu-id="74c96-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="74c96-122">Resource group name</span></span>

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

### <span data-ttu-id="74c96-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74c96-123">-SubscriptionId</span></span>
<span data-ttu-id="74c96-124">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="74c96-124">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c96-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="74c96-125">-Tag</span></span>
<span data-ttu-id="74c96-126">ARM tagów zasobów</span><span class="sxs-lookup"><span data-stu-id="74c96-126">ARM resource tags</span></span>

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

### <span data-ttu-id="74c96-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74c96-127">-Confirm</span></span>
<span data-ttu-id="74c96-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74c96-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c96-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c96-129">-WhatIf</span></span>
<span data-ttu-id="74c96-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c96-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c96-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74c96-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c96-132">CommonParameters</span></span>
<span data-ttu-id="74c96-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c96-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c96-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c96-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74c96-135">INPUTS</span></span>

### <span data-ttu-id="74c96-136">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="74c96-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="74c96-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74c96-137">OUTPUTS</span></span>

### <span data-ttu-id="74c96-138">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="74c96-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="74c96-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74c96-139">NOTES</span></span>

<span data-ttu-id="74c96-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="74c96-140">ALIASES</span></span>

<span data-ttu-id="74c96-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74c96-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74c96-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="74c96-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74c96-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74c96-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74c96-144">INPUTOBJECT: <IConfluentIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="74c96-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74c96-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="74c96-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74c96-146">`[OrganizationName <String>]`: nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="74c96-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="74c96-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="74c96-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="74c96-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="74c96-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="74c96-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74c96-149">RELATED LINKS</span></span>

