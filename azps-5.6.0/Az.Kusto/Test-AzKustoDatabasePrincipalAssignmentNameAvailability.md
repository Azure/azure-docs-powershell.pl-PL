---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972817"
---
# <span data-ttu-id="0c7fc-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0c7fc-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="0c7fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7fc-103">Sprawdza, czy główne przypisanie bazy danych jest prawidłowe i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="0c7fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c7fc-104">SYNTAX</span></span>

### <span data-ttu-id="0c7fc-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="0c7fc-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c7fc-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0c7fc-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c7fc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c7fc-107">DESCRIPTION</span></span>
<span data-ttu-id="0c7fc-108">Sprawdza, czy główne przypisanie bazy danych jest prawidłowe i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="0c7fc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c7fc-109">EXAMPLES</span></span>

### <span data-ttu-id="0c7fc-110">Przykład 1. Sprawdzanie dostępności nazwy podmiotu zabezpieczeń bazy danych, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="0c7fc-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="0c7fc-111">Powyższe polecenie zwraca, czy istnieje w bazie danych "mykustodatabase" jednostki PrincipalAssignment o nazwie "myprincipal" z grupy "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0c7fc-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="0c7fc-112">Przykład 2. Sprawdzanie dostępności nazwy podmiotu zabezpieczeń bazy danych, która nie jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="0c7fc-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="0c7fc-113">Powyższe polecenie zwraca, czy istnieje w bazie danych "mykustodatabase" jednostki PrincipalAssignment o nazwie "myprincipal" z grupy "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0c7fc-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="0c7fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7fc-114">PARAMETERS</span></span>

### <span data-ttu-id="0c7fc-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0c7fc-115">-ClusterName</span></span>
<span data-ttu-id="0c7fc-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c7fc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c7fc-117">-DatabaseName</span></span>
<span data-ttu-id="0c7fc-118">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c7fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7fc-119">-DefaultProfile</span></span>
<span data-ttu-id="0c7fc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c7fc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7fc-121">-InputObject</span></span>
<span data-ttu-id="0c7fc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0c7fc-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c7fc-123">-Name</span></span>
<span data-ttu-id="0c7fc-124">Nazwa zasobu przydziału głównego.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="0c7fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c7fc-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c7fc-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c7fc-127">-SubscriptionId</span></span>
<span data-ttu-id="0c7fc-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0c7fc-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0c7fc-130">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="0c7fc-130">-Type</span></span>
<span data-ttu-id="0c7fc-131">Typ zasobu, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="0c7fc-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c7fc-132">-Confirm</span></span>
<span data-ttu-id="0c7fc-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7fc-134">-WhatIf</span></span>
<span data-ttu-id="0c7fc-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7fc-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7fc-137">CommonParameters</span></span>
<span data-ttu-id="0c7fc-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7fc-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7fc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7fc-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7fc-140">INPUTS</span></span>

### <span data-ttu-id="0c7fc-141">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0c7fc-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0c7fc-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7fc-142">OUTPUTS</span></span>

### <span data-ttu-id="0c7fc-143">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="0c7fc-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="0c7fc-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c7fc-144">NOTES</span></span>

<span data-ttu-id="0c7fc-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0c7fc-145">ALIASES</span></span>

<span data-ttu-id="0c7fc-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c7fc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c7fc-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c7fc-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c7fc-149">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0c7fc-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c7fc-150">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0c7fc-151">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0c7fc-152">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0c7fc-153">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0c7fc-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0c7fc-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c7fc-155">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0c7fc-156">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0c7fc-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0c7fc-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0c7fc-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0c7fc-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0c7fc-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c7fc-160">RELATED LINKS</span></span>

