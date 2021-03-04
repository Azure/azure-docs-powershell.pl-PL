---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988947"
---
# <span data-ttu-id="f46c7-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f46c7-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="f46c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f46c7-103">Aktualizuje istniejący pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="f46c7-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="f46c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f46c7-104">SYNTAX</span></span>

### <span data-ttu-id="f46c7-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f46c7-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f46c7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f46c7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f46c7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f46c7-107">DESCRIPTION</span></span>
<span data-ttu-id="f46c7-108">Aktualizuje istniejący pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="f46c7-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="f46c7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f46c7-109">EXAMPLES</span></span>

### <span data-ttu-id="f46c7-110">Przykład 1. Aktualizowanie tagów pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="f46c7-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="f46c7-111">Aktualizowanie tagów na pulpicie nawigacyjnym.</span><span class="sxs-lookup"><span data-stu-id="f46c7-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="f46c7-112">Tagi są reprezentowane jako wbudowane skróty.</span><span class="sxs-lookup"><span data-stu-id="f46c7-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="f46c7-113">Przykład 2. Aktualizowanie tagów pulpitu nawigacyjnego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="f46c7-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="f46c7-114">Aktualizowanie tagów na pulpicie nawigacyjnym ponoszy za pomocą narzędzia Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="f46c7-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="f46c7-115">Umożliwia to aktualizowanie tagów na jednym pulpicie nawigacyjnym lub wielu pulpitach nawigacyjnych.</span><span class="sxs-lookup"><span data-stu-id="f46c7-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="f46c7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f46c7-116">PARAMETERS</span></span>

### <span data-ttu-id="f46c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46c7-117">-DefaultProfile</span></span>
<span data-ttu-id="f46c7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f46c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46c7-119">-InputObject</span></span>
<span data-ttu-id="f46c7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f46c7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f46c7-121">— Lens</span><span class="sxs-lookup"><span data-stu-id="f46c7-121">-Lens</span></span>
<span data-ttu-id="f46c7-122">Pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="f46c7-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="f46c7-123">— Metadane</span><span class="sxs-lookup"><span data-stu-id="f46c7-123">-Metadata</span></span>
<span data-ttu-id="f46c7-124">Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f46c7-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="f46c7-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f46c7-125">-Name</span></span>
<span data-ttu-id="f46c7-126">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f46c7-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="f46c7-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f46c7-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f46c7-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f46c7-129">-SubscriptionId</span></span>
<span data-ttu-id="f46c7-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f46c7-130">The Azure subscription ID.</span></span>
<span data-ttu-id="f46c7-131">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="f46c7-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="f46c7-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="f46c7-132">-Tag</span></span>
<span data-ttu-id="f46c7-133">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="f46c7-133">Resource tags</span></span>

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

### <span data-ttu-id="f46c7-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f46c7-134">-Confirm</span></span>
<span data-ttu-id="f46c7-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f46c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46c7-136">-WhatIf</span></span>
<span data-ttu-id="f46c7-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f46c7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46c7-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f46c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46c7-139">CommonParameters</span></span>
<span data-ttu-id="f46c7-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46c7-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f46c7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46c7-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f46c7-142">INPUTS</span></span>

### <span data-ttu-id="f46c7-143">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="f46c7-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="f46c7-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f46c7-144">OUTPUTS</span></span>

### <span data-ttu-id="f46c7-145">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="f46c7-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f46c7-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f46c7-146">NOTES</span></span>

<span data-ttu-id="f46c7-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f46c7-147">ALIASES</span></span>

<span data-ttu-id="f46c7-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f46c7-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f46c7-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f46c7-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f46c7-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f46c7-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f46c7-151">INPUTOBJECT: <IPortalIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f46c7-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f46c7-152">`[DashboardName <String>]`: nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f46c7-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="f46c7-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f46c7-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f46c7-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f46c7-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f46c7-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f46c7-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="f46c7-156">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="f46c7-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="f46c7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f46c7-157">RELATED LINKS</span></span>

