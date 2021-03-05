---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 714f971b32f9863ab2e5dc088d07859f2f5181a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964433"
---
# <span data-ttu-id="ee1a8-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ee1a8-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="ee1a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1a8-103">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-103">Returns a database.</span></span>

## <span data-ttu-id="ee1a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee1a8-104">SYNTAX</span></span>

### <span data-ttu-id="ee1a8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ee1a8-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1a8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ee1a8-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1a8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1a8-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee1a8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee1a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ee1a8-109">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-109">Returns a database.</span></span>

## <span data-ttu-id="ee1a8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee1a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ee1a8-111">Przykład 1. Lista wszystkich baz danych kusto w klastrze według nazw</span><span class="sxs-lookup"><span data-stu-id="ee1a8-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ee1a8-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "testnewkustocluster" znalezione w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ee1a8-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ee1a8-113">Przykład 2. Uzyskiwanie konkretnej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="ee1a8-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ee1a8-114">Powyższe polecenie zwraca bazę danych Kusto o nazwie "mykustodatabase" w klastrze "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="ee1a8-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="ee1a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1a8-115">PARAMETERS</span></span>

### <span data-ttu-id="ee1a8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ee1a8-116">-ClusterName</span></span>
<span data-ttu-id="ee1a8-117">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee1a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1a8-118">-DefaultProfile</span></span>
<span data-ttu-id="ee1a8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1a8-120">-InputObject</span></span>
<span data-ttu-id="ee1a8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee1a8-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ee1a8-122">-Name</span></span>
<span data-ttu-id="ee1a8-123">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee1a8-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ee1a8-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee1a8-126">-SubscriptionId</span></span>
<span data-ttu-id="ee1a8-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee1a8-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ee1a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1a8-129">CommonParameters</span></span>
<span data-ttu-id="ee1a8-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1a8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1a8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1a8-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee1a8-132">INPUTS</span></span>

### <span data-ttu-id="ee1a8-133">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1a8-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ee1a8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee1a8-134">OUTPUTS</span></span>

### <span data-ttu-id="ee1a8-135">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDatabase</span><span class="sxs-lookup"><span data-stu-id="ee1a8-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="ee1a8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee1a8-136">NOTES</span></span>

<span data-ttu-id="ee1a8-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ee1a8-137">ALIASES</span></span>

<span data-ttu-id="ee1a8-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee1a8-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee1a8-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee1a8-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee1a8-141">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ee1a8-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee1a8-142">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ee1a8-143">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ee1a8-144">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ee1a8-145">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ee1a8-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ee1a8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee1a8-147">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ee1a8-148">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ee1a8-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ee1a8-150">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ee1a8-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ee1a8-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ee1a8-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee1a8-152">RELATED LINKS</span></span>

