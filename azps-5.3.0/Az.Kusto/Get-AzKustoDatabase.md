---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490205"
---
# <span data-ttu-id="75ce2-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="75ce2-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="75ce2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="75ce2-103">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="75ce2-103">Returns a database.</span></span>

## <span data-ttu-id="75ce2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75ce2-104">SYNTAX</span></span>

### <span data-ttu-id="75ce2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="75ce2-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75ce2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="75ce2-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75ce2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75ce2-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="75ce2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="75ce2-109">Zwraca bazę danych.</span><span class="sxs-lookup"><span data-stu-id="75ce2-109">Returns a database.</span></span>

## <span data-ttu-id="75ce2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75ce2-110">EXAMPLES</span></span>

### <span data-ttu-id="75ce2-111">Przykład 1: wyświetlanie wszystkich baz danych Kusto w klastrze według nazwy</span><span class="sxs-lookup"><span data-stu-id="75ce2-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="75ce2-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "testnewkustocluster", które znajdują się w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="75ce2-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="75ce2-113">Przykład 2: uzyskiwanie określonej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="75ce2-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="75ce2-114">Powyższe polecenie zwraca bazę danych Kusto o nazwie "mykustodatabase" w klastrze "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="75ce2-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="75ce2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75ce2-115">PARAMETERS</span></span>

### <span data-ttu-id="75ce2-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="75ce2-116">-ClusterName</span></span>
<span data-ttu-id="75ce2-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="75ce2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ce2-118">-DefaultProfile</span></span>
<span data-ttu-id="75ce2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75ce2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ce2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75ce2-120">-InputObject</span></span>
<span data-ttu-id="75ce2-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="75ce2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75ce2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75ce2-122">-Name</span></span>
<span data-ttu-id="75ce2-123">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="75ce2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ce2-124">-ResourceGroupName</span></span>
<span data-ttu-id="75ce2-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="75ce2-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="75ce2-126">-SubscriptionId</span></span>
<span data-ttu-id="75ce2-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75ce2-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75ce2-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="75ce2-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="75ce2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ce2-129">CommonParameters</span></span>
<span data-ttu-id="75ce2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ce2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ce2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75ce2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ce2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75ce2-132">INPUTS</span></span>

### <span data-ttu-id="75ce2-133">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="75ce2-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="75ce2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75ce2-134">OUTPUTS</span></span>

### <span data-ttu-id="75ce2-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDatabase</span><span class="sxs-lookup"><span data-stu-id="75ce2-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="75ce2-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75ce2-136">NOTES</span></span>

<span data-ttu-id="75ce2-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="75ce2-137">ALIASES</span></span>

<span data-ttu-id="75ce2-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75ce2-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75ce2-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="75ce2-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75ce2-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75ce2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75ce2-141">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="75ce2-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75ce2-142">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="75ce2-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="75ce2-143">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="75ce2-144">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="75ce2-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="75ce2-145">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="75ce2-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="75ce2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75ce2-147">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75ce2-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="75ce2-148">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="75ce2-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="75ce2-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="75ce2-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="75ce2-150">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75ce2-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="75ce2-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="75ce2-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="75ce2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75ce2-152">RELATED LINKS</span></span>

