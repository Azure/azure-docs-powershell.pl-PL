---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180819"
---
# <span data-ttu-id="b1c31-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="b1c31-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="b1c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1c31-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c31-103">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="b1c31-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="b1c31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b1c31-104">SYNTAX</span></span>

### <span data-ttu-id="b1c31-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="b1c31-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c31-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1c31-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1c31-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b1c31-107">DESCRIPTION</span></span>
<span data-ttu-id="b1c31-108">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="b1c31-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="b1c31-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b1c31-109">EXAMPLES</span></span>

### <span data-ttu-id="b1c31-110">Przykład 1. Usuwanie komunikacji równorzędnej w sieci VNET z danymibricks według nazwy</span><span class="sxs-lookup"><span data-stu-id="b1c31-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="b1c31-111">To polecenie usuwa komunikacji równorzędnej w sieci VNET z danymibricks według nazwy</span><span class="sxs-lookup"><span data-stu-id="b1c31-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="b1c31-112">Przykład 2. Usuwanie komunikacji równorzędnej w sieci VNET z przechyłki danych według obiektu</span><span class="sxs-lookup"><span data-stu-id="b1c31-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="b1c31-113">To polecenie usuwa komunikacji równorzędnej w sieci VNET z danymibricks według obiektu</span><span class="sxs-lookup"><span data-stu-id="b1c31-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="b1c31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1c31-114">PARAMETERS</span></span>

### <span data-ttu-id="b1c31-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b1c31-115">-AsJob</span></span>
<span data-ttu-id="b1c31-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b1c31-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b1c31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c31-117">-DefaultProfile</span></span>
<span data-ttu-id="b1c31-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c31-119">-InputObject</span></span>
<span data-ttu-id="b1c31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b1c31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c31-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b1c31-121">-Name</span></span>
<span data-ttu-id="b1c31-122">Nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b1c31-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="b1c31-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1c31-123">-NoWait</span></span>
<span data-ttu-id="b1c31-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b1c31-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1c31-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1c31-125">-PassThru</span></span>
<span data-ttu-id="b1c31-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b1c31-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1c31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c31-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1c31-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1c31-128">The name of the resource group.</span></span>
<span data-ttu-id="b1c31-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b1c31-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b1c31-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1c31-130">-SubscriptionId</span></span>
<span data-ttu-id="b1c31-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b1c31-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b1c31-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1c31-132">-WorkspaceName</span></span>
<span data-ttu-id="b1c31-133">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b1c31-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="b1c31-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1c31-134">-Confirm</span></span>
<span data-ttu-id="b1c31-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b1c31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c31-136">-WhatIf</span></span>
<span data-ttu-id="b1c31-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c31-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b1c31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c31-139">CommonParameters</span></span>
<span data-ttu-id="b1c31-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c31-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1c31-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c31-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1c31-142">INPUTS</span></span>

### <span data-ttu-id="b1c31-143">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="b1c31-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b1c31-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1c31-144">OUTPUTS</span></span>

### <span data-ttu-id="b1c31-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1c31-145">System.Boolean</span></span>

## <span data-ttu-id="b1c31-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b1c31-146">NOTES</span></span>

<span data-ttu-id="b1c31-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b1c31-147">ALIASES</span></span>

<span data-ttu-id="b1c31-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b1c31-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1c31-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b1c31-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1c31-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1c31-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1c31-151">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b1c31-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1c31-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b1c31-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1c31-153">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b1c31-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b1c31-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1c31-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b1c31-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b1c31-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b1c31-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b1c31-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b1c31-157">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b1c31-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b1c31-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1c31-158">RELATED LINKS</span></span>

