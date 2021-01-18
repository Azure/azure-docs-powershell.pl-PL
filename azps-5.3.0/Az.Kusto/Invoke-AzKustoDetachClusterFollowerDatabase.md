---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503349"
---
# <span data-ttu-id="e14b7-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e14b7-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="e14b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e14b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e14b7-103">Umożliwia odłączenie wszystkich obserwatorów bazy danych należącej do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="e14b7-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e14b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e14b7-104">SYNTAX</span></span>

### <span data-ttu-id="e14b7-105">DetachExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e14b7-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e14b7-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e14b7-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e14b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e14b7-107">DESCRIPTION</span></span>
<span data-ttu-id="e14b7-108">Umożliwia odłączenie wszystkich obserwatorów bazy danych należącej do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="e14b7-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e14b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e14b7-109">EXAMPLES</span></span>

### <span data-ttu-id="e14b7-110">Przykład 1. odłączanie bazy danych z danymi</span><span class="sxs-lookup"><span data-stu-id="e14b7-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="e14b7-111">Powyższe polecenie odłącza bazę danych programu zgodna ze zdefiniowaną w AttachedDatabaseConfiguration "myfollowerconfiguration" z poziomu klastra "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="e14b7-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="e14b7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e14b7-112">PARAMETERS</span></span>

### <span data-ttu-id="e14b7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e14b7-113">-AsJob</span></span>
<span data-ttu-id="e14b7-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e14b7-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e14b7-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e14b7-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="e14b7-116">Nazwa zasobu dołączonej konfiguracji bazy danych w klastrze z danymi.</span><span class="sxs-lookup"><span data-stu-id="e14b7-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="e14b7-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e14b7-117">-ClusterName</span></span>
<span data-ttu-id="e14b7-118">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="e14b7-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e14b7-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="e14b7-119">-ClusterResourceId</span></span>
<span data-ttu-id="e14b7-120">Identyfikator zasobu klastra znajdującego się za bazą danych należącymi do tego klastra.</span><span class="sxs-lookup"><span data-stu-id="e14b7-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="e14b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14b7-121">-DefaultProfile</span></span>
<span data-ttu-id="e14b7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e14b7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14b7-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e14b7-123">-InputObject</span></span>
<span data-ttu-id="e14b7-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e14b7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e14b7-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e14b7-125">-NoWait</span></span>
<span data-ttu-id="e14b7-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e14b7-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e14b7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e14b7-127">-PassThru</span></span>
<span data-ttu-id="e14b7-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e14b7-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e14b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="e14b7-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e14b7-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e14b7-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e14b7-131">-SubscriptionId</span></span>
<span data-ttu-id="e14b7-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e14b7-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e14b7-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e14b7-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e14b7-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e14b7-134">-Confirm</span></span>
<span data-ttu-id="e14b7-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14b7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14b7-136">-WhatIf</span></span>
<span data-ttu-id="e14b7-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14b7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14b7-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e14b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14b7-139">CommonParameters</span></span>
<span data-ttu-id="e14b7-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14b7-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e14b7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14b7-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e14b7-142">INPUTS</span></span>

### <span data-ttu-id="e14b7-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e14b7-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e14b7-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e14b7-144">OUTPUTS</span></span>

### <span data-ttu-id="e14b7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e14b7-145">System.Boolean</span></span>

## <span data-ttu-id="e14b7-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e14b7-146">NOTES</span></span>

<span data-ttu-id="e14b7-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e14b7-147">ALIASES</span></span>

<span data-ttu-id="e14b7-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e14b7-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e14b7-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e14b7-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e14b7-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e14b7-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e14b7-151">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e14b7-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e14b7-152">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e14b7-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e14b7-153">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="e14b7-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e14b7-154">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="e14b7-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e14b7-155">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="e14b7-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e14b7-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e14b7-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e14b7-157">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e14b7-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e14b7-158">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e14b7-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e14b7-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e14b7-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e14b7-160">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e14b7-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e14b7-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e14b7-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e14b7-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e14b7-162">RELATED LINKS</span></span>

