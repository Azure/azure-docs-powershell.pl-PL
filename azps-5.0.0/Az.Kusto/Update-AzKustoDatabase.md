---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232185"
---
# <span data-ttu-id="06b48-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="06b48-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="06b48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06b48-102">SYNOPSIS</span></span>
<span data-ttu-id="06b48-103">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="06b48-103">Updates a database.</span></span>

## <span data-ttu-id="06b48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06b48-104">SYNTAX</span></span>

### <span data-ttu-id="06b48-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06b48-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06b48-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="06b48-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06b48-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06b48-107">DESCRIPTION</span></span>
<span data-ttu-id="06b48-108">Aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="06b48-108">Updates a database.</span></span>

## <span data-ttu-id="06b48-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06b48-109">EXAMPLES</span></span>

### <span data-ttu-id="06b48-110">Przykład 1: aktualizowanie istniejącej bazy danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="06b48-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="06b48-111">Powyższe polecenie aktualizuje okres usuwania nietrwałego i okres pamięci podręcznej Kusto bazy danych "mykustodatabase" w klastrze "testnewkustocluster" odnaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="06b48-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="06b48-112">Przykład 2: aktualizowanie istniejącej bazy danych przy użyciu tożsamości</span><span class="sxs-lookup"><span data-stu-id="06b48-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="06b48-113">Powyższe polecenie aktualizuje okres usuwania nietrwałego i okres pamięci podręcznej Kusto bazy danych "mykustodatabase" w klastrze "testnewkustocluster" odnaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="06b48-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="06b48-114">Przykład 3: aktualizowanie istniejącej bazy danych tylko do odczytu według nazwy</span><span class="sxs-lookup"><span data-stu-id="06b48-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="06b48-115">Powyższe polecenie aktualizuje okres pamięci podręcznej bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="06b48-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="06b48-116">Przykład 4: aktualizowanie istniejącej bazy danych tylko do odczytu za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="06b48-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="06b48-117">Powyższe polecenie aktualizuje okres pamięci podręcznej bazy danych Kusto "mykustodatabase" w klastrze "myfollowercluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="06b48-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="06b48-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06b48-118">PARAMETERS</span></span>

### <span data-ttu-id="06b48-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06b48-119">-AsJob</span></span>
<span data-ttu-id="06b48-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="06b48-120">Run the command as a job</span></span>

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

### <span data-ttu-id="06b48-121">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="06b48-121">-ClusterName</span></span>
<span data-ttu-id="06b48-122">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="06b48-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b48-123">-DefaultProfile</span></span>
<span data-ttu-id="06b48-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06b48-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b48-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="06b48-125">-HotCachePeriod</span></span>
<span data-ttu-id="06b48-126">Czas przechowywania danych w pamięci podręcznej w przypadku szybkiego wykonywania kwerend w polu TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="06b48-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="06b48-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="06b48-127">-InputObject</span></span>
<span data-ttu-id="06b48-128">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="06b48-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06b48-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="06b48-129">-Kind</span></span>
<span data-ttu-id="06b48-130">Rodzaj bazy danych</span><span class="sxs-lookup"><span data-stu-id="06b48-130">Kind of the database</span></span>

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

### <span data-ttu-id="06b48-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06b48-131">-Location</span></span>
<span data-ttu-id="06b48-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="06b48-132">Resource location.</span></span>

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

### <span data-ttu-id="06b48-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06b48-133">-Name</span></span>
<span data-ttu-id="06b48-134">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="06b48-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="06b48-135">-NoWait</span></span>
<span data-ttu-id="06b48-136">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="06b48-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06b48-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b48-137">-ResourceGroupName</span></span>
<span data-ttu-id="06b48-138">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="06b48-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="06b48-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="06b48-140">Czas przechowywania danych przed zakończeniem dostępu do zapytań w polu TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="06b48-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="06b48-141">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="06b48-141">-SubscriptionId</span></span>
<span data-ttu-id="06b48-142">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06b48-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06b48-143">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="06b48-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06b48-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06b48-144">-Confirm</span></span>
<span data-ttu-id="06b48-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06b48-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b48-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b48-146">-WhatIf</span></span>
<span data-ttu-id="06b48-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06b48-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b48-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06b48-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b48-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b48-149">CommonParameters</span></span>
<span data-ttu-id="06b48-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b48-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b48-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b48-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b48-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06b48-152">INPUTS</span></span>

### <span data-ttu-id="06b48-153">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="06b48-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="06b48-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06b48-154">OUTPUTS</span></span>

### <span data-ttu-id="06b48-155">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="06b48-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="06b48-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06b48-156">NOTES</span></span>

<span data-ttu-id="06b48-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="06b48-157">ALIASES</span></span>

<span data-ttu-id="06b48-158">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06b48-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06b48-159">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="06b48-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06b48-160">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06b48-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06b48-161">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="06b48-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06b48-162">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="06b48-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="06b48-163">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="06b48-164">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="06b48-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="06b48-165">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="06b48-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="06b48-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06b48-167">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06b48-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="06b48-168">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="06b48-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="06b48-169">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="06b48-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="06b48-170">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06b48-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06b48-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="06b48-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06b48-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06b48-172">RELATED LINKS</span></span>

