---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 753f2e4f2a1e2b60a12570307b518a5f2a78887b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964538"
---
# <span data-ttu-id="e5fc5-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e5fc5-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="e5fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fc5-103">Pobiera klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="e5fc5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5fc5-104">SYNTAX</span></span>

### <span data-ttu-id="e5fc5-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e5fc5-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5fc5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e5fc5-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5fc5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5fc5-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5fc5-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e5fc5-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5fc5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5fc5-109">DESCRIPTION</span></span>
<span data-ttu-id="e5fc5-110">Pobiera klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="e5fc5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5fc5-111">EXAMPLES</span></span>

### <span data-ttu-id="e5fc5-112">Przykład 1. Lista wszystkich klastrów Kusto w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e5fc5-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="e5fc5-113">Powyższe polecenie zawiera listę wszystkich klastrów Kusto w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="e5fc5-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="e5fc5-114">Przykład 2. Uzyskiwanie określonego klastru Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="e5fc5-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e5fc5-115">Powyższe polecenie zwraca klaster Kusto o nazwie "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="e5fc5-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="e5fc5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5fc5-116">PARAMETERS</span></span>

### <span data-ttu-id="e5fc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fc5-117">-DefaultProfile</span></span>
<span data-ttu-id="e5fc5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5fc5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5fc5-119">-InputObject</span></span>
<span data-ttu-id="e5fc5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5fc5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e5fc5-121">-Name</span></span>
<span data-ttu-id="e5fc5-122">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e5fc5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fc5-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5fc5-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e5fc5-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5fc5-125">-SubscriptionId</span></span>
<span data-ttu-id="e5fc5-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5fc5-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5fc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fc5-128">CommonParameters</span></span>
<span data-ttu-id="e5fc5-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fc5-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fc5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fc5-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5fc5-131">INPUTS</span></span>

### <span data-ttu-id="e5fc5-132">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e5fc5-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e5fc5-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5fc5-133">OUTPUTS</span></span>

### <span data-ttu-id="e5fc5-134">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="e5fc5-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="e5fc5-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5fc5-135">NOTES</span></span>

<span data-ttu-id="e5fc5-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e5fc5-136">ALIASES</span></span>

<span data-ttu-id="e5fc5-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5fc5-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5fc5-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5fc5-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5fc5-140">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e5fc5-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5fc5-141">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e5fc5-142">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e5fc5-143">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e5fc5-144">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e5fc5-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e5fc5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5fc5-146">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e5fc5-147">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e5fc5-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e5fc5-149">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e5fc5-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e5fc5-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e5fc5-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5fc5-151">RELATED LINKS</span></span>

