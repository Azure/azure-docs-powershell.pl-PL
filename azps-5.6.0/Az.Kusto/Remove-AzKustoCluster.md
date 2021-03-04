---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 90d080f3c45db107c3f7f86ed8c32c3efe0b066c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957089"
---
# <span data-ttu-id="ffa14-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ffa14-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="ffa14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa14-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa14-103">Usuwa klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="ffa14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ffa14-104">SYNTAX</span></span>

### <span data-ttu-id="ffa14-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="ffa14-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ffa14-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa14-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffa14-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ffa14-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa14-108">Usuwa klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="ffa14-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ffa14-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa14-110">Przykład 1. Usuwanie istniejącego klastru Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="ffa14-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="ffa14-111">Powyższe polecenie usuwa klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ffa14-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="ffa14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa14-112">PARAMETERS</span></span>

### <span data-ttu-id="ffa14-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa14-113">-AsJob</span></span>
<span data-ttu-id="ffa14-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ffa14-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ffa14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa14-115">-DefaultProfile</span></span>
<span data-ttu-id="ffa14-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa14-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa14-117">-InputObject</span></span>
<span data-ttu-id="ffa14-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ffa14-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ffa14-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ffa14-119">-Name</span></span>
<span data-ttu-id="ffa14-120">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa14-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ffa14-121">-NoWait</span></span>
<span data-ttu-id="ffa14-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ffa14-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ffa14-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffa14-123">-PassThru</span></span>
<span data-ttu-id="ffa14-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ffa14-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ffa14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa14-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffa14-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ffa14-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffa14-127">-SubscriptionId</span></span>
<span data-ttu-id="ffa14-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa14-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ffa14-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ffa14-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ffa14-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffa14-130">-Confirm</span></span>
<span data-ttu-id="ffa14-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ffa14-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa14-132">-WhatIf</span></span>
<span data-ttu-id="ffa14-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa14-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa14-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ffa14-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa14-135">CommonParameters</span></span>
<span data-ttu-id="ffa14-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa14-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffa14-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa14-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa14-138">INPUTS</span></span>

### <span data-ttu-id="ffa14-139">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa14-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ffa14-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa14-140">OUTPUTS</span></span>

### <span data-ttu-id="ffa14-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffa14-141">System.Boolean</span></span>

## <span data-ttu-id="ffa14-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ffa14-142">NOTES</span></span>

<span data-ttu-id="ffa14-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ffa14-143">ALIASES</span></span>

<span data-ttu-id="ffa14-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffa14-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ffa14-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ffa14-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ffa14-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ffa14-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ffa14-147">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ffa14-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ffa14-148">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ffa14-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ffa14-149">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ffa14-150">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ffa14-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ffa14-151">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ffa14-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ffa14-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ffa14-153">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa14-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ffa14-154">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ffa14-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ffa14-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ffa14-156">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa14-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ffa14-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ffa14-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ffa14-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffa14-158">RELATED LINKS</span></span>

