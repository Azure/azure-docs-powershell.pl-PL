---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980762"
---
# <span data-ttu-id="8d45b-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="8d45b-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="8d45b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d45b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d45b-103">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="8d45b-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="8d45b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d45b-104">SYNTAX</span></span>

### <span data-ttu-id="8d45b-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="8d45b-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d45b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d45b-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d45b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d45b-107">DESCRIPTION</span></span>
<span data-ttu-id="8d45b-108">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="8d45b-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="8d45b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d45b-109">EXAMPLES</span></span>

### <span data-ttu-id="8d45b-110">Przykład 1. Usuwanie komunikacji równorzędnej w sieci VNET dla danychbricks według nazwy</span><span class="sxs-lookup"><span data-stu-id="8d45b-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="8d45b-111">To polecenie usuwa komunikacji równorzędnej w sieci VNET z danymibricks według nazwy</span><span class="sxs-lookup"><span data-stu-id="8d45b-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="8d45b-112">Przykład 2. Usuwanie komunikacji równorzędnej w sieci VNET z przechyłki danych według obiektu</span><span class="sxs-lookup"><span data-stu-id="8d45b-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="8d45b-113">To polecenie usuwa komunikacji równorzędnej w sieci VNET z danymibricks według obiektu</span><span class="sxs-lookup"><span data-stu-id="8d45b-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="8d45b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d45b-114">PARAMETERS</span></span>

### <span data-ttu-id="8d45b-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8d45b-115">-AsJob</span></span>
<span data-ttu-id="8d45b-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8d45b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8d45b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d45b-117">-DefaultProfile</span></span>
<span data-ttu-id="8d45b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d45b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d45b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d45b-119">-InputObject</span></span>
<span data-ttu-id="8d45b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8d45b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d45b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d45b-121">-Name</span></span>
<span data-ttu-id="8d45b-122">Nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8d45b-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="8d45b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d45b-123">-NoWait</span></span>
<span data-ttu-id="8d45b-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8d45b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d45b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d45b-125">-PassThru</span></span>
<span data-ttu-id="8d45b-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8d45b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8d45b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d45b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d45b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d45b-128">The name of the resource group.</span></span>
<span data-ttu-id="8d45b-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8d45b-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d45b-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d45b-130">-SubscriptionId</span></span>
<span data-ttu-id="8d45b-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d45b-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d45b-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8d45b-132">-WorkspaceName</span></span>
<span data-ttu-id="8d45b-133">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8d45b-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="8d45b-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d45b-134">-Confirm</span></span>
<span data-ttu-id="8d45b-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d45b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d45b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d45b-136">-WhatIf</span></span>
<span data-ttu-id="8d45b-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d45b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d45b-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d45b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d45b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d45b-139">CommonParameters</span></span>
<span data-ttu-id="8d45b-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d45b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d45b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d45b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d45b-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d45b-142">INPUTS</span></span>

### <span data-ttu-id="8d45b-143">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="8d45b-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="8d45b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d45b-144">OUTPUTS</span></span>

### <span data-ttu-id="8d45b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d45b-145">System.Boolean</span></span>

## <span data-ttu-id="8d45b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d45b-146">NOTES</span></span>

<span data-ttu-id="8d45b-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8d45b-147">ALIASES</span></span>

<span data-ttu-id="8d45b-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d45b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d45b-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d45b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d45b-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d45b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d45b-151">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8d45b-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d45b-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8d45b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d45b-153">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8d45b-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="8d45b-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d45b-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d45b-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8d45b-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d45b-156">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d45b-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d45b-157">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8d45b-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="8d45b-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d45b-158">RELATED LINKS</span></span>

