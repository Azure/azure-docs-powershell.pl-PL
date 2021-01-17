---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490197"
---
# <span data-ttu-id="c6d65-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c6d65-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c6d65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6d65-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d65-103">Pobiera Kusto bazy danych klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c6d65-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c6d65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6d65-104">SYNTAX</span></span>

### <span data-ttu-id="c6d65-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c6d65-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6d65-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c6d65-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6d65-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6d65-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6d65-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6d65-108">DESCRIPTION</span></span>
<span data-ttu-id="c6d65-109">Pobiera Kusto bazy danych klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c6d65-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c6d65-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6d65-110">EXAMPLES</span></span>

### <span data-ttu-id="c6d65-111">Przykład 1: wyświetlanie wszystkich PrincipalAssignment w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="c6d65-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c6d65-112">Powyższe polecenie zwraca wszystkie PrincipalAssignment z bazy danych "mykustodatabase", które znajdują się w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c6d65-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c6d65-113">Przykład 2: uzyskiwanie określonego PrincipalAssignment w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="c6d65-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c6d65-114">Powyższe polecenie zwraca wszystkie PrincipalAssignment o nazwie "kustoprincipal1" w bazie danych "mykustodatabase", które znajdują się w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c6d65-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c6d65-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6d65-115">PARAMETERS</span></span>

### <span data-ttu-id="c6d65-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="c6d65-116">-ClusterName</span></span>
<span data-ttu-id="c6d65-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6d65-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6d65-118">-DatabaseName</span></span>
<span data-ttu-id="c6d65-119">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6d65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d65-120">-DefaultProfile</span></span>
<span data-ttu-id="c6d65-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d65-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6d65-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6d65-122">-InputObject</span></span>
<span data-ttu-id="c6d65-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c6d65-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6d65-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c6d65-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c6d65-125">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c6d65-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c6d65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d65-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6d65-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6d65-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c6d65-128">-SubscriptionId</span></span>
<span data-ttu-id="c6d65-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d65-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6d65-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c6d65-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c6d65-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d65-131">CommonParameters</span></span>
<span data-ttu-id="c6d65-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d65-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d65-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6d65-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d65-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6d65-134">INPUTS</span></span>

### <span data-ttu-id="c6d65-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c6d65-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c6d65-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6d65-136">OUTPUTS</span></span>

### <span data-ttu-id="c6d65-137">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c6d65-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c6d65-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6d65-138">NOTES</span></span>

<span data-ttu-id="c6d65-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c6d65-139">ALIASES</span></span>

<span data-ttu-id="c6d65-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6d65-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6d65-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c6d65-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6d65-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6d65-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6d65-143">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c6d65-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6d65-144">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c6d65-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c6d65-145">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c6d65-146">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="c6d65-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c6d65-147">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c6d65-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c6d65-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6d65-149">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d65-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c6d65-150">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c6d65-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c6d65-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c6d65-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c6d65-152">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d65-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c6d65-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c6d65-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c6d65-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6d65-154">RELATED LINKS</span></span>

