---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377895"
---
# <span data-ttu-id="1633c-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="1633c-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="1633c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1633c-102">SYNOPSIS</span></span>
<span data-ttu-id="1633c-103">Aktualizuje zapytanie wykresu, które zostało już dodane.</span><span class="sxs-lookup"><span data-stu-id="1633c-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="1633c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1633c-104">SYNTAX</span></span>

### <span data-ttu-id="1633c-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1633c-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1633c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1633c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1633c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1633c-107">DESCRIPTION</span></span>
<span data-ttu-id="1633c-108">Aktualizuje zapytanie wykresu, które zostało już dodane.</span><span class="sxs-lookup"><span data-stu-id="1633c-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="1633c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1633c-109">EXAMPLES</span></span>

### <span data-ttu-id="1633c-110">Przykład 1: aktualizowanie kwerendy parametrycznej i znacznika według nazwy</span><span class="sxs-lookup"><span data-stu-id="1633c-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="1633c-111">To polecenie powoduje zaktualizowanie kwerendy parametrycznej i znacznika za pomocą nazwy.</span><span class="sxs-lookup"><span data-stu-id="1633c-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="1633c-112">Przykład 2: aktualizowanie pliku parametrów według obiektów</span><span class="sxs-lookup"><span data-stu-id="1633c-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="1633c-113">To polecenie powoduje zaktualizowanie kwerendy parametrycznej i znacznika za pomocą obiektu.</span><span class="sxs-lookup"><span data-stu-id="1633c-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="1633c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1633c-114">PARAMETERS</span></span>

### <span data-ttu-id="1633c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1633c-115">-DefaultProfile</span></span>
<span data-ttu-id="1633c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1633c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1633c-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="1633c-117">-Description</span></span>
<span data-ttu-id="1633c-118">Opis zapytania dotyczącego wykresu.</span><span class="sxs-lookup"><span data-stu-id="1633c-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="1633c-119">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="1633c-119">-File</span></span>
<span data-ttu-id="1633c-120">Zawartość pliku zostanie przekazana do parametru zapytania.</span><span class="sxs-lookup"><span data-stu-id="1633c-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="1633c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1633c-121">-InputObject</span></span>
<span data-ttu-id="1633c-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1633c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1633c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1633c-123">-Name</span></span>
<span data-ttu-id="1633c-124">Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="1633c-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="1633c-125">-Query</span><span class="sxs-lookup"><span data-stu-id="1633c-125">-Query</span></span>
<span data-ttu-id="1633c-126">Kwerenda Keyword, która będzie wykresem.</span><span class="sxs-lookup"><span data-stu-id="1633c-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="1633c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1633c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1633c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1633c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1633c-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1633c-129">-SubscriptionId</span></span>
<span data-ttu-id="1633c-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1633c-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="1633c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1633c-131">-Tag</span></span>
<span data-ttu-id="1633c-132">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="1633c-132">Resource tags</span></span>

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

### <span data-ttu-id="1633c-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1633c-133">-Confirm</span></span>
<span data-ttu-id="1633c-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1633c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1633c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1633c-135">-WhatIf</span></span>
<span data-ttu-id="1633c-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1633c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1633c-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1633c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1633c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1633c-138">CommonParameters</span></span>
<span data-ttu-id="1633c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1633c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1633c-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1633c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1633c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1633c-141">INPUTS</span></span>

### <span data-ttu-id="1633c-142">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="1633c-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="1633c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1633c-143">OUTPUTS</span></span>

### <span data-ttu-id="1633c-144">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="1633c-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="1633c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1633c-145">NOTES</span></span>

<span data-ttu-id="1633c-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1633c-146">ALIASES</span></span>

<span data-ttu-id="1633c-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1633c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1633c-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1633c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1633c-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1633c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1633c-150">INPUTobject <IResourceGraphIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1633c-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1633c-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1633c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1633c-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1633c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1633c-153">`[ResourceName <String>]`: Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="1633c-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="1633c-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1633c-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="1633c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1633c-155">RELATED LINKS</span></span>

