---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 76e712a881c88490a71933056f82fe1959df2948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955841"
---
# <span data-ttu-id="ec2f8-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ec2f8-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="ec2f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2f8-103">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-103">Updates a database.</span></span>

## <span data-ttu-id="ec2f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec2f8-104">SYNTAX</span></span>

### <span data-ttu-id="ec2f8-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ec2f8-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec2f8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec2f8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec2f8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec2f8-107">DESCRIPTION</span></span>
<span data-ttu-id="ec2f8-108">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-108">Updates a database.</span></span>

## <span data-ttu-id="ec2f8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec2f8-109">EXAMPLES</span></span>

### <span data-ttu-id="ec2f8-110">Przykład 1. Aktualizowanie istniejącej bazy danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="ec2f8-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ec2f8-111">Powyższe polecenie aktualizuje okres "miękkiego usunięcia" i okres pamięci podręcznej dostępu bazy danych Kusto "mykustodatabase" w klastrze "testnewkustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ec2f8-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ec2f8-112">Przykład 2. Aktualizowanie istniejącej bazy danych za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec2f8-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ec2f8-113">Powyższe polecenie aktualizuje okres "miękkiego usunięcia" i okres pamięci podręcznej dostępu bazy danych Kusto "mykustodatabase" w klastrze "testnewkustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ec2f8-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ec2f8-114">Przykład 3. Aktualizowanie istniejącej bazy danych ReadOnly według nazwy</span><span class="sxs-lookup"><span data-stu-id="ec2f8-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ec2f8-115">Powyższe polecenie aktualizuje okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ec2f8-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ec2f8-116">Przykład 4. Aktualizowanie istniejącej bazy danych ReadOnly za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec2f8-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ec2f8-117">Powyższe polecenie aktualizuje okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ec2f8-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="ec2f8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec2f8-118">PARAMETERS</span></span>

### <span data-ttu-id="ec2f8-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ec2f8-119">-AsJob</span></span>
<span data-ttu-id="ec2f8-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ec2f8-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ec2f8-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ec2f8-121">-ClusterName</span></span>
<span data-ttu-id="ec2f8-122">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2f8-123">-DefaultProfile</span></span>
<span data-ttu-id="ec2f8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec2f8-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="ec2f8-125">-HotCachePeriod</span></span>
<span data-ttu-id="ec2f8-126">Czas przechowywania danych w pamięci podręcznej szybkich zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec2f8-127">-InputObject</span></span>
<span data-ttu-id="ec2f8-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-129">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="ec2f8-129">-Kind</span></span>
<span data-ttu-id="ec2f8-130">Typ bazy danych</span><span class="sxs-lookup"><span data-stu-id="ec2f8-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ec2f8-131">-Location</span></span>
<span data-ttu-id="ec2f8-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-132">Resource location.</span></span>

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

### <span data-ttu-id="ec2f8-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec2f8-133">-Name</span></span>
<span data-ttu-id="ec2f8-134">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec2f8-135">-NoWait</span></span>
<span data-ttu-id="ec2f8-136">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ec2f8-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec2f8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec2f8-137">-ResourceGroupName</span></span>
<span data-ttu-id="ec2f8-138">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="ec2f8-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="ec2f8-140">Czas przechowywania danych, zanim przestanie być dostępny dla zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec2f8-141">-SubscriptionId</span></span>
<span data-ttu-id="ec2f8-142">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ec2f8-143">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f8-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec2f8-144">-Confirm</span></span>
<span data-ttu-id="ec2f8-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2f8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2f8-146">-WhatIf</span></span>
<span data-ttu-id="ec2f8-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec2f8-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2f8-149">CommonParameters</span></span>
<span data-ttu-id="ec2f8-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2f8-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec2f8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2f8-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec2f8-152">INPUTS</span></span>

### <span data-ttu-id="ec2f8-153">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ec2f8-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ec2f8-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec2f8-154">OUTPUTS</span></span>

### <span data-ttu-id="ec2f8-155">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDatabase</span><span class="sxs-lookup"><span data-stu-id="ec2f8-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="ec2f8-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec2f8-156">NOTES</span></span>

<span data-ttu-id="ec2f8-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ec2f8-157">ALIASES</span></span>

<span data-ttu-id="ec2f8-158">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec2f8-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec2f8-159">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec2f8-160">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec2f8-161">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec2f8-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec2f8-162">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ec2f8-163">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ec2f8-164">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ec2f8-165">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ec2f8-166">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ec2f8-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec2f8-167">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ec2f8-168">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ec2f8-169">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ec2f8-170">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ec2f8-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ec2f8-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec2f8-172">RELATED LINKS</span></span>

