---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 14eee624f4de3129ddeefee05d402abb0cb686db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180426"
---
# <span data-ttu-id="20e0d-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="20e0d-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="20e0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="20e0d-103">Sprawdza, czy nazwa połączenia danych jest prawidłowa i nie jest jeszcze w użyciu.</span><span class="sxs-lookup"><span data-stu-id="20e0d-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="20e0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20e0d-104">SYNTAX</span></span>

### <span data-ttu-id="20e0d-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="20e0d-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20e0d-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="20e0d-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20e0d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="20e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="20e0d-108">Sprawdza, czy nazwa połączenia danych jest prawidłowa i nie jest jeszcze w użyciu.</span><span class="sxs-lookup"><span data-stu-id="20e0d-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="20e0d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20e0d-109">EXAMPLES</span></span>

### <span data-ttu-id="20e0d-110">Przykład 1. Sprawdzanie dostępności nazwy połączenia danych, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="20e0d-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="20e0d-111">Powyższe polecenie zwraca, czy w bazie danych "mykustodataconnection" istnieje połączenie danych o nazwie "mykustodataconnection".</span><span class="sxs-lookup"><span data-stu-id="20e0d-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="20e0d-112">Przykład 2. Sprawdzanie dostępności nazwy połączenia danych, która nie jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="20e0d-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="20e0d-113">Powyższe polecenie zwraca, czy w bazie danych "mykustodatabase" istnieje połączenie danych o nazwie "mydataconnection".</span><span class="sxs-lookup"><span data-stu-id="20e0d-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="20e0d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20e0d-114">PARAMETERS</span></span>

### <span data-ttu-id="20e0d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="20e0d-115">-ClusterName</span></span>
<span data-ttu-id="20e0d-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="20e0d-117">-DatabaseName</span></span>
<span data-ttu-id="20e0d-118">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e0d-119">-DefaultProfile</span></span>
<span data-ttu-id="20e0d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20e0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e0d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20e0d-121">-InputObject</span></span>
<span data-ttu-id="20e0d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="20e0d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="20e0d-123">-Name</span></span>
<span data-ttu-id="20e0d-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="20e0d-124">Data Connection name.</span></span>

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

### <span data-ttu-id="20e0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="20e0d-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20e0d-127">-SubscriptionId</span></span>
<span data-ttu-id="20e0d-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20e0d-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="20e0d-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="20e0d-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-130">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="20e0d-130">-Type</span></span>
<span data-ttu-id="20e0d-131">Typ zasobu, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="20e0d-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e0d-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20e0d-132">-Confirm</span></span>
<span data-ttu-id="20e0d-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20e0d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e0d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e0d-134">-WhatIf</span></span>
<span data-ttu-id="20e0d-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20e0d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e0d-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="20e0d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e0d-137">CommonParameters</span></span>
<span data-ttu-id="20e0d-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e0d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20e0d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e0d-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20e0d-140">INPUTS</span></span>

### <span data-ttu-id="20e0d-141">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="20e0d-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="20e0d-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20e0d-142">OUTPUTS</span></span>

### <span data-ttu-id="20e0d-143">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="20e0d-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="20e0d-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20e0d-144">NOTES</span></span>

<span data-ttu-id="20e0d-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="20e0d-145">ALIASES</span></span>

<span data-ttu-id="20e0d-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20e0d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20e0d-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="20e0d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20e0d-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20e0d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20e0d-149">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="20e0d-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20e0d-150">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="20e0d-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="20e0d-151">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="20e0d-152">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="20e0d-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="20e0d-153">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="20e0d-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="20e0d-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20e0d-155">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="20e0d-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="20e0d-156">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="20e0d-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="20e0d-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="20e0d-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20e0d-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="20e0d-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="20e0d-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="20e0d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20e0d-160">RELATED LINKS</span></span>

