---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203775"
---
# <span data-ttu-id="94678-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="94678-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="94678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94678-102">SYNOPSIS</span></span>
<span data-ttu-id="94678-103">Usuwa przypisanie główne Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="94678-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94678-104">SYNTAX</span></span>

### <span data-ttu-id="94678-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="94678-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94678-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94678-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94678-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="94678-107">DESCRIPTION</span></span>
<span data-ttu-id="94678-108">Usuwa przypisanie główne Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="94678-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94678-109">EXAMPLES</span></span>

### <span data-ttu-id="94678-110">Przykład 1. Usuwanie istniejącej bazy danych Kusto PrincipalAssignment według nazwy</span><span class="sxs-lookup"><span data-stu-id="94678-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="94678-111">Powyższe polecenie usuwa przypisanie dyrektora o nazwie "kustoprincipal1" w bazie danych Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="94678-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="94678-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94678-112">PARAMETERS</span></span>

### <span data-ttu-id="94678-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="94678-113">-AsJob</span></span>
<span data-ttu-id="94678-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="94678-114">Run the command as a job</span></span>

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

### <span data-ttu-id="94678-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94678-115">-ClusterName</span></span>
<span data-ttu-id="94678-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="94678-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94678-117">-DatabaseName</span></span>
<span data-ttu-id="94678-118">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="94678-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94678-119">-DefaultProfile</span></span>
<span data-ttu-id="94678-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94678-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94678-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94678-121">-InputObject</span></span>
<span data-ttu-id="94678-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="94678-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94678-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94678-123">-NoWait</span></span>
<span data-ttu-id="94678-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="94678-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94678-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94678-125">-PassThru</span></span>
<span data-ttu-id="94678-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94678-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94678-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="94678-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="94678-128">Nazwa dopisu głównego( Kusto principalAssignment).</span><span class="sxs-lookup"><span data-stu-id="94678-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="94678-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94678-129">-ResourceGroupName</span></span>
<span data-ttu-id="94678-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="94678-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94678-131">-SubscriptionId</span></span>
<span data-ttu-id="94678-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94678-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94678-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="94678-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94678-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94678-134">-Confirm</span></span>
<span data-ttu-id="94678-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94678-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94678-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94678-136">-WhatIf</span></span>
<span data-ttu-id="94678-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94678-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94678-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94678-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94678-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94678-139">CommonParameters</span></span>
<span data-ttu-id="94678-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94678-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94678-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94678-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94678-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94678-142">INPUTS</span></span>

### <span data-ttu-id="94678-143">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="94678-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="94678-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94678-144">OUTPUTS</span></span>

### <span data-ttu-id="94678-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94678-145">System.Boolean</span></span>

## <span data-ttu-id="94678-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94678-146">NOTES</span></span>

<span data-ttu-id="94678-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="94678-147">ALIASES</span></span>

<span data-ttu-id="94678-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="94678-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94678-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="94678-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94678-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94678-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94678-151">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="94678-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94678-152">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94678-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="94678-153">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="94678-154">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="94678-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="94678-155">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="94678-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="94678-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94678-157">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="94678-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="94678-158">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="94678-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="94678-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="94678-160">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94678-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94678-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="94678-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94678-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94678-162">RELATED LINKS</span></span>

