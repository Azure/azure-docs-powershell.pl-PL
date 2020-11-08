---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233483"
---
# <span data-ttu-id="d43ce-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d43ce-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="d43ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d43ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d43ce-103">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="d43ce-103">Returns a database.</span></span>

## <span data-ttu-id="d43ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d43ce-104">SYNTAX</span></span>

### <span data-ttu-id="d43ce-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d43ce-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d43ce-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d43ce-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d43ce-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d43ce-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d43ce-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d43ce-108">DESCRIPTION</span></span>
<span data-ttu-id="d43ce-109">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="d43ce-109">Returns a database.</span></span>

## <span data-ttu-id="d43ce-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d43ce-110">EXAMPLES</span></span>

### <span data-ttu-id="d43ce-111">Przykład 1: wyświetlanie wszystkich baz danych Kusto w klastrze według nazwy</span><span class="sxs-lookup"><span data-stu-id="d43ce-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d43ce-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "testnewkustocluster", które znajdują się w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d43ce-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d43ce-113">Przykład 2: uzyskiwanie określonej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="d43ce-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d43ce-114">Powyższe polecenie zwraca bazę danych Kusto o nazwie "mykustodatabase" w klastrze "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d43ce-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="d43ce-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d43ce-115">PARAMETERS</span></span>

### <span data-ttu-id="d43ce-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d43ce-116">-ClusterName</span></span>
<span data-ttu-id="d43ce-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d43ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43ce-118">-DefaultProfile</span></span>
<span data-ttu-id="d43ce-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d43ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43ce-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d43ce-120">-InputObject</span></span>
<span data-ttu-id="d43ce-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d43ce-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d43ce-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d43ce-122">-Name</span></span>
<span data-ttu-id="d43ce-123">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d43ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="d43ce-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d43ce-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d43ce-126">-SubscriptionId</span></span>
<span data-ttu-id="d43ce-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d43ce-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d43ce-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d43ce-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d43ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43ce-129">CommonParameters</span></span>
<span data-ttu-id="d43ce-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43ce-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d43ce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43ce-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d43ce-132">INPUTS</span></span>

### <span data-ttu-id="d43ce-133">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d43ce-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d43ce-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d43ce-134">OUTPUTS</span></span>

### <span data-ttu-id="d43ce-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="d43ce-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="d43ce-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d43ce-136">NOTES</span></span>

<span data-ttu-id="d43ce-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d43ce-137">ALIASES</span></span>

<span data-ttu-id="d43ce-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d43ce-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d43ce-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d43ce-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d43ce-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d43ce-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d43ce-141">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d43ce-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d43ce-142">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d43ce-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d43ce-143">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d43ce-144">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d43ce-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d43ce-145">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d43ce-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d43ce-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d43ce-147">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d43ce-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d43ce-148">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d43ce-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d43ce-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d43ce-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d43ce-150">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d43ce-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d43ce-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d43ce-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d43ce-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d43ce-152">RELATED LINKS</span></span>

