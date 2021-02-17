---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: 01f22e069e1e5d664ceac5c6cef7698cf9ffa980
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185211"
---
# <span data-ttu-id="148df-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="148df-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="148df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="148df-102">SYNOPSIS</span></span>
<span data-ttu-id="148df-103">Sprawdza, czy nazwa bazy danych jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="148df-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="148df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="148df-104">SYNTAX</span></span>

### <span data-ttu-id="148df-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="148df-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="148df-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="148df-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="148df-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="148df-107">DESCRIPTION</span></span>
<span data-ttu-id="148df-108">Sprawdza, czy nazwa bazy danych jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="148df-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="148df-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="148df-109">EXAMPLES</span></span>

### <span data-ttu-id="148df-110">Przykład 1. Sprawdzanie dostępności nazwy bazy danych Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="148df-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="148df-111">Powyższe polecenie zwraca, czy baza danych Kusto o nazwie "mykustodatabase" istnieje w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="148df-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="148df-112">Przykład 2. Sprawdzanie dostępności nazwy bazy danych Kusto, która nie jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="148df-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="148df-113">Powyższe polecenie zwraca, czy baza danych Kusto o nazwie "mykustodatabase2" istnieje w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="148df-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="148df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="148df-114">PARAMETERS</span></span>

### <span data-ttu-id="148df-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="148df-115">-ClusterName</span></span>
<span data-ttu-id="148df-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="148df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148df-117">-DefaultProfile</span></span>
<span data-ttu-id="148df-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="148df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="148df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="148df-119">-InputObject</span></span>
<span data-ttu-id="148df-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="148df-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="148df-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="148df-121">-Name</span></span>
<span data-ttu-id="148df-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="148df-122">Resource name.</span></span>

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

### <span data-ttu-id="148df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148df-123">-ResourceGroupName</span></span>
<span data-ttu-id="148df-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="148df-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="148df-125">-SubscriptionId</span></span>
<span data-ttu-id="148df-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="148df-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="148df-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="148df-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="148df-128">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="148df-128">-Type</span></span>
<span data-ttu-id="148df-129">Typ zasobu, na przykład Microsoft.Kusto/Clusters/databases.</span><span class="sxs-lookup"><span data-stu-id="148df-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="148df-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="148df-130">-Confirm</span></span>
<span data-ttu-id="148df-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="148df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148df-132">-WhatIf</span></span>
<span data-ttu-id="148df-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="148df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="148df-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="148df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148df-135">CommonParameters</span></span>
<span data-ttu-id="148df-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148df-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="148df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148df-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="148df-138">INPUTS</span></span>

### <span data-ttu-id="148df-139">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="148df-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="148df-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="148df-140">OUTPUTS</span></span>

### <span data-ttu-id="148df-141">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="148df-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="148df-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="148df-142">NOTES</span></span>

<span data-ttu-id="148df-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="148df-143">ALIASES</span></span>

<span data-ttu-id="148df-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="148df-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="148df-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="148df-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="148df-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="148df-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="148df-147">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="148df-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="148df-148">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="148df-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="148df-149">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="148df-150">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="148df-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="148df-151">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="148df-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="148df-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="148df-153">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="148df-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="148df-154">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="148df-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="148df-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="148df-156">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="148df-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="148df-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="148df-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="148df-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="148df-158">RELATED LINKS</span></span>

