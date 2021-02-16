---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194283"
---
# <span data-ttu-id="9baa2-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9baa2-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="9baa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9baa2-102">SYNOPSIS</span></span>
<span data-ttu-id="9baa2-103">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9baa2-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="9baa2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9baa2-104">SYNTAX</span></span>

### <span data-ttu-id="9baa2-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="9baa2-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9baa2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9baa2-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9baa2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9baa2-107">DESCRIPTION</span></span>
<span data-ttu-id="9baa2-108">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9baa2-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="9baa2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9baa2-109">EXAMPLES</span></span>

### <span data-ttu-id="9baa2-110">Przykład 1. Usuwanie istniejącej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="9baa2-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="9baa2-111">Powyższe polecenie usuwa bazę danych Kusto o nazwie "mykustodatabase" w klastrze "testnewkustocluster" znalezioną w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="9baa2-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="9baa2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9baa2-112">PARAMETERS</span></span>

### <span data-ttu-id="9baa2-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9baa2-113">-AsJob</span></span>
<span data-ttu-id="9baa2-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9baa2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9baa2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9baa2-115">-ClusterName</span></span>
<span data-ttu-id="9baa2-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9baa2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9baa2-117">-DefaultProfile</span></span>
<span data-ttu-id="9baa2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9baa2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9baa2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9baa2-119">-InputObject</span></span>
<span data-ttu-id="9baa2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9baa2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9baa2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9baa2-121">-Name</span></span>
<span data-ttu-id="9baa2-122">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9baa2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9baa2-123">-NoWait</span></span>
<span data-ttu-id="9baa2-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9baa2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9baa2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9baa2-125">-PassThru</span></span>
<span data-ttu-id="9baa2-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9baa2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9baa2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9baa2-127">-ResourceGroupName</span></span>
<span data-ttu-id="9baa2-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9baa2-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9baa2-129">-SubscriptionId</span></span>
<span data-ttu-id="9baa2-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9baa2-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9baa2-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9baa2-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9baa2-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9baa2-132">-Confirm</span></span>
<span data-ttu-id="9baa2-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9baa2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9baa2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9baa2-134">-WhatIf</span></span>
<span data-ttu-id="9baa2-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9baa2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9baa2-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9baa2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9baa2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9baa2-137">CommonParameters</span></span>
<span data-ttu-id="9baa2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9baa2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9baa2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9baa2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9baa2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9baa2-140">INPUTS</span></span>

### <span data-ttu-id="9baa2-141">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9baa2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9baa2-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9baa2-142">OUTPUTS</span></span>

### <span data-ttu-id="9baa2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9baa2-143">System.Boolean</span></span>

## <span data-ttu-id="9baa2-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9baa2-144">NOTES</span></span>

<span data-ttu-id="9baa2-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9baa2-145">ALIASES</span></span>

<span data-ttu-id="9baa2-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9baa2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9baa2-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9baa2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9baa2-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9baa2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9baa2-149">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9baa2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9baa2-150">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9baa2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9baa2-151">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9baa2-152">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="9baa2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9baa2-153">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9baa2-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9baa2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9baa2-155">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9baa2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9baa2-156">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9baa2-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9baa2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9baa2-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9baa2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9baa2-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9baa2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9baa2-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9baa2-160">RELATED LINKS</span></span>

