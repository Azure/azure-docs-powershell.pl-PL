---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232690"
---
# <span data-ttu-id="3835f-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3835f-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="3835f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3835f-102">SYNOPSIS</span></span>
<span data-ttu-id="3835f-103">Tworzy lub aktualizuje zasób Przenieś w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="3835f-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="3835f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3835f-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3835f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3835f-105">DESCRIPTION</span></span>
<span data-ttu-id="3835f-106">Tworzy lub aktualizuje zasób Przenieś w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="3835f-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="3835f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3835f-107">EXAMPLES</span></span>

### <span data-ttu-id="3835f-108">Przykład 1: Dodawanie zasobu do kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="3835f-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="3835f-109">Dodawanie zasobu do kolekcji Move w ramach określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="3835f-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="3835f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3835f-110">PARAMETERS</span></span>

### <span data-ttu-id="3835f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3835f-111">-AsJob</span></span>
<span data-ttu-id="3835f-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3835f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3835f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3835f-113">-DefaultProfile</span></span>
<span data-ttu-id="3835f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3835f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3835f-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="3835f-115">-DependsOnOverride</span></span>
<span data-ttu-id="3835f-116">Pobiera lub ustawia zastąpienia funkcji Przenieś zależności zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="3835f-117">Aby skonstruować, zobacz sekcję notatki dla właściwości DEPENDSONOVERRIDE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3835f-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3835f-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="3835f-118">-ExistingTargetId</span></span>
<span data-ttu-id="3835f-119">Pobiera lub ustawia istniejący docelowy identyfikator ARM zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="3835f-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3835f-120">-MoveCollectionName</span></span>
<span data-ttu-id="3835f-121">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="3835f-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3835f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3835f-122">-Name</span></span>
<span data-ttu-id="3835f-123">Nazwa przeniesienia zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="3835f-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3835f-124">-NoWait</span></span>
<span data-ttu-id="3835f-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3835f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3835f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3835f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3835f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3835f-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3835f-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="3835f-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="3835f-129">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-129">The resource type.</span></span>
<span data-ttu-id="3835f-130">Na przykład wartością może być Microsoft. COMPUTE/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="3835f-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="3835f-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="3835f-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="3835f-132">Pobiera lub ustawia nazwę zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="3835f-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="3835f-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="3835f-133">-SourceId</span></span>
<span data-ttu-id="3835f-134">Pobiera lub ustawia identyfikator RAMIENIa źródłowego zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="3835f-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="3835f-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="3835f-136">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-136">The resource type.</span></span>
<span data-ttu-id="3835f-137">Na przykład wartością może być Microsoft. COMPUTE/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="3835f-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="3835f-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="3835f-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="3835f-139">Pobiera lub ustawia nazwę zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="3835f-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="3835f-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3835f-140">-SubscriptionId</span></span>
<span data-ttu-id="3835f-141">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="3835f-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="3835f-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3835f-142">-Confirm</span></span>
<span data-ttu-id="3835f-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3835f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3835f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3835f-144">-WhatIf</span></span>
<span data-ttu-id="3835f-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3835f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3835f-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3835f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3835f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3835f-147">CommonParameters</span></span>
<span data-ttu-id="3835f-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3835f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3835f-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3835f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3835f-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3835f-150">INPUTS</span></span>

## <span data-ttu-id="3835f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3835f-151">OUTPUTS</span></span>

### <span data-ttu-id="3835f-152">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="3835f-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="3835f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3835f-153">NOTES</span></span>

<span data-ttu-id="3835f-154">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3835f-154">ALIASES</span></span>

<span data-ttu-id="3835f-155">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3835f-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3835f-156">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3835f-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3835f-157">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3835f-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3835f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: Pobiera lub ustawia zastąpienia funkcji Przenieś zależności zasobu.</span><span class="sxs-lookup"><span data-stu-id="3835f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="3835f-159">`[Id <String>]`: Pobiera lub ustawia identyfikator ARM zasobu zależnego.</span><span class="sxs-lookup"><span data-stu-id="3835f-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="3835f-160">`[TargetId <String>]`: Pobiera lub ustawia identyfikator ARM zasobu MoveResource lub identyfikator ARM zasobu zależnego.</span><span class="sxs-lookup"><span data-stu-id="3835f-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="3835f-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3835f-161">RELATED LINKS</span></span>

