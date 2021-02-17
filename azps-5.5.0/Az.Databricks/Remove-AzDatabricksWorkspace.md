---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180811"
---
# <span data-ttu-id="bf6e4-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf6e4-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="bf6e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6e4-103">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-103">Deletes the workspace.</span></span>

## <span data-ttu-id="bf6e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf6e4-104">SYNTAX</span></span>

### <span data-ttu-id="bf6e4-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="bf6e4-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf6e4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf6e4-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf6e4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf6e4-107">DESCRIPTION</span></span>
<span data-ttu-id="bf6e4-108">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-108">Deletes the workspace.</span></span>

## <span data-ttu-id="bf6e4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf6e4-109">EXAMPLES</span></span>

### <span data-ttu-id="bf6e4-110">Przykład 1. Usuwanie obszaru roboczego programu Databricks</span><span class="sxs-lookup"><span data-stu-id="bf6e4-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="bf6e4-111">To polecenie powoduje usunięcie obszaru roboczego programu Databricks z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="bf6e4-112">Przykład 2. Usuwanie obszaru roboczego z obszaru roboczego danych według obiektu</span><span class="sxs-lookup"><span data-stu-id="bf6e4-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="bf6e4-113">To polecenie powoduje usunięcie obszaru roboczego programu Databricks z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="bf6e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf6e4-114">PARAMETERS</span></span>

### <span data-ttu-id="bf6e4-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bf6e4-115">-AsJob</span></span>
<span data-ttu-id="bf6e4-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bf6e4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bf6e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6e4-117">-DefaultProfile</span></span>
<span data-ttu-id="bf6e4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf6e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf6e4-119">-InputObject</span></span>
<span data-ttu-id="bf6e4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bf6e4-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bf6e4-121">-Name</span></span>
<span data-ttu-id="bf6e4-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf6e4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf6e4-123">-NoWait</span></span>
<span data-ttu-id="bf6e4-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bf6e4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bf6e4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf6e4-125">-PassThru</span></span>
<span data-ttu-id="bf6e4-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bf6e4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf6e4-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf6e4-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-128">The name of the resource group.</span></span>
<span data-ttu-id="bf6e4-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf6e4-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf6e4-130">-SubscriptionId</span></span>
<span data-ttu-id="bf6e4-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf6e4-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf6e4-132">-Confirm</span></span>
<span data-ttu-id="bf6e4-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf6e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf6e4-134">-WhatIf</span></span>
<span data-ttu-id="bf6e4-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf6e4-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf6e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6e4-137">CommonParameters</span></span>
<span data-ttu-id="bf6e4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6e4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf6e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6e4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf6e4-140">INPUTS</span></span>

### <span data-ttu-id="bf6e4-141">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="bf6e4-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bf6e4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf6e4-142">OUTPUTS</span></span>

### <span data-ttu-id="bf6e4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf6e4-143">System.Boolean</span></span>

## <span data-ttu-id="bf6e4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf6e4-144">NOTES</span></span>

<span data-ttu-id="bf6e4-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bf6e4-145">ALIASES</span></span>

<span data-ttu-id="bf6e4-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bf6e4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf6e4-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf6e4-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf6e4-149">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bf6e4-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf6e4-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bf6e4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf6e4-151">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bf6e4-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bf6e4-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="bf6e4-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bf6e4-155">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="bf6e4-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bf6e4-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf6e4-156">RELATED LINKS</span></span>

