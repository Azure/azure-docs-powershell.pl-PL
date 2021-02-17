---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185243"
---
# <span data-ttu-id="592d7-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="592d7-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="592d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592d7-102">SYNOPSIS</span></span>
<span data-ttu-id="592d7-103">Zwraca połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="592d7-103">Returns a data connection.</span></span>

## <span data-ttu-id="592d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="592d7-104">SYNTAX</span></span>

### <span data-ttu-id="592d7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="592d7-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="592d7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="592d7-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="592d7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="592d7-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="592d7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="592d7-108">DESCRIPTION</span></span>
<span data-ttu-id="592d7-109">Zwraca połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="592d7-109">Returns a data connection.</span></span>

## <span data-ttu-id="592d7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="592d7-110">EXAMPLES</span></span>

### <span data-ttu-id="592d7-111">Przykład 1. Lista wszystkich połączeń danych w określonej bazie danych</span><span class="sxs-lookup"><span data-stu-id="592d7-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="592d7-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "testnewkustocluster" znalezione w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="592d7-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="592d7-113">Przykład 2. Uzyskiwanie określonego połączenia danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="592d7-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="592d7-114">Powyższe polecenie zwraca połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" znalezione w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="592d7-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="592d7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="592d7-115">PARAMETERS</span></span>

### <span data-ttu-id="592d7-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="592d7-116">-ClusterName</span></span>
<span data-ttu-id="592d7-117">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="592d7-118">-DatabaseName</span></span>
<span data-ttu-id="592d7-119">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592d7-120">-DefaultProfile</span></span>
<span data-ttu-id="592d7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="592d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592d7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="592d7-122">-InputObject</span></span>
<span data-ttu-id="592d7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="592d7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="592d7-124">-Name</span></span>
<span data-ttu-id="592d7-125">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="592d7-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="592d7-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="592d7-128">-SubscriptionId</span></span>
<span data-ttu-id="592d7-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="592d7-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="592d7-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="592d7-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592d7-131">CommonParameters</span></span>
<span data-ttu-id="592d7-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592d7-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="592d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592d7-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592d7-134">INPUTS</span></span>

### <span data-ttu-id="592d7-135">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="592d7-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="592d7-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592d7-136">OUTPUTS</span></span>

### <span data-ttu-id="592d7-137">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="592d7-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="592d7-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="592d7-138">NOTES</span></span>

<span data-ttu-id="592d7-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="592d7-139">ALIASES</span></span>

<span data-ttu-id="592d7-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="592d7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="592d7-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="592d7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="592d7-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="592d7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="592d7-143">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="592d7-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="592d7-144">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="592d7-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="592d7-145">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="592d7-146">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="592d7-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="592d7-147">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="592d7-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="592d7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="592d7-149">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="592d7-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="592d7-150">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="592d7-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="592d7-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="592d7-152">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="592d7-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="592d7-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="592d7-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="592d7-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="592d7-154">RELATED LINKS</span></span>

