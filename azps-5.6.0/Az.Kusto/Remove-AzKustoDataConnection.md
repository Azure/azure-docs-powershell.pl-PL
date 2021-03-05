---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: ac2eac129231f33a2f74732923652d3851debbd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974833"
---
# <span data-ttu-id="f07ab-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="f07ab-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="f07ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f07ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f07ab-103">Usuwa połączenie danych z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="f07ab-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="f07ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f07ab-104">SYNTAX</span></span>

### <span data-ttu-id="f07ab-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="f07ab-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f07ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f07ab-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f07ab-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f07ab-107">DESCRIPTION</span></span>
<span data-ttu-id="f07ab-108">Usuwa połączenie danych z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="f07ab-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="f07ab-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f07ab-109">EXAMPLES</span></span>

### <span data-ttu-id="f07ab-110">Przykład 1. Usuwanie istniejącego połączenia danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="f07ab-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="f07ab-111">Powyższe polecenie usuwa połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" znalezione w grupie zasobów "testrg"</span><span class="sxs-lookup"><span data-stu-id="f07ab-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="f07ab-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f07ab-112">PARAMETERS</span></span>

### <span data-ttu-id="f07ab-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f07ab-113">-AsJob</span></span>
<span data-ttu-id="f07ab-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f07ab-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f07ab-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f07ab-115">-ClusterName</span></span>
<span data-ttu-id="f07ab-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f07ab-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f07ab-117">-DatabaseName</span></span>
<span data-ttu-id="f07ab-118">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f07ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07ab-119">-DefaultProfile</span></span>
<span data-ttu-id="f07ab-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f07ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f07ab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f07ab-121">-InputObject</span></span>
<span data-ttu-id="f07ab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f07ab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f07ab-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f07ab-123">-Name</span></span>
<span data-ttu-id="f07ab-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="f07ab-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07ab-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f07ab-125">-NoWait</span></span>
<span data-ttu-id="f07ab-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f07ab-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f07ab-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f07ab-127">-PassThru</span></span>
<span data-ttu-id="f07ab-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f07ab-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f07ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="f07ab-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f07ab-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f07ab-131">-SubscriptionId</span></span>
<span data-ttu-id="f07ab-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f07ab-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f07ab-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f07ab-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f07ab-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f07ab-134">-Confirm</span></span>
<span data-ttu-id="f07ab-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f07ab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f07ab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07ab-136">-WhatIf</span></span>
<span data-ttu-id="f07ab-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f07ab-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07ab-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f07ab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f07ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07ab-139">CommonParameters</span></span>
<span data-ttu-id="f07ab-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07ab-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f07ab-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07ab-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f07ab-142">INPUTS</span></span>

### <span data-ttu-id="f07ab-143">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f07ab-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f07ab-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f07ab-144">OUTPUTS</span></span>

### <span data-ttu-id="f07ab-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f07ab-145">System.Boolean</span></span>

## <span data-ttu-id="f07ab-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f07ab-146">NOTES</span></span>

<span data-ttu-id="f07ab-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f07ab-147">ALIASES</span></span>

<span data-ttu-id="f07ab-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f07ab-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f07ab-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f07ab-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f07ab-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f07ab-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f07ab-151">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f07ab-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f07ab-152">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f07ab-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f07ab-153">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f07ab-154">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="f07ab-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f07ab-155">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f07ab-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f07ab-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f07ab-157">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f07ab-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f07ab-158">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f07ab-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f07ab-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f07ab-160">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f07ab-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f07ab-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f07ab-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f07ab-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f07ab-162">RELATED LINKS</span></span>

