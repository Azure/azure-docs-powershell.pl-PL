---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220819"
---
# <span data-ttu-id="4ed48-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4ed48-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="4ed48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed48-103">Sprawdza, czy nazwa połączenia danych jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="4ed48-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="4ed48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ed48-104">SYNTAX</span></span>

### <span data-ttu-id="4ed48-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4ed48-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ed48-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ed48-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ed48-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4ed48-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed48-108">Sprawdza, czy nazwa połączenia danych jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="4ed48-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="4ed48-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ed48-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed48-110">Przykład 1. Sprawdź dostępność nazwy połączenia danych, która jest w użyciu.</span><span class="sxs-lookup"><span data-stu-id="4ed48-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="4ed48-111">Powyższe polecenie zwraca informację o tym, czy połączenie danych o nazwie "mykustodataconnection" istnieje w bazie danych "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="4ed48-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="4ed48-112">Przykład 2: Sprawdzanie dostępności nazwy połączenia danych, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="4ed48-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="4ed48-113">Powyższe polecenie zwraca informację o tym, czy połączenie danych o nazwie "mydataconnection" istnieje w bazie danych "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="4ed48-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="4ed48-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ed48-114">PARAMETERS</span></span>

### <span data-ttu-id="4ed48-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="4ed48-115">-ClusterName</span></span>
<span data-ttu-id="4ed48-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ed48-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ed48-117">-DatabaseName</span></span>
<span data-ttu-id="4ed48-118">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ed48-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed48-119">-DefaultProfile</span></span>
<span data-ttu-id="4ed48-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed48-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed48-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ed48-121">-InputObject</span></span>
<span data-ttu-id="4ed48-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ed48-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ed48-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ed48-123">-Name</span></span>
<span data-ttu-id="4ed48-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="4ed48-124">Data Connection name.</span></span>

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

### <span data-ttu-id="4ed48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed48-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ed48-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ed48-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4ed48-127">-SubscriptionId</span></span>
<span data-ttu-id="4ed48-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed48-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ed48-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4ed48-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ed48-130">-Type</span><span class="sxs-lookup"><span data-stu-id="4ed48-130">-Type</span></span>
<span data-ttu-id="4ed48-131">Typ zasobu, Microsoft. Kusto/klastry/połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="4ed48-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="4ed48-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ed48-132">-Confirm</span></span>
<span data-ttu-id="4ed48-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed48-134">-WhatIf</span></span>
<span data-ttu-id="4ed48-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed48-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ed48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed48-137">CommonParameters</span></span>
<span data-ttu-id="4ed48-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed48-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ed48-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed48-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ed48-140">INPUTS</span></span>

### <span data-ttu-id="4ed48-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4ed48-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4ed48-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ed48-142">OUTPUTS</span></span>

### <span data-ttu-id="4ed48-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="4ed48-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="4ed48-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ed48-144">NOTES</span></span>

<span data-ttu-id="4ed48-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4ed48-145">ALIASES</span></span>

<span data-ttu-id="4ed48-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ed48-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ed48-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4ed48-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ed48-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ed48-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ed48-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4ed48-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ed48-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4ed48-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4ed48-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4ed48-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="4ed48-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4ed48-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4ed48-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4ed48-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ed48-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed48-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4ed48-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4ed48-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4ed48-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4ed48-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4ed48-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed48-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4ed48-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4ed48-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4ed48-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ed48-160">RELATED LINKS</span></span>

