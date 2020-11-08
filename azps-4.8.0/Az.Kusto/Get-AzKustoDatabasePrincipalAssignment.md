---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064051"
---
# <span data-ttu-id="fee94-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fee94-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fee94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fee94-102">SYNOPSIS</span></span>
<span data-ttu-id="fee94-103">Pobiera Kusto bazy danych klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fee94-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fee94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fee94-104">SYNTAX</span></span>

### <span data-ttu-id="fee94-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fee94-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fee94-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fee94-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fee94-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fee94-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fee94-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fee94-108">DESCRIPTION</span></span>
<span data-ttu-id="fee94-109">Pobiera Kusto bazy danych klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fee94-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fee94-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fee94-110">EXAMPLES</span></span>

### <span data-ttu-id="fee94-111">Przykład 1: wyświetlanie wszystkich PrincipalAssignment w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="fee94-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="fee94-112">Powyższe polecenie zwraca wszystkie PrincipalAssignment z bazy danych "mykustodatabase", które znajdują się w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="fee94-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="fee94-113">Przykład 2: uzyskiwanie określonego PrincipalAssignment w bazie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="fee94-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="fee94-114">Powyższe polecenie zwraca wszystkie PrincipalAssignment o nazwie "kustoprincipal1" w bazie danych "mykustodatabase", które znajdują się w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="fee94-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="fee94-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fee94-115">PARAMETERS</span></span>

### <span data-ttu-id="fee94-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="fee94-116">-ClusterName</span></span>
<span data-ttu-id="fee94-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fee94-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fee94-118">-DatabaseName</span></span>
<span data-ttu-id="fee94-119">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="fee94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee94-120">-DefaultProfile</span></span>
<span data-ttu-id="fee94-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fee94-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee94-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fee94-122">-InputObject</span></span>
<span data-ttu-id="fee94-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fee94-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fee94-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fee94-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="fee94-125">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fee94-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="fee94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee94-126">-ResourceGroupName</span></span>
<span data-ttu-id="fee94-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fee94-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fee94-128">-SubscriptionId</span></span>
<span data-ttu-id="fee94-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fee94-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fee94-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="fee94-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fee94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee94-131">CommonParameters</span></span>
<span data-ttu-id="fee94-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee94-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee94-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fee94-134">INPUTS</span></span>

### <span data-ttu-id="fee94-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fee94-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fee94-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fee94-136">OUTPUTS</span></span>

### <span data-ttu-id="fee94-137">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fee94-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fee94-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fee94-138">NOTES</span></span>

<span data-ttu-id="fee94-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="fee94-139">ALIASES</span></span>

<span data-ttu-id="fee94-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fee94-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fee94-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fee94-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fee94-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fee94-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fee94-143">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="fee94-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fee94-144">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fee94-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fee94-145">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fee94-146">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="fee94-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fee94-147">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fee94-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fee94-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fee94-149">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fee94-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fee94-150">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fee94-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fee94-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fee94-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fee94-152">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fee94-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fee94-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="fee94-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fee94-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fee94-154">RELATED LINKS</span></span>

