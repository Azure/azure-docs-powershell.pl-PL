---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242626"
---
# <span data-ttu-id="f16e4-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="f16e4-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="f16e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f16e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f16e4-103">Tworzy lub aktualizuje zasób przenoszenia w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="f16e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f16e4-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f16e4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f16e4-105">DESCRIPTION</span></span>
<span data-ttu-id="f16e4-106">Tworzy lub aktualizuje zasób przenoszenia w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="f16e4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f16e4-107">EXAMPLES</span></span>

### <span data-ttu-id="f16e4-108">Przykład 1. Dodawanie zasobu do kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="f16e4-109">Dodawanie zasobu do kolekcji przenoszenia w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f16e4-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="f16e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f16e4-110">PARAMETERS</span></span>

### <span data-ttu-id="f16e4-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f16e4-111">-AsJob</span></span>
<span data-ttu-id="f16e4-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f16e4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f16e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f16e4-113">-DefaultProfile</span></span>
<span data-ttu-id="f16e4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f16e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f16e4-115">- DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="f16e4-115">-DependsOnOverride</span></span>
<span data-ttu-id="f16e4-116">Pobiera lub ustawia zastępowanie zależności zasobów przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="f16e4-117">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach DEPENDSONOVERRIDE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f16e4-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16e4-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="f16e4-118">-ExistingTargetId</span></span>
<span data-ttu-id="f16e4-119">Pobiera lub ustawia istniejący identyfikator ARM zasobu.</span><span class="sxs-lookup"><span data-stu-id="f16e4-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="f16e4-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="f16e4-120">-MoveCollectionName</span></span>
<span data-ttu-id="f16e4-121">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f16e4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f16e4-122">-Name</span></span>
<span data-ttu-id="f16e4-123">Nazwa zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16e4-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f16e4-124">-NoWait</span></span>
<span data-ttu-id="f16e4-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f16e4-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f16e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f16e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f16e4-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f16e4-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f16e4-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="f16e4-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="f16e4-129">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="f16e4-129">The resource type.</span></span>
<span data-ttu-id="f16e4-130">Na przykład wartością może być Microsoft.Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="f16e4-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="f16e4-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="f16e4-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="f16e4-132">Pobiera lub ustawia nazwę zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="f16e4-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="f16e4-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="f16e4-133">-SourceId</span></span>
<span data-ttu-id="f16e4-134">Pobiera lub ustawia identyfikator ARM źródłowego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f16e4-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="f16e4-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="f16e4-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="f16e4-136">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="f16e4-136">The resource type.</span></span>
<span data-ttu-id="f16e4-137">Na przykład wartością może być Microsoft.Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="f16e4-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="f16e4-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="f16e4-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="f16e4-139">Pobiera lub ustawia nazwę zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="f16e4-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="f16e4-140">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f16e4-140">-SubscriptionId</span></span>
<span data-ttu-id="f16e4-141">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f16e4-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="f16e4-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f16e4-142">-Confirm</span></span>
<span data-ttu-id="f16e4-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f16e4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f16e4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f16e4-144">-WhatIf</span></span>
<span data-ttu-id="f16e4-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f16e4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f16e4-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f16e4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f16e4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16e4-147">CommonParameters</span></span>
<span data-ttu-id="f16e4-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f16e4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16e4-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f16e4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16e4-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f16e4-150">INPUTS</span></span>

## <span data-ttu-id="f16e4-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f16e4-151">OUTPUTS</span></span>

### <span data-ttu-id="f16e4-152">Microsoft.Azure.PowerShell.Cmdlet.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="f16e4-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="f16e4-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f16e4-153">NOTES</span></span>

<span data-ttu-id="f16e4-154">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f16e4-154">ALIASES</span></span>

<span data-ttu-id="f16e4-155">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f16e4-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f16e4-156">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f16e4-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f16e4-157">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f16e4-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f16e4-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Pobiera lub ustawia zastępowanie zależności zasobów przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f16e4-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="f16e4-159">`[Id <String>]`: Pobiera lub ustawia ARM identyfikatora zasobu zależnego.</span><span class="sxs-lookup"><span data-stu-id="f16e4-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="f16e4-160">`[TargetId <String>]`: Pobiera lub ustawia ARM identyfikatora zasobu albo identyfikatora ARM MoveResource lub zasobu zależnego.</span><span class="sxs-lookup"><span data-stu-id="f16e4-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="f16e4-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f16e4-161">RELATED LINKS</span></span>

