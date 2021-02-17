---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185267"
---
# <span data-ttu-id="890ba-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="890ba-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="890ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="890ba-102">SYNOPSIS</span></span>
<span data-ttu-id="890ba-103">Otrzymuje przypisanie podmiotu zabezpieczeń klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="890ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="890ba-104">SYNTAX</span></span>

### <span data-ttu-id="890ba-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="890ba-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="890ba-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="890ba-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="890ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="890ba-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="890ba-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="890ba-108">DESCRIPTION</span></span>
<span data-ttu-id="890ba-109">Otrzymuje przypisanie podmiotu zabezpieczeń klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="890ba-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="890ba-110">EXAMPLES</span></span>

### <span data-ttu-id="890ba-111">Przykład 1. Lista wszystkich funkcji głównych grupowania Kusto</span><span class="sxs-lookup"><span data-stu-id="890ba-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="890ba-112">Powyższe polecenie zawiera listę wszystkich funkcji principalAssignment w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="890ba-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="890ba-113">Przykład 2. Pobiera przypisanie podmiotu głównego grupowania Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="890ba-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="890ba-114">Powyższe polecenie zwraca wartość jednostki zabezpieczeń klastrów Kusto o nazwie "kustoprincipal1" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="890ba-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="890ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="890ba-115">PARAMETERS</span></span>

### <span data-ttu-id="890ba-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="890ba-116">-ClusterName</span></span>
<span data-ttu-id="890ba-117">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="890ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890ba-118">-DefaultProfile</span></span>
<span data-ttu-id="890ba-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="890ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890ba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="890ba-120">-InputObject</span></span>
<span data-ttu-id="890ba-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="890ba-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="890ba-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="890ba-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="890ba-123">Nazwa dopisu głównego Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="890ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="890ba-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="890ba-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="890ba-126">-SubscriptionId</span></span>
<span data-ttu-id="890ba-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="890ba-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="890ba-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="890ba-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="890ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890ba-129">CommonParameters</span></span>
<span data-ttu-id="890ba-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890ba-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="890ba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890ba-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="890ba-132">INPUTS</span></span>

### <span data-ttu-id="890ba-133">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="890ba-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="890ba-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="890ba-134">OUTPUTS</span></span>

### <span data-ttu-id="890ba-135">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="890ba-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="890ba-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="890ba-136">NOTES</span></span>

<span data-ttu-id="890ba-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="890ba-137">ALIASES</span></span>

<span data-ttu-id="890ba-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="890ba-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="890ba-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="890ba-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="890ba-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="890ba-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="890ba-141">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="890ba-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="890ba-142">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="890ba-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="890ba-143">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="890ba-144">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="890ba-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="890ba-145">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="890ba-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="890ba-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="890ba-147">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="890ba-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="890ba-148">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="890ba-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="890ba-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="890ba-150">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="890ba-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="890ba-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="890ba-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="890ba-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="890ba-152">RELATED LINKS</span></span>

