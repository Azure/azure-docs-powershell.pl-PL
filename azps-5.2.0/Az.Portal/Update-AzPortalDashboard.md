---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355201"
---
# <span data-ttu-id="7df21-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="7df21-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="7df21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7df21-102">SYNOPSIS</span></span>
<span data-ttu-id="7df21-103">Aktualizuje istniejący pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="7df21-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="7df21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7df21-104">SYNTAX</span></span>

### <span data-ttu-id="7df21-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7df21-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7df21-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7df21-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7df21-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7df21-107">DESCRIPTION</span></span>
<span data-ttu-id="7df21-108">Aktualizuje istniejący pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="7df21-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="7df21-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7df21-109">EXAMPLES</span></span>

### <span data-ttu-id="7df21-110">Przykład 1: aktualizowanie tagów pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="7df21-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="7df21-111">Zaktualizuj znaczniki na pulpicie nawigacyjnym.</span><span class="sxs-lookup"><span data-stu-id="7df21-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="7df21-112">Tagi są reprezentowane jako wbudowana obiekt Hashtable.</span><span class="sxs-lookup"><span data-stu-id="7df21-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="7df21-113">Przykład 2: aktualizowanie tagów pulpitu nawigacyjnego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="7df21-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="7df21-114">Zaktualizuj znaczniki na pulpicie nawigacyjnym, ponawiając próbę użycia polecenia Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="7df21-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="7df21-115">Można go użyć w celu zaktualizowania znaczników na jednym pulpicie nawigacyjnym lub wielu dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="7df21-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="7df21-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7df21-116">PARAMETERS</span></span>

### <span data-ttu-id="7df21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df21-117">-DefaultProfile</span></span>
<span data-ttu-id="7df21-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7df21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df21-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7df21-119">-InputObject</span></span>
<span data-ttu-id="7df21-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7df21-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7df21-121">-Soczewki</span><span class="sxs-lookup"><span data-stu-id="7df21-121">-Lens</span></span>
<span data-ttu-id="7df21-122">Soczewki na pulpicie nawigacyjnym.</span><span class="sxs-lookup"><span data-stu-id="7df21-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="7df21-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7df21-123">-Metadata</span></span>
<span data-ttu-id="7df21-124">Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="7df21-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="7df21-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7df21-125">-Name</span></span>
<span data-ttu-id="7df21-126">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="7df21-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="7df21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df21-127">-ResourceGroupName</span></span>
<span data-ttu-id="7df21-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7df21-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="7df21-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7df21-129">-SubscriptionId</span></span>
<span data-ttu-id="7df21-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7df21-130">The Azure subscription ID.</span></span>
<span data-ttu-id="7df21-131">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7df21-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7df21-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="7df21-132">-Tag</span></span>
<span data-ttu-id="7df21-133">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="7df21-133">Resource tags</span></span>

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

### <span data-ttu-id="7df21-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7df21-134">-Confirm</span></span>
<span data-ttu-id="7df21-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df21-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df21-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df21-136">-WhatIf</span></span>
<span data-ttu-id="7df21-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df21-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df21-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7df21-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df21-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df21-139">CommonParameters</span></span>
<span data-ttu-id="7df21-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df21-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df21-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df21-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df21-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7df21-142">INPUTS</span></span>

### <span data-ttu-id="7df21-143">Microsoft. Azure. PowerShell. polecenia cmdlet. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="7df21-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="7df21-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7df21-144">OUTPUTS</span></span>

### <span data-ttu-id="7df21-145">Microsoft. Azure. PowerShell. cmdlet. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="7df21-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="7df21-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7df21-146">NOTES</span></span>

<span data-ttu-id="7df21-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7df21-147">ALIASES</span></span>

<span data-ttu-id="7df21-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7df21-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7df21-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7df21-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7df21-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7df21-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7df21-151">INPUTobject <IPortalIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7df21-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7df21-152">`[DashboardName <String>]`: Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="7df21-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="7df21-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7df21-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7df21-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7df21-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7df21-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7df21-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7df21-156">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7df21-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7df21-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7df21-157">RELATED LINKS</span></span>

