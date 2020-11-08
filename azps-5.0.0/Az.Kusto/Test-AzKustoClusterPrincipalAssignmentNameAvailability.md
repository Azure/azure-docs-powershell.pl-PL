---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234648"
---
# <span data-ttu-id="d96d4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d96d4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="d96d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d96d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d96d4-103">Sprawdza, czy główna nazwa zadania jest prawidłowa i nie jest już używana.</span><span class="sxs-lookup"><span data-stu-id="d96d4-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="d96d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d96d4-104">SYNTAX</span></span>

### <span data-ttu-id="d96d4-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d96d4-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d96d4-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d96d4-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d96d4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d96d4-107">DESCRIPTION</span></span>
<span data-ttu-id="d96d4-108">Sprawdza, czy główna nazwa zadania jest prawidłowa i nie jest już używana.</span><span class="sxs-lookup"><span data-stu-id="d96d4-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="d96d4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d96d4-109">EXAMPLES</span></span>

### <span data-ttu-id="d96d4-110">Przykład 1. Sprawdź dostępność nazwy principalassignment klastra, która jest w użyciu.</span><span class="sxs-lookup"><span data-stu-id="d96d4-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="d96d4-111">Powyższe polecenie zwraca informację o tym, czy w klastrze "testnewkustocluster" istnieje PrincipalAssignment o nazwie "The Principal".</span><span class="sxs-lookup"><span data-stu-id="d96d4-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d96d4-112">Przykład 2: Sprawdzanie dostępności principalassignment klastra nazwa, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="d96d4-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="d96d4-113">Powyższe polecenie zwraca informację o tym, czy w klastrze "testnewkustocluster" istnieje PrincipalAssignment o nazwie "NewPrincipal".</span><span class="sxs-lookup"><span data-stu-id="d96d4-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="d96d4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d96d4-114">PARAMETERS</span></span>

### <span data-ttu-id="d96d4-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d96d4-115">-ClusterName</span></span>
<span data-ttu-id="d96d4-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d96d4-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d96d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96d4-117">-DefaultProfile</span></span>
<span data-ttu-id="d96d4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d96d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d96d4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d96d4-119">-InputObject</span></span>
<span data-ttu-id="d96d4-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d96d4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d96d4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d96d4-121">-Name</span></span>
<span data-ttu-id="d96d4-122">Nazwa zasobu przydziału podstawowego.</span><span class="sxs-lookup"><span data-stu-id="d96d4-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="d96d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d96d4-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d96d4-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d96d4-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d96d4-125">-SubscriptionId</span></span>
<span data-ttu-id="d96d4-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d96d4-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d96d4-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d96d4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d96d4-128">-Type</span><span class="sxs-lookup"><span data-stu-id="d96d4-128">-Type</span></span>
<span data-ttu-id="d96d4-129">Typ zasobu, Microsoft. Kusto/klastrów/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="d96d4-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="d96d4-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d96d4-130">-Confirm</span></span>
<span data-ttu-id="d96d4-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d96d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96d4-132">-WhatIf</span></span>
<span data-ttu-id="d96d4-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d96d4-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d96d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d96d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96d4-135">CommonParameters</span></span>
<span data-ttu-id="d96d4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96d4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d96d4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96d4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d96d4-138">INPUTS</span></span>

### <span data-ttu-id="d96d4-139">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d96d4-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d96d4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d96d4-140">OUTPUTS</span></span>

### <span data-ttu-id="d96d4-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="d96d4-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="d96d4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d96d4-142">NOTES</span></span>

<span data-ttu-id="d96d4-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d96d4-143">ALIASES</span></span>

<span data-ttu-id="d96d4-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d96d4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d96d4-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d96d4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d96d4-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d96d4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d96d4-147">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d96d4-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d96d4-148">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d96d4-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d96d4-149">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d96d4-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d96d4-150">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d96d4-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d96d4-151">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d96d4-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d96d4-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d96d4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d96d4-153">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d96d4-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d96d4-154">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d96d4-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d96d4-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d96d4-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d96d4-156">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d96d4-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d96d4-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d96d4-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d96d4-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d96d4-158">RELATED LINKS</span></span>

