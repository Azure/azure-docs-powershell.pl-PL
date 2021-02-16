---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180418"
---
# <span data-ttu-id="f3f52-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f3f52-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="f3f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f52-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f52-103">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f3f52-103">Updates a database.</span></span>

## <span data-ttu-id="f3f52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3f52-104">SYNTAX</span></span>

### <span data-ttu-id="f3f52-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f3f52-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3f52-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f3f52-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3f52-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3f52-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f52-108">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f3f52-108">Updates a database.</span></span>

## <span data-ttu-id="f3f52-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3f52-109">EXAMPLES</span></span>

### <span data-ttu-id="f3f52-110">Przykład 1. Aktualizowanie istniejącej bazy danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="f3f52-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f3f52-111">Powyższe polecenie aktualizuje okres "miękkiego usunięcia" i okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "testnewkustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="f3f52-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f3f52-112">Przykład 2. Aktualizowanie istniejącej bazy danych za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="f3f52-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f3f52-113">Powyższe polecenie aktualizuje okres "miękkiego usunięcia" i okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "testnewkustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="f3f52-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f3f52-114">Przykład 3. Aktualizowanie istniejącej bazy danych ReadOnly według nazwy</span><span class="sxs-lookup"><span data-stu-id="f3f52-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f3f52-115">Powyższe polecenie aktualizuje okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="f3f52-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f3f52-116">Przykład 4. Aktualizowanie istniejącej bazy danych ReadOnly za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="f3f52-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f3f52-117">Powyższe polecenie aktualizuje okres hot cache bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="f3f52-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="f3f52-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3f52-118">PARAMETERS</span></span>

### <span data-ttu-id="f3f52-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f3f52-119">-AsJob</span></span>
<span data-ttu-id="f3f52-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f3f52-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f3f52-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f3f52-121">-ClusterName</span></span>
<span data-ttu-id="f3f52-122">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f3f52-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f52-123">-DefaultProfile</span></span>
<span data-ttu-id="f3f52-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f52-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3f52-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="f3f52-125">-HotCachePeriod</span></span>
<span data-ttu-id="f3f52-126">Czas przechowywania danych w pamięci podręcznej szybkich zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="f3f52-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="f3f52-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3f52-127">-InputObject</span></span>
<span data-ttu-id="f3f52-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f3f52-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3f52-129">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="f3f52-129">-Kind</span></span>
<span data-ttu-id="f3f52-130">Typ bazy danych</span><span class="sxs-lookup"><span data-stu-id="f3f52-130">Kind of the database</span></span>

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

### <span data-ttu-id="f3f52-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f3f52-131">-Location</span></span>
<span data-ttu-id="f3f52-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3f52-132">Resource location.</span></span>

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

### <span data-ttu-id="f3f52-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f3f52-133">-Name</span></span>
<span data-ttu-id="f3f52-134">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f3f52-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3f52-135">-NoWait</span></span>
<span data-ttu-id="f3f52-136">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f3f52-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3f52-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f52-137">-ResourceGroupName</span></span>
<span data-ttu-id="f3f52-138">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f3f52-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="f3f52-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="f3f52-140">Czas przechowywania danych, zanim przestanie być dostępny dla zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="f3f52-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="f3f52-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3f52-141">-SubscriptionId</span></span>
<span data-ttu-id="f3f52-142">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f52-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3f52-143">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f3f52-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f3f52-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3f52-144">-Confirm</span></span>
<span data-ttu-id="f3f52-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3f52-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f52-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f52-146">-WhatIf</span></span>
<span data-ttu-id="f3f52-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3f52-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f52-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f3f52-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f52-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f52-149">CommonParameters</span></span>
<span data-ttu-id="f3f52-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f52-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f52-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3f52-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f52-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3f52-152">INPUTS</span></span>

### <span data-ttu-id="f3f52-153">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f3f52-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f3f52-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3f52-154">OUTPUTS</span></span>

### <span data-ttu-id="f3f52-155">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDatabase</span><span class="sxs-lookup"><span data-stu-id="f3f52-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="f3f52-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3f52-156">NOTES</span></span>

<span data-ttu-id="f3f52-157">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f3f52-157">ALIASES</span></span>

<span data-ttu-id="f3f52-158">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f3f52-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3f52-159">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f3f52-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3f52-160">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3f52-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3f52-161">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f3f52-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3f52-162">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3f52-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f3f52-163">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f3f52-164">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="f3f52-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f3f52-165">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f3f52-166">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f3f52-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3f52-167">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f52-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f3f52-168">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f3f52-169">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f3f52-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f3f52-170">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f52-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f3f52-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f3f52-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f3f52-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3f52-172">RELATED LINKS</span></span>

