---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 60dcb163e480371fe211651cc929b6335877490b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000097"
---
# <span data-ttu-id="c3200-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="c3200-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="c3200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3200-102">SYNOPSIS</span></span>
<span data-ttu-id="c3200-103">Aktualizuje zapytanie wykresu, które już zostało dodane.</span><span class="sxs-lookup"><span data-stu-id="c3200-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="c3200-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3200-104">SYNTAX</span></span>

### <span data-ttu-id="c3200-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c3200-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3200-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3200-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3200-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3200-107">DESCRIPTION</span></span>
<span data-ttu-id="c3200-108">Aktualizuje zapytanie wykresu, które już zostało dodane.</span><span class="sxs-lookup"><span data-stu-id="c3200-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="c3200-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3200-109">EXAMPLES</span></span>

### <span data-ttu-id="c3200-110">Przykład 1. Aktualizowanie zapytania parametryowego i tagowanie według nazwy</span><span class="sxs-lookup"><span data-stu-id="c3200-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="c3200-111">To polecenie aktualizuje zapytanie parametryowe i tagowanie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="c3200-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="c3200-112">Przykład 2. Aktualizowanie pliku parametru według obiektu</span><span class="sxs-lookup"><span data-stu-id="c3200-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="c3200-113">To polecenie aktualizuje zapytanie parametryowe i tagowanie według obiektu.</span><span class="sxs-lookup"><span data-stu-id="c3200-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="c3200-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3200-114">PARAMETERS</span></span>

### <span data-ttu-id="c3200-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3200-115">-DefaultProfile</span></span>
<span data-ttu-id="c3200-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3200-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3200-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="c3200-117">-Description</span></span>
<span data-ttu-id="c3200-118">Opis zapytania wykresu.</span><span class="sxs-lookup"><span data-stu-id="c3200-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="c3200-119">— Plik</span><span class="sxs-lookup"><span data-stu-id="c3200-119">-File</span></span>
<span data-ttu-id="c3200-120">Zawartość pliku zostanie przekazana do parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="c3200-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="c3200-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3200-121">-InputObject</span></span>
<span data-ttu-id="c3200-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c3200-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3200-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3200-123">-Name</span></span>
<span data-ttu-id="c3200-124">Nazwa zasobu zapytanie programu Graph.</span><span class="sxs-lookup"><span data-stu-id="c3200-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="c3200-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="c3200-125">-Query</span></span>
<span data-ttu-id="c3200-126">Zapytanie KQL, które będzie grafem.</span><span class="sxs-lookup"><span data-stu-id="c3200-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="c3200-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3200-127">-ResourceGroupName</span></span>
<span data-ttu-id="c3200-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3200-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3200-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3200-129">-SubscriptionId</span></span>
<span data-ttu-id="c3200-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3200-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="c3200-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="c3200-131">-Tag</span></span>
<span data-ttu-id="c3200-132">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="c3200-132">Resource tags</span></span>

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

### <span data-ttu-id="c3200-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3200-133">-Confirm</span></span>
<span data-ttu-id="c3200-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3200-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3200-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3200-135">-WhatIf</span></span>
<span data-ttu-id="c3200-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3200-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3200-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3200-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3200-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3200-138">CommonParameters</span></span>
<span data-ttu-id="c3200-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3200-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3200-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3200-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3200-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3200-141">INPUTS</span></span>

### <span data-ttu-id="c3200-142">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="c3200-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="c3200-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3200-143">OUTPUTS</span></span>

### <span data-ttu-id="c3200-144">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="c3200-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="c3200-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3200-145">NOTES</span></span>

<span data-ttu-id="c3200-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c3200-146">ALIASES</span></span>

<span data-ttu-id="c3200-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3200-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3200-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c3200-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3200-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3200-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3200-150">INPUTOBJECT: <IResourceGraphIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c3200-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3200-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c3200-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3200-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3200-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c3200-153">`[ResourceName <String>]`: nazwa zasobu zapytania programu Graph.</span><span class="sxs-lookup"><span data-stu-id="c3200-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="c3200-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3200-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="c3200-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3200-155">RELATED LINKS</span></span>

