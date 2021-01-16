---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333985"
---
# <span data-ttu-id="5b4a9-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b4a9-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="5b4a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4a9-103">Umożliwia usunięcie dołączonej konfiguracji bazy danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="5b4a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b4a9-104">SYNTAX</span></span>

### <span data-ttu-id="5b4a9-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5b4a9-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5b4a9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b4a9-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b4a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5b4a9-107">DESCRIPTION</span></span>
<span data-ttu-id="5b4a9-108">Umożliwia usunięcie dołączonej konfiguracji bazy danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="5b4a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b4a9-109">EXAMPLES</span></span>

### <span data-ttu-id="5b4a9-110">Przykład 1. Usuń istniejące AttachedDatabaseConfiguration według nazwy</span><span class="sxs-lookup"><span data-stu-id="5b4a9-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="5b4a9-111">Powyższe polecenie usuwa bazę danych z danymi zdefiniowanymi w AttachedDatabaseConfiguration "myfollowerconfiguration" z poziomu klastra "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="5b4a9-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="5b4a9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b4a9-112">PARAMETERS</span></span>

### <span data-ttu-id="5b4a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b4a9-113">-AsJob</span></span>
<span data-ttu-id="5b4a9-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5b4a9-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="5b4a9-115">-ClusterName</span></span>
<span data-ttu-id="5b4a9-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4a9-117">-DefaultProfile</span></span>
<span data-ttu-id="5b4a9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4a9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b4a9-119">-InputObject</span></span>
<span data-ttu-id="5b4a9-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b4a9-121">-Name</span></span>
<span data-ttu-id="5b4a9-122">Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5b4a9-123">-NoWait</span></span>
<span data-ttu-id="5b4a9-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5b4a9-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b4a9-125">-PassThru</span></span>
<span data-ttu-id="5b4a9-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-126">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b4a9-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5b4a9-129">-SubscriptionId</span></span>
<span data-ttu-id="5b4a9-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b4a9-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4a9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b4a9-132">-Confirm</span></span>
<span data-ttu-id="5b4a9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4a9-134">-WhatIf</span></span>
<span data-ttu-id="5b4a9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4a9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4a9-137">CommonParameters</span></span>
<span data-ttu-id="5b4a9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4a9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b4a9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4a9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b4a9-140">INPUTS</span></span>

### <span data-ttu-id="5b4a9-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5b4a9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5b4a9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b4a9-142">OUTPUTS</span></span>

### <span data-ttu-id="5b4a9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b4a9-143">System.Boolean</span></span>

## <span data-ttu-id="5b4a9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b4a9-144">NOTES</span></span>

<span data-ttu-id="5b4a9-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5b4a9-145">ALIASES</span></span>

<span data-ttu-id="5b4a9-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b4a9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b4a9-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b4a9-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b4a9-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5b4a9-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b4a9-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5b4a9-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5b4a9-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5b4a9-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5b4a9-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5b4a9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b4a9-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5b4a9-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5b4a9-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5b4a9-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b4a9-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5b4a9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5b4a9-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b4a9-160">RELATED LINKS</span></span>

