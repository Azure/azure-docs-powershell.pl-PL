---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490213"
---
# <span data-ttu-id="7e05f-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="7e05f-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="7e05f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e05f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e05f-103">Zwraca połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="7e05f-103">Returns a data connection.</span></span>

## <span data-ttu-id="7e05f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e05f-104">SYNTAX</span></span>

### <span data-ttu-id="7e05f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7e05f-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7e05f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7e05f-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7e05f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7e05f-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7e05f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e05f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e05f-109">Zwraca połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="7e05f-109">Returns a data connection.</span></span>

## <span data-ttu-id="7e05f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e05f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e05f-111">Przykład 1: wyświetlanie wszystkich połączeń danych w określonej bazie danych</span><span class="sxs-lookup"><span data-stu-id="7e05f-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="7e05f-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "testnewkustocluster", które znajdują się w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="7e05f-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7e05f-113">Przykład 2: uzyskiwanie określonego połączenia danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="7e05f-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="7e05f-114">Powyższe polecenie zwraca połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="7e05f-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="7e05f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e05f-115">PARAMETERS</span></span>

### <span data-ttu-id="7e05f-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7e05f-116">-ClusterName</span></span>
<span data-ttu-id="7e05f-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e05f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e05f-118">-DatabaseName</span></span>
<span data-ttu-id="7e05f-119">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e05f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e05f-120">-DefaultProfile</span></span>
<span data-ttu-id="7e05f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e05f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e05f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e05f-122">-InputObject</span></span>
<span data-ttu-id="7e05f-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7e05f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e05f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e05f-124">-Name</span></span>
<span data-ttu-id="7e05f-125">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="7e05f-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="7e05f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e05f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e05f-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e05f-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7e05f-128">-SubscriptionId</span></span>
<span data-ttu-id="7e05f-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e05f-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7e05f-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7e05f-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7e05f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e05f-131">CommonParameters</span></span>
<span data-ttu-id="7e05f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e05f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e05f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e05f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e05f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e05f-134">INPUTS</span></span>

### <span data-ttu-id="7e05f-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7e05f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7e05f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e05f-136">OUTPUTS</span></span>

### <span data-ttu-id="7e05f-137">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="7e05f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="7e05f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e05f-138">NOTES</span></span>

<span data-ttu-id="7e05f-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7e05f-139">ALIASES</span></span>

<span data-ttu-id="7e05f-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e05f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e05f-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7e05f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e05f-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e05f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e05f-143">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7e05f-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e05f-144">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7e05f-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7e05f-145">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7e05f-146">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="7e05f-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7e05f-147">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7e05f-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7e05f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e05f-149">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7e05f-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7e05f-150">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7e05f-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7e05f-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7e05f-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7e05f-152">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e05f-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7e05f-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7e05f-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7e05f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e05f-154">RELATED LINKS</span></span>

