---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176434"
---
# <span data-ttu-id="57a8c-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="57a8c-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="57a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="57a8c-103">Usuwanie zapytania wykresu.</span><span class="sxs-lookup"><span data-stu-id="57a8c-103">Delete a graph query.</span></span>

## <span data-ttu-id="57a8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57a8c-104">SYNTAX</span></span>

### <span data-ttu-id="57a8c-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="57a8c-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57a8c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57a8c-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57a8c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="57a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="57a8c-108">Usuwanie zapytania wykresu.</span><span class="sxs-lookup"><span data-stu-id="57a8c-108">Delete a graph query.</span></span>

## <span data-ttu-id="57a8c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57a8c-109">EXAMPLES</span></span>

### <span data-ttu-id="57a8c-110">Przykład 1. Usuwanie zapytania wykresu zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="57a8c-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="57a8c-111">To polecenie usuwa zapytanie wykresu zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="57a8c-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="57a8c-112">Przykład 2. Usuwanie zapytania wykresu zasobu według obiektu</span><span class="sxs-lookup"><span data-stu-id="57a8c-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="57a8c-113">To polecenie usuwa zapytanie wykresu zasobów według obiektów.</span><span class="sxs-lookup"><span data-stu-id="57a8c-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="57a8c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57a8c-114">PARAMETERS</span></span>

### <span data-ttu-id="57a8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a8c-115">-DefaultProfile</span></span>
<span data-ttu-id="57a8c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57a8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a8c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a8c-117">-InputObject</span></span>
<span data-ttu-id="57a8c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="57a8c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57a8c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57a8c-119">-Name</span></span>
<span data-ttu-id="57a8c-120">Nazwa zasobu zapytanie programu Graph.</span><span class="sxs-lookup"><span data-stu-id="57a8c-120">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a8c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a8c-121">-PassThru</span></span>
<span data-ttu-id="57a8c-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="57a8c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57a8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="57a8c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57a8c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a8c-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57a8c-125">-SubscriptionId</span></span>
<span data-ttu-id="57a8c-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57a8c-126">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a8c-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57a8c-127">-Confirm</span></span>
<span data-ttu-id="57a8c-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="57a8c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a8c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a8c-129">-WhatIf</span></span>
<span data-ttu-id="57a8c-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a8c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a8c-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="57a8c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a8c-132">CommonParameters</span></span>
<span data-ttu-id="57a8c-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a8c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57a8c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a8c-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57a8c-135">INPUTS</span></span>

### <span data-ttu-id="57a8c-136">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="57a8c-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="57a8c-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57a8c-137">OUTPUTS</span></span>

### <span data-ttu-id="57a8c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57a8c-138">System.Boolean</span></span>

## <span data-ttu-id="57a8c-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57a8c-139">NOTES</span></span>

<span data-ttu-id="57a8c-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="57a8c-140">ALIASES</span></span>

<span data-ttu-id="57a8c-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="57a8c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57a8c-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="57a8c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57a8c-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57a8c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57a8c-144">INPUTOBJECT: <IResourceGraphIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="57a8c-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57a8c-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="57a8c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57a8c-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57a8c-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="57a8c-147">`[ResourceName <String>]`: nazwa zasobu zapytania programu Graph.</span><span class="sxs-lookup"><span data-stu-id="57a8c-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="57a8c-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57a8c-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="57a8c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57a8c-149">RELATED LINKS</span></span>

