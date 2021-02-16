---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194290"
---
# <span data-ttu-id="11ceb-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="11ceb-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="11ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="11ceb-103">Usuwa połączenie danych z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="11ceb-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="11ceb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11ceb-104">SYNTAX</span></span>

### <span data-ttu-id="11ceb-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="11ceb-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11ceb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11ceb-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11ceb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="11ceb-107">DESCRIPTION</span></span>
<span data-ttu-id="11ceb-108">Usuwa połączenie danych z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="11ceb-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="11ceb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11ceb-109">EXAMPLES</span></span>

### <span data-ttu-id="11ceb-110">Przykład 1. Usuwanie istniejącego połączenia danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="11ceb-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="11ceb-111">Powyższe polecenie usuwa połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" znalezione w grupie zasobów "testrg"</span><span class="sxs-lookup"><span data-stu-id="11ceb-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="11ceb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11ceb-112">PARAMETERS</span></span>

### <span data-ttu-id="11ceb-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11ceb-113">-AsJob</span></span>
<span data-ttu-id="11ceb-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="11ceb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="11ceb-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11ceb-115">-ClusterName</span></span>
<span data-ttu-id="11ceb-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="11ceb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11ceb-117">-DatabaseName</span></span>
<span data-ttu-id="11ceb-118">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="11ceb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ceb-119">-DefaultProfile</span></span>
<span data-ttu-id="11ceb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11ceb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ceb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ceb-121">-InputObject</span></span>
<span data-ttu-id="11ceb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="11ceb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11ceb-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11ceb-123">-Name</span></span>
<span data-ttu-id="11ceb-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="11ceb-124">The name of the data connection.</span></span>

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

### <span data-ttu-id="11ceb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11ceb-125">-NoWait</span></span>
<span data-ttu-id="11ceb-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="11ceb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11ceb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11ceb-127">-PassThru</span></span>
<span data-ttu-id="11ceb-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="11ceb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="11ceb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ceb-129">-ResourceGroupName</span></span>
<span data-ttu-id="11ceb-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="11ceb-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11ceb-131">-SubscriptionId</span></span>
<span data-ttu-id="11ceb-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11ceb-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11ceb-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="11ceb-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11ceb-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11ceb-134">-Confirm</span></span>
<span data-ttu-id="11ceb-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11ceb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ceb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ceb-136">-WhatIf</span></span>
<span data-ttu-id="11ceb-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ceb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ceb-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11ceb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ceb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ceb-139">CommonParameters</span></span>
<span data-ttu-id="11ceb-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ceb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ceb-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11ceb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ceb-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ceb-142">INPUTS</span></span>

### <span data-ttu-id="11ceb-143">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="11ceb-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="11ceb-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ceb-144">OUTPUTS</span></span>

### <span data-ttu-id="11ceb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11ceb-145">System.Boolean</span></span>

## <span data-ttu-id="11ceb-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11ceb-146">NOTES</span></span>

<span data-ttu-id="11ceb-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="11ceb-147">ALIASES</span></span>

<span data-ttu-id="11ceb-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="11ceb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11ceb-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="11ceb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11ceb-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11ceb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11ceb-151">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="11ceb-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11ceb-152">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="11ceb-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="11ceb-153">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="11ceb-154">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="11ceb-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="11ceb-155">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="11ceb-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="11ceb-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11ceb-157">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="11ceb-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="11ceb-158">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="11ceb-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="11ceb-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="11ceb-160">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11ceb-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="11ceb-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="11ceb-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11ceb-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ceb-162">RELATED LINKS</span></span>

