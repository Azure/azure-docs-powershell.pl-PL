---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503467"
---
# <span data-ttu-id="48bd6-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="48bd6-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="48bd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="48bd6-103">Pobiera klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="48bd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48bd6-104">SYNTAX</span></span>

### <span data-ttu-id="48bd6-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48bd6-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48bd6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="48bd6-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48bd6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48bd6-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48bd6-108">Lista</span><span class="sxs-lookup"><span data-stu-id="48bd6-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48bd6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="48bd6-109">DESCRIPTION</span></span>
<span data-ttu-id="48bd6-110">Pobiera klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="48bd6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48bd6-111">EXAMPLES</span></span>

### <span data-ttu-id="48bd6-112">Przykład 1: wyświetlanie wszystkich klastrów Kusto w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="48bd6-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="48bd6-113">Powyższe polecenie wyświetla listę wszystkich Kustoych klastrów w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="48bd6-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="48bd6-114">Przykład 2: uzyskiwanie określonego klastra Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="48bd6-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="48bd6-115">Powyższe polecenie zwraca klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="48bd6-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="48bd6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48bd6-116">PARAMETERS</span></span>

### <span data-ttu-id="48bd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48bd6-117">-DefaultProfile</span></span>
<span data-ttu-id="48bd6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48bd6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48bd6-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48bd6-119">-InputObject</span></span>
<span data-ttu-id="48bd6-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="48bd6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48bd6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48bd6-121">-Name</span></span>
<span data-ttu-id="48bd6-122">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48bd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48bd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="48bd6-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="48bd6-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="48bd6-125">-SubscriptionId</span></span>
<span data-ttu-id="48bd6-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48bd6-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="48bd6-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="48bd6-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48bd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48bd6-128">CommonParameters</span></span>
<span data-ttu-id="48bd6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48bd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48bd6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48bd6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48bd6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48bd6-131">INPUTS</span></span>

### <span data-ttu-id="48bd6-132">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="48bd6-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="48bd6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48bd6-133">OUTPUTS</span></span>

### <span data-ttu-id="48bd6-134">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="48bd6-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="48bd6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48bd6-135">NOTES</span></span>

<span data-ttu-id="48bd6-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="48bd6-136">ALIASES</span></span>

<span data-ttu-id="48bd6-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48bd6-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48bd6-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="48bd6-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48bd6-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48bd6-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48bd6-140">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="48bd6-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48bd6-141">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="48bd6-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="48bd6-142">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="48bd6-143">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="48bd6-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="48bd6-144">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="48bd6-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="48bd6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48bd6-146">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48bd6-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="48bd6-147">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="48bd6-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="48bd6-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="48bd6-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="48bd6-149">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48bd6-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="48bd6-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="48bd6-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48bd6-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48bd6-151">RELATED LINKS</span></span>

