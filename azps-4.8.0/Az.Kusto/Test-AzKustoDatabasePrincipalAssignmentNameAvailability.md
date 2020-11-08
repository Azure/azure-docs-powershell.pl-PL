---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220653"
---
# <span data-ttu-id="d6ae2-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d6ae2-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="d6ae2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ae2-103">Sprawdza, czy przypisanie główne bazy danych jest prawidłowe i nie jest już używane.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="d6ae2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6ae2-104">SYNTAX</span></span>

### <span data-ttu-id="d6ae2-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6ae2-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6ae2-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d6ae2-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6ae2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ae2-108">Sprawdza, czy przypisanie główne bazy danych jest prawidłowe i nie jest już używane.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="d6ae2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ae2-110">Przykład 1: Sprawdzanie dostępności nazwy principalassignment bazy danych, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="d6ae2-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="d6ae2-111">Powyższe polecenie zwraca informację o tym, czy PrincipalAssignment o nazwie "Moja Principal" istnieje w bazie danych "mykustodatabase" z poziomu klastra "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d6ae2-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d6ae2-112">Przykład 2: Sprawdzanie dostępności bazy danych principalassignment nazwa, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="d6ae2-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="d6ae2-113">Powyższe polecenie zwraca informację o tym, czy PrincipalAssignment o nazwie "Moja Principal" istnieje w bazie danych "mykustodatabase" z poziomu klastra "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d6ae2-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="d6ae2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6ae2-114">PARAMETERS</span></span>

### <span data-ttu-id="d6ae2-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d6ae2-115">-ClusterName</span></span>
<span data-ttu-id="d6ae2-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d6ae2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6ae2-117">-DatabaseName</span></span>
<span data-ttu-id="d6ae2-118">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d6ae2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ae2-119">-DefaultProfile</span></span>
<span data-ttu-id="d6ae2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ae2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d6ae2-121">-InputObject</span></span>
<span data-ttu-id="d6ae2-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6ae2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6ae2-123">-Name</span></span>
<span data-ttu-id="d6ae2-124">Nazwa zasobu przydziału podstawowego.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="d6ae2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ae2-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6ae2-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d6ae2-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d6ae2-127">-SubscriptionId</span></span>
<span data-ttu-id="d6ae2-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6ae2-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6ae2-130">-Type</span><span class="sxs-lookup"><span data-stu-id="d6ae2-130">-Type</span></span>
<span data-ttu-id="d6ae2-131">Typ zasobu, Microsoft. Kusto/klaster/bazy danych/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="d6ae2-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6ae2-132">-Confirm</span></span>
<span data-ttu-id="d6ae2-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ae2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ae2-134">-WhatIf</span></span>
<span data-ttu-id="d6ae2-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ae2-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ae2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ae2-137">CommonParameters</span></span>
<span data-ttu-id="d6ae2-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ae2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6ae2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ae2-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ae2-140">INPUTS</span></span>

### <span data-ttu-id="d6ae2-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d6ae2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d6ae2-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6ae2-142">OUTPUTS</span></span>

### <span data-ttu-id="d6ae2-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="d6ae2-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="d6ae2-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6ae2-144">NOTES</span></span>

<span data-ttu-id="d6ae2-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d6ae2-145">ALIASES</span></span>

<span data-ttu-id="d6ae2-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6ae2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6ae2-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6ae2-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6ae2-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d6ae2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6ae2-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d6ae2-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d6ae2-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d6ae2-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d6ae2-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d6ae2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6ae2-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d6ae2-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d6ae2-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d6ae2-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d6ae2-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d6ae2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6ae2-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6ae2-160">RELATED LINKS</span></span>

