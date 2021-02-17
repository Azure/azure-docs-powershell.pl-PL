---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191442"
---
# <span data-ttu-id="0b621-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="0b621-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="0b621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b621-102">SYNOPSIS</span></span>
<span data-ttu-id="0b621-103">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="0b621-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0b621-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b621-104">SYNTAX</span></span>

### <span data-ttu-id="0b621-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="0b621-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b621-106">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="0b621-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b621-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="0b621-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b621-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b621-108">DESCRIPTION</span></span>
<span data-ttu-id="0b621-109">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="0b621-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0b621-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b621-110">EXAMPLES</span></span>

### <span data-ttu-id="0b621-111">Przykład 1. Tworzenie pulpitu nawigacyjnego przy użyciu pliku szablonu pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="0b621-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="0b621-112">Utwórz nowy pulpit nawigacyjny przy użyciu podanego pliku szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="0b621-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b621-113">PARAMETERS</span></span>

### <span data-ttu-id="0b621-114">— Pulpit nawigacyjny</span><span class="sxs-lookup"><span data-stu-id="0b621-114">-Dashboard</span></span>
<span data-ttu-id="0b621-115">Definicja zasobu udostępnionego pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="0b621-116">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach pulpitu nawigacyjnego i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="0b621-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-117">- DashboardPath</span><span class="sxs-lookup"><span data-stu-id="0b621-117">-DashboardPath</span></span>
<span data-ttu-id="0b621-118">Ścieżka do istniejącego szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="0b621-119">Szablony pulpitów nawigacyjnych można pobierać z portalu.</span><span class="sxs-lookup"><span data-stu-id="0b621-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b621-120">-DefaultProfile</span></span>
<span data-ttu-id="0b621-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b621-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b621-122">— Lens</span><span class="sxs-lookup"><span data-stu-id="0b621-122">-Lens</span></span>
<span data-ttu-id="0b621-123">Pulpit nawigacyjny został pochylił się.</span><span class="sxs-lookup"><span data-stu-id="0b621-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0b621-124">-Location</span></span>
<span data-ttu-id="0b621-125">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="0b621-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-126">— Metadane</span><span class="sxs-lookup"><span data-stu-id="0b621-126">-Metadata</span></span>
<span data-ttu-id="0b621-127">Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b621-128">-Name</span></span>
<span data-ttu-id="0b621-129">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b621-130">-ResourceGroupName</span></span>
<span data-ttu-id="0b621-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b621-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b621-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b621-132">-SubscriptionId</span></span>
<span data-ttu-id="0b621-133">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b621-133">The Azure subscription ID.</span></span>
<span data-ttu-id="0b621-134">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="0b621-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="0b621-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="0b621-135">-Tag</span></span>
<span data-ttu-id="0b621-136">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="0b621-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b621-137">-Confirm</span></span>
<span data-ttu-id="0b621-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b621-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b621-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b621-139">-WhatIf</span></span>
<span data-ttu-id="0b621-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b621-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b621-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b621-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b621-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b621-142">CommonParameters</span></span>
<span data-ttu-id="0b621-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b621-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b621-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b621-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b621-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b621-145">INPUTS</span></span>

### <span data-ttu-id="0b621-146">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="0b621-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="0b621-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b621-147">OUTPUTS</span></span>

### <span data-ttu-id="0b621-148">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="0b621-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="0b621-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b621-149">NOTES</span></span>

<span data-ttu-id="0b621-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0b621-150">ALIASES</span></span>

<span data-ttu-id="0b621-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0b621-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b621-152">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0b621-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b621-153">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b621-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b621-154">PULPIT <IDashboard> NAWIGACYJNY: definicja zasobów udostępnionego pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="0b621-155">`Location <String>`: lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="0b621-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="0b621-156">`[Lens <IDashboardPropertiesLenses>]`: Pulpit nawigacyjny jest podbłędny.</span><span class="sxs-lookup"><span data-stu-id="0b621-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="0b621-157">`[(Any) <IDashboardLens>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="0b621-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b621-158">`[Metadata <IDashboardPropertiesMetadata>]`: Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b621-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="0b621-159">`[(Any) <Object>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="0b621-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b621-160">`[Tag <IDashboardTags>]`: tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="0b621-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="0b621-161">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="0b621-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="0b621-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b621-162">RELATED LINKS</span></span>

