---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 0fbffb0effff782c154e4b6c38d6eb296b89ffb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180427"
---
# <span data-ttu-id="66359-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="66359-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="66359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66359-102">SYNOPSIS</span></span>
<span data-ttu-id="66359-103">Sprawdza, czy główna nazwa przydziału jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="66359-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="66359-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66359-104">SYNTAX</span></span>

### <span data-ttu-id="66359-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="66359-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="66359-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66359-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66359-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="66359-107">DESCRIPTION</span></span>
<span data-ttu-id="66359-108">Sprawdza, czy główna nazwa przydziału jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="66359-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="66359-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66359-109">EXAMPLES</span></span>

### <span data-ttu-id="66359-110">Przykład 1. Sprawdzanie dostępności nazwy podmiotu zabezpieczeń klastrów, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="66359-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="66359-111">Powyższe polecenie zwraca, czy w klastrze "testnewkustocluster" istnieje funkcja PrincipalAssignment o nazwie "myprincipal".</span><span class="sxs-lookup"><span data-stu-id="66359-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="66359-112">Przykład 2. Sprawdzanie dostępności nazwy podmiotu zabezpieczeń klastrów, która nie jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="66359-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="66359-113">Powyższe polecenie zwraca, czy w klastrze "testnewkustocluster" istnieje funkcja PrincipalAssignment o nazwie "newprincipal".</span><span class="sxs-lookup"><span data-stu-id="66359-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="66359-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66359-114">PARAMETERS</span></span>

### <span data-ttu-id="66359-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="66359-115">-ClusterName</span></span>
<span data-ttu-id="66359-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66359-117">-DefaultProfile</span></span>
<span data-ttu-id="66359-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66359-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66359-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66359-119">-InputObject</span></span>
<span data-ttu-id="66359-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="66359-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66359-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66359-121">-Name</span></span>
<span data-ttu-id="66359-122">Nazwa zasobu przydziału głównego.</span><span class="sxs-lookup"><span data-stu-id="66359-122">Principal Assignment resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66359-123">-ResourceGroupName</span></span>
<span data-ttu-id="66359-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66359-125">-SubscriptionId</span></span>
<span data-ttu-id="66359-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66359-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66359-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="66359-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-128">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="66359-128">-Type</span></span>
<span data-ttu-id="66359-129">Typ zasobu, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="66359-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66359-130">-Confirm</span></span>
<span data-ttu-id="66359-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="66359-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66359-132">-WhatIf</span></span>
<span data-ttu-id="66359-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66359-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66359-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="66359-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66359-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66359-135">CommonParameters</span></span>
<span data-ttu-id="66359-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66359-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66359-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66359-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66359-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66359-138">INPUTS</span></span>

### <span data-ttu-id="66359-139">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="66359-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="66359-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66359-140">OUTPUTS</span></span>

### <span data-ttu-id="66359-141">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="66359-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="66359-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66359-142">NOTES</span></span>

<span data-ttu-id="66359-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="66359-143">ALIASES</span></span>

<span data-ttu-id="66359-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="66359-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66359-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="66359-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66359-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66359-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66359-147">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="66359-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66359-148">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="66359-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="66359-149">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="66359-150">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="66359-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="66359-151">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="66359-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="66359-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66359-153">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="66359-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="66359-154">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="66359-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="66359-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="66359-156">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66359-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66359-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="66359-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="66359-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66359-158">RELATED LINKS</span></span>

