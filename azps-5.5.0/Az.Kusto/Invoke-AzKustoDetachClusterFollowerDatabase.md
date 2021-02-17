---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243338"
---
# <span data-ttu-id="831c3-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="831c3-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="831c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="831c3-102">SYNOPSIS</span></span>
<span data-ttu-id="831c3-103">Odłącza wszystkich obserwatorów bazy danych należącej do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="831c3-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="831c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="831c3-104">SYNTAX</span></span>

### <span data-ttu-id="831c3-105">DetachExpanded (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="831c3-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="831c3-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="831c3-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="831c3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="831c3-107">DESCRIPTION</span></span>
<span data-ttu-id="831c3-108">Odłącza wszystkich obserwatorów bazy danych należącej do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="831c3-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="831c3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="831c3-109">EXAMPLES</span></span>

### <span data-ttu-id="831c3-110">Przykład 1. Odłączanie bazy danych obserwowanych</span><span class="sxs-lookup"><span data-stu-id="831c3-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="831c3-111">Powyższe polecenie odłącza bazę danych obserwowaną zdefiniowaną w określonej przez attachedDatabaseConfiguration "myfo followwerconfiguration" od cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="831c3-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="831c3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="831c3-112">PARAMETERS</span></span>

### <span data-ttu-id="831c3-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="831c3-113">-AsJob</span></span>
<span data-ttu-id="831c3-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="831c3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="831c3-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="831c3-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="831c3-116">Nazwa zasobu dołączonej konfiguracji bazy danych w klastrze śledzącym.</span><span class="sxs-lookup"><span data-stu-id="831c3-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="831c3-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="831c3-117">-ClusterName</span></span>
<span data-ttu-id="831c3-118">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831c3-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="831c3-119">-ClusterResourceId</span></span>
<span data-ttu-id="831c3-120">Identyfikator zasobu klastra, który jest następujący po bazie danych należącej do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="831c3-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="831c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831c3-121">-DefaultProfile</span></span>
<span data-ttu-id="831c3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="831c3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="831c3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="831c3-123">-InputObject</span></span>
<span data-ttu-id="831c3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="831c3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="831c3-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="831c3-125">-NoWait</span></span>
<span data-ttu-id="831c3-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="831c3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="831c3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="831c3-127">-PassThru</span></span>
<span data-ttu-id="831c3-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="831c3-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="831c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="831c3-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831c3-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="831c3-131">-SubscriptionId</span></span>
<span data-ttu-id="831c3-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="831c3-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="831c3-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="831c3-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831c3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="831c3-134">-Confirm</span></span>
<span data-ttu-id="831c3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="831c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="831c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="831c3-136">-WhatIf</span></span>
<span data-ttu-id="831c3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="831c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="831c3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="831c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="831c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831c3-139">CommonParameters</span></span>
<span data-ttu-id="831c3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831c3-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="831c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831c3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="831c3-142">INPUTS</span></span>

### <span data-ttu-id="831c3-143">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="831c3-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="831c3-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="831c3-144">OUTPUTS</span></span>

### <span data-ttu-id="831c3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="831c3-145">System.Boolean</span></span>

## <span data-ttu-id="831c3-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="831c3-146">NOTES</span></span>

<span data-ttu-id="831c3-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="831c3-147">ALIASES</span></span>

<span data-ttu-id="831c3-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="831c3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="831c3-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="831c3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="831c3-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="831c3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="831c3-151">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="831c3-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="831c3-152">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="831c3-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="831c3-153">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="831c3-154">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="831c3-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="831c3-155">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="831c3-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="831c3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="831c3-157">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="831c3-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="831c3-158">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="831c3-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="831c3-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="831c3-160">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="831c3-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="831c3-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="831c3-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="831c3-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="831c3-162">RELATED LINKS</span></span>

