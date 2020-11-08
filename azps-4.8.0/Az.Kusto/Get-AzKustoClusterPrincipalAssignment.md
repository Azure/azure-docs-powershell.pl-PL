---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064438"
---
# <span data-ttu-id="9175a-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9175a-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9175a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9175a-102">SYNOPSIS</span></span>
<span data-ttu-id="9175a-103">Pobiera principalAssignment klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9175a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9175a-104">SYNTAX</span></span>

### <span data-ttu-id="9175a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9175a-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9175a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9175a-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9175a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9175a-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9175a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9175a-108">DESCRIPTION</span></span>
<span data-ttu-id="9175a-109">Pobiera principalAssignment klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9175a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9175a-110">EXAMPLES</span></span>

### <span data-ttu-id="9175a-111">Przykład 1: Lista wszystkich Kusto klastra principalAssignment</span><span class="sxs-lookup"><span data-stu-id="9175a-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="9175a-112">Powyższe polecenie wyświetla listę wszystkich principalAssignment w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9175a-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9175a-113">Przykład 2: Pobiera Kusto klastra principalAssignment według nazwy</span><span class="sxs-lookup"><span data-stu-id="9175a-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="9175a-114">Powyższe polecenie zwraca Kusto klastra principalAssignment o nazwie "kustoprincipal1" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9175a-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9175a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9175a-115">PARAMETERS</span></span>

### <span data-ttu-id="9175a-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="9175a-116">-ClusterName</span></span>
<span data-ttu-id="9175a-117">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9175a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9175a-118">-DefaultProfile</span></span>
<span data-ttu-id="9175a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9175a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9175a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9175a-120">-InputObject</span></span>
<span data-ttu-id="9175a-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9175a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9175a-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9175a-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="9175a-123">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9175a-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="9175a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9175a-124">-ResourceGroupName</span></span>
<span data-ttu-id="9175a-125">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9175a-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9175a-126">-SubscriptionId</span></span>
<span data-ttu-id="9175a-127">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9175a-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9175a-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9175a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9175a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9175a-129">CommonParameters</span></span>
<span data-ttu-id="9175a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9175a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9175a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9175a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9175a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9175a-132">INPUTS</span></span>

### <span data-ttu-id="9175a-133">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9175a-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9175a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9175a-134">OUTPUTS</span></span>

### <span data-ttu-id="9175a-135">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9175a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9175a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9175a-136">NOTES</span></span>

<span data-ttu-id="9175a-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9175a-137">ALIASES</span></span>

<span data-ttu-id="9175a-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9175a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9175a-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9175a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9175a-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9175a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9175a-141">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9175a-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9175a-142">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9175a-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9175a-143">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9175a-144">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="9175a-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9175a-145">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9175a-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9175a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9175a-147">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9175a-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9175a-148">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9175a-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9175a-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9175a-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9175a-150">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9175a-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9175a-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9175a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9175a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9175a-152">RELATED LINKS</span></span>

