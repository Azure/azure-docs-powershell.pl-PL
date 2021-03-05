---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986805"
---
# <span data-ttu-id="cccee-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cccee-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="cccee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccee-102">SYNOPSIS</span></span>
<span data-ttu-id="cccee-103">Pobiera główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="cccee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cccee-104">SYNTAX</span></span>

### <span data-ttu-id="cccee-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cccee-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cccee-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cccee-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cccee-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cccee-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cccee-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cccee-108">DESCRIPTION</span></span>
<span data-ttu-id="cccee-109">Pobiera główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="cccee-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cccee-110">EXAMPLES</span></span>

### <span data-ttu-id="cccee-111">Przykład 1. Lista wszystkich podpisów głównych w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="cccee-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="cccee-112">Powyższe polecenie zwraca wszystkie funkcje PrincipalAssignment w bazie danych "mykustodatabase" znalezionej w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="cccee-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="cccee-113">Przykład 2. Uzyskiwanie określonego przypisania Dyrektora w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="cccee-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="cccee-114">Powyższe polecenie zwraca wszystkie funkcje PrincipalAssignment o nazwie "kustoprincipal1" w bazie danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="cccee-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="cccee-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cccee-115">PARAMETERS</span></span>

### <span data-ttu-id="cccee-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cccee-116">-ClusterName</span></span>
<span data-ttu-id="cccee-117">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cccee-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cccee-118">-DatabaseName</span></span>
<span data-ttu-id="cccee-119">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cccee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccee-120">-DefaultProfile</span></span>
<span data-ttu-id="cccee-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cccee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccee-122">-InputObject</span></span>
<span data-ttu-id="cccee-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cccee-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cccee-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cccee-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="cccee-125">Nazwa dopisu głównego( Kusto principalAssignment).</span><span class="sxs-lookup"><span data-stu-id="cccee-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccee-126">-ResourceGroupName</span></span>
<span data-ttu-id="cccee-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cccee-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cccee-128">-SubscriptionId</span></span>
<span data-ttu-id="cccee-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cccee-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cccee-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="cccee-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cccee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccee-131">CommonParameters</span></span>
<span data-ttu-id="cccee-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccee-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cccee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccee-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cccee-134">INPUTS</span></span>

### <span data-ttu-id="cccee-135">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cccee-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cccee-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cccee-136">OUTPUTS</span></span>

### <span data-ttu-id="cccee-137">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cccee-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="cccee-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cccee-138">NOTES</span></span>

<span data-ttu-id="cccee-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cccee-139">ALIASES</span></span>

<span data-ttu-id="cccee-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cccee-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cccee-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cccee-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cccee-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cccee-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cccee-143">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="cccee-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cccee-144">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cccee-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cccee-145">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cccee-146">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="cccee-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cccee-147">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cccee-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cccee-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cccee-149">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="cccee-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cccee-150">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cccee-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cccee-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cccee-152">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cccee-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cccee-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="cccee-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cccee-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cccee-154">RELATED LINKS</span></span>

