---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001258"
---
# <span data-ttu-id="2dbb9-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="2dbb9-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="2dbb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dbb9-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbb9-103">Usuwa przypisanie główne grupowania Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="2dbb9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2dbb9-104">SYNTAX</span></span>

### <span data-ttu-id="2dbb9-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="2dbb9-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dbb9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2dbb9-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2dbb9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2dbb9-107">DESCRIPTION</span></span>
<span data-ttu-id="2dbb9-108">Usuwa przypisanie główne grupowania Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="2dbb9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2dbb9-109">EXAMPLES</span></span>

### <span data-ttu-id="2dbb9-110">Przykład 1. Usuwanie istniejącego przypisania głównego grupowania Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="2dbb9-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="2dbb9-111">Powyższe polecenie usuwa przypisanie dyrektora o nazwie "kustoprincipal1" w klastrze Kusto "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="2dbb9-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="2dbb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dbb9-112">PARAMETERS</span></span>

### <span data-ttu-id="2dbb9-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2dbb9-113">-AsJob</span></span>
<span data-ttu-id="2dbb9-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2dbb9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2dbb9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2dbb9-115">-ClusterName</span></span>
<span data-ttu-id="2dbb9-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2dbb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbb9-117">-DefaultProfile</span></span>
<span data-ttu-id="2dbb9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dbb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dbb9-119">-InputObject</span></span>
<span data-ttu-id="2dbb9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbb9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2dbb9-121">-NoWait</span></span>
<span data-ttu-id="2dbb9-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2dbb9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2dbb9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dbb9-123">-PassThru</span></span>
<span data-ttu-id="2dbb9-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2dbb9-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2dbb9-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="2dbb9-126">Nazwa dopisu głównego( Kusto principalAssignment).</span><span class="sxs-lookup"><span data-stu-id="2dbb9-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="2dbb9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbb9-127">-ResourceGroupName</span></span>
<span data-ttu-id="2dbb9-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2dbb9-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dbb9-129">-SubscriptionId</span></span>
<span data-ttu-id="2dbb9-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2dbb9-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2dbb9-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dbb9-132">-Confirm</span></span>
<span data-ttu-id="2dbb9-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dbb9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dbb9-134">-WhatIf</span></span>
<span data-ttu-id="2dbb9-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dbb9-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dbb9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbb9-137">CommonParameters</span></span>
<span data-ttu-id="2dbb9-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbb9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dbb9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbb9-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dbb9-140">INPUTS</span></span>

### <span data-ttu-id="2dbb9-141">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2dbb9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2dbb9-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dbb9-142">OUTPUTS</span></span>

### <span data-ttu-id="2dbb9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2dbb9-143">System.Boolean</span></span>

## <span data-ttu-id="2dbb9-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2dbb9-144">NOTES</span></span>

<span data-ttu-id="2dbb9-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2dbb9-145">ALIASES</span></span>

<span data-ttu-id="2dbb9-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dbb9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2dbb9-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2dbb9-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2dbb9-149">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2dbb9-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2dbb9-150">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2dbb9-151">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2dbb9-152">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2dbb9-153">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2dbb9-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2dbb9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2dbb9-155">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2dbb9-156">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2dbb9-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2dbb9-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2dbb9-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="2dbb9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2dbb9-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dbb9-160">RELATED LINKS</span></span>

