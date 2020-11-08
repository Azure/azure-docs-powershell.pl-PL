---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232192"
---
# <span data-ttu-id="6a9f2-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6a9f2-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="6a9f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9f2-103">Sprawdza, czy nazwa bazy danych jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="6a9f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a9f2-104">SYNTAX</span></span>

### <span data-ttu-id="6a9f2-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a9f2-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6a9f2-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a9f2-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a9f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6a9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="6a9f2-108">Sprawdza, czy nazwa bazy danych jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="6a9f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a9f2-109">EXAMPLES</span></span>

### <span data-ttu-id="6a9f2-110">Przykład 1: Sprawdzanie dostępności nazwy bazy danych Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="6a9f2-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="6a9f2-111">Powyższe polecenie zwraca informację o tym, czy w klastrze "testnewkustocluster" istnieje Kusto baza danych o nazwie "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="6a9f2-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="6a9f2-112">Przykład 2: Sprawdzanie dostępności nazwy bazy danych Kusto, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="6a9f2-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="6a9f2-113">Powyższe polecenie zwraca informację o tym, czy w klastrze "testnewkustocluster" istnieje Kusto baza danych o nazwie "mykustodatabase2".</span><span class="sxs-lookup"><span data-stu-id="6a9f2-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="6a9f2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a9f2-114">PARAMETERS</span></span>

### <span data-ttu-id="6a9f2-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6a9f2-115">-ClusterName</span></span>
<span data-ttu-id="6a9f2-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6a9f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9f2-117">-DefaultProfile</span></span>
<span data-ttu-id="6a9f2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9f2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a9f2-119">-InputObject</span></span>
<span data-ttu-id="6a9f2-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a9f2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a9f2-121">-Name</span></span>
<span data-ttu-id="6a9f2-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-122">Resource name.</span></span>

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

### <span data-ttu-id="6a9f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a9f2-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6a9f2-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a9f2-125">-SubscriptionId</span></span>
<span data-ttu-id="6a9f2-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a9f2-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a9f2-128">-Type</span><span class="sxs-lookup"><span data-stu-id="6a9f2-128">-Type</span></span>
<span data-ttu-id="6a9f2-129">Typ zasobu, na przykład Microsoft. Kusto/klastry/bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="6a9f2-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a9f2-130">-Confirm</span></span>
<span data-ttu-id="6a9f2-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a9f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a9f2-132">-WhatIf</span></span>
<span data-ttu-id="6a9f2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a9f2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a9f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9f2-135">CommonParameters</span></span>
<span data-ttu-id="6a9f2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9f2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a9f2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9f2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a9f2-138">INPUTS</span></span>

### <span data-ttu-id="6a9f2-139">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6a9f2-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6a9f2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a9f2-140">OUTPUTS</span></span>

### <span data-ttu-id="6a9f2-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="6a9f2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="6a9f2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a9f2-142">NOTES</span></span>

<span data-ttu-id="6a9f2-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6a9f2-143">ALIASES</span></span>

<span data-ttu-id="6a9f2-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a9f2-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a9f2-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a9f2-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a9f2-147">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6a9f2-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a9f2-148">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6a9f2-149">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6a9f2-150">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6a9f2-151">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6a9f2-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6a9f2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a9f2-153">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6a9f2-154">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6a9f2-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6a9f2-156">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a9f2-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6a9f2-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6a9f2-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a9f2-158">RELATED LINKS</span></span>

