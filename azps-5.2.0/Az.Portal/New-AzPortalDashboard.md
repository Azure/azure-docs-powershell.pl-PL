---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370895"
---
# <span data-ttu-id="b890a-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="b890a-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="b890a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b890a-102">SYNOPSIS</span></span>
<span data-ttu-id="b890a-103">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="b890a-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="b890a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b890a-104">SYNTAX</span></span>

### <span data-ttu-id="b890a-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b890a-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b890a-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="b890a-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b890a-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="b890a-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b890a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b890a-108">DESCRIPTION</span></span>
<span data-ttu-id="b890a-109">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="b890a-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="b890a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b890a-110">EXAMPLES</span></span>

### <span data-ttu-id="b890a-111">Przykład 1. tworzenie pulpitu nawigacyjnego przy użyciu pliku szablonu pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="b890a-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="b890a-112">Utwórz nowy pulpit nawigacyjny przy użyciu podanego pliku szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="b890a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b890a-113">PARAMETERS</span></span>

### <span data-ttu-id="b890a-114">— Pulpit nawigacyjny</span><span class="sxs-lookup"><span data-stu-id="b890a-114">-Dashboard</span></span>
<span data-ttu-id="b890a-115">Definicja zasobu udostępnionego pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="b890a-116">Aby skonstruować, zobacz sekcję notatki dla właściwości pulpitu NAWIGACYJNego i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b890a-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="b890a-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="b890a-117">-DashboardPath</span></span>
<span data-ttu-id="b890a-118">Ścieżka do istniejącego szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="b890a-119">Szablony pulpitu nawigacyjnego mogą być pobierane z portalu.</span><span class="sxs-lookup"><span data-stu-id="b890a-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="b890a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b890a-120">-DefaultProfile</span></span>
<span data-ttu-id="b890a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b890a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b890a-122">-Soczewki</span><span class="sxs-lookup"><span data-stu-id="b890a-122">-Lens</span></span>
<span data-ttu-id="b890a-123">Soczewki na pulpicie nawigacyjnym.</span><span class="sxs-lookup"><span data-stu-id="b890a-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="b890a-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b890a-124">-Location</span></span>
<span data-ttu-id="b890a-125">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="b890a-125">Resource location</span></span>

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

### <span data-ttu-id="b890a-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b890a-126">-Metadata</span></span>
<span data-ttu-id="b890a-127">Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="b890a-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b890a-128">-Name</span></span>
<span data-ttu-id="b890a-129">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="b890a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b890a-130">-ResourceGroupName</span></span>
<span data-ttu-id="b890a-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b890a-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="b890a-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b890a-132">-SubscriptionId</span></span>
<span data-ttu-id="b890a-133">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b890a-133">The Azure subscription ID.</span></span>
<span data-ttu-id="b890a-134">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b890a-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="b890a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b890a-135">-Tag</span></span>
<span data-ttu-id="b890a-136">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="b890a-136">Resource tags</span></span>

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

### <span data-ttu-id="b890a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b890a-137">-Confirm</span></span>
<span data-ttu-id="b890a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b890a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b890a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b890a-139">-WhatIf</span></span>
<span data-ttu-id="b890a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b890a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b890a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b890a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b890a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b890a-142">CommonParameters</span></span>
<span data-ttu-id="b890a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b890a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b890a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b890a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b890a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b890a-145">INPUTS</span></span>

### <span data-ttu-id="b890a-146">Microsoft. Azure. PowerShell. cmdlet. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="b890a-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="b890a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b890a-147">OUTPUTS</span></span>

### <span data-ttu-id="b890a-148">Microsoft. Azure. PowerShell. cmdlet. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="b890a-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="b890a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b890a-149">NOTES</span></span>

<span data-ttu-id="b890a-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b890a-150">ALIASES</span></span>

<span data-ttu-id="b890a-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b890a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b890a-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b890a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b890a-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b890a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b890a-154">Pulpit NAWIGACYJNy <IDashboard> : definicja zasobu udostępnionego pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="b890a-155">`Location <String>`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="b890a-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="b890a-156">`[Lens <IDashboardPropertiesLenses>]`: Soczewki na pulpicie nawigacyjnym.</span><span class="sxs-lookup"><span data-stu-id="b890a-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="b890a-157">`[(Any) <IDashboardLens>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="b890a-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b890a-158">`[Metadata <IDashboardPropertiesMetadata>]`: Metadane pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b890a-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="b890a-159">`[(Any) <Object>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="b890a-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b890a-160">`[Tag <IDashboardTags>]`: Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="b890a-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="b890a-161">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="b890a-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="b890a-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b890a-162">RELATED LINKS</span></span>

