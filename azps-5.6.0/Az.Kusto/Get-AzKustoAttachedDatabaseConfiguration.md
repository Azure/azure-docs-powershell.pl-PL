---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fc4d1edfe23e6520af230960b6a9262afba43b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964561"
---
# <span data-ttu-id="bb300-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb300-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="bb300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb300-102">SYNOPSIS</span></span>
<span data-ttu-id="bb300-103">Zwraca załączoną konfigurację bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bb300-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="bb300-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb300-104">SYNTAX</span></span>

### <span data-ttu-id="bb300-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="bb300-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb300-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bb300-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb300-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb300-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb300-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb300-108">DESCRIPTION</span></span>
<span data-ttu-id="bb300-109">Zwraca załączoną konfigurację bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bb300-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="bb300-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb300-110">EXAMPLES</span></span>

### <span data-ttu-id="bb300-111">Przykład 1. Lista wszystkich pól AttachedDatabaseConfigurations w klastrze</span><span class="sxs-lookup"><span data-stu-id="bb300-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="bb300-112">Powyższe polecenie zawiera listę wszystkich konfiguracji AttachedDatabaseConfigurations w klastrze "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="bb300-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="bb300-113">Przykład 2. Uzyskiwanie konkretnej konfiguracji AttachedDatabaseConfiguration w klastrze</span><span class="sxs-lookup"><span data-stu-id="bb300-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="bb300-114">Powyższe polecenie zwraca wartość danych AttachedDatabaseConfigurations o nazwie "myfollowerconfiguration" w klastrze "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="bb300-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="bb300-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb300-115">PARAMETERS</span></span>

### <span data-ttu-id="bb300-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bb300-116">-ClusterName</span></span>
<span data-ttu-id="bb300-117">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="bb300-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb300-118">-DefaultProfile</span></span>
<span data-ttu-id="bb300-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb300-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb300-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb300-120">-InputObject</span></span>
<span data-ttu-id="bb300-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bb300-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb300-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb300-122">-Name</span></span>
<span data-ttu-id="bb300-123">Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bb300-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb300-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb300-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="bb300-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb300-126">-SubscriptionId</span></span>
<span data-ttu-id="bb300-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb300-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb300-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="bb300-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bb300-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb300-129">CommonParameters</span></span>
<span data-ttu-id="bb300-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb300-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb300-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb300-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb300-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb300-132">INPUTS</span></span>

### <span data-ttu-id="bb300-133">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bb300-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bb300-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb300-134">OUTPUTS</span></span>

### <span data-ttu-id="bb300-135">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb300-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="bb300-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb300-136">NOTES</span></span>

<span data-ttu-id="bb300-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bb300-137">ALIASES</span></span>

<span data-ttu-id="bb300-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb300-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb300-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bb300-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb300-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb300-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb300-141">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bb300-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb300-142">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bb300-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bb300-143">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bb300-144">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="bb300-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bb300-145">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bb300-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bb300-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb300-147">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bb300-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bb300-148">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bb300-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb300-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bb300-150">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb300-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bb300-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="bb300-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bb300-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb300-152">RELATED LINKS</span></span>

