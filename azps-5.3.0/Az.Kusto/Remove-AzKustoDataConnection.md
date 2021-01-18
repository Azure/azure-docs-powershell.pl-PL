---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501480"
---
# <span data-ttu-id="b52e5-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="b52e5-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="b52e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b52e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b52e5-103">Umożliwia usunięcie połączenia danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="b52e5-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="b52e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b52e5-104">SYNTAX</span></span>

### <span data-ttu-id="b52e5-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b52e5-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b52e5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b52e5-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b52e5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b52e5-107">DESCRIPTION</span></span>
<span data-ttu-id="b52e5-108">Umożliwia usunięcie połączenia danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="b52e5-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="b52e5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b52e5-109">EXAMPLES</span></span>

### <span data-ttu-id="b52e5-110">Przykład 1. Usuń istniejące połączenie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="b52e5-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="b52e5-111">Powyższe polecenie usunie połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="b52e5-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="b52e5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b52e5-112">PARAMETERS</span></span>

### <span data-ttu-id="b52e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b52e5-113">-AsJob</span></span>
<span data-ttu-id="b52e5-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b52e5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b52e5-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="b52e5-115">-ClusterName</span></span>
<span data-ttu-id="b52e5-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b52e5-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b52e5-117">-DatabaseName</span></span>
<span data-ttu-id="b52e5-118">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b52e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b52e5-119">-DefaultProfile</span></span>
<span data-ttu-id="b52e5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b52e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b52e5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b52e5-121">-InputObject</span></span>
<span data-ttu-id="b52e5-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b52e5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b52e5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b52e5-123">-Name</span></span>
<span data-ttu-id="b52e5-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="b52e5-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b52e5-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b52e5-125">-NoWait</span></span>
<span data-ttu-id="b52e5-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b52e5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b52e5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b52e5-127">-PassThru</span></span>
<span data-ttu-id="b52e5-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b52e5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b52e5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b52e5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b52e5-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b52e5-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b52e5-131">-SubscriptionId</span></span>
<span data-ttu-id="b52e5-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b52e5-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b52e5-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b52e5-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b52e5-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b52e5-134">-Confirm</span></span>
<span data-ttu-id="b52e5-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b52e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52e5-136">-WhatIf</span></span>
<span data-ttu-id="b52e5-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b52e5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52e5-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b52e5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b52e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52e5-139">CommonParameters</span></span>
<span data-ttu-id="b52e5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b52e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52e5-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b52e5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52e5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b52e5-142">INPUTS</span></span>

### <span data-ttu-id="b52e5-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b52e5-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b52e5-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b52e5-144">OUTPUTS</span></span>

### <span data-ttu-id="b52e5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b52e5-145">System.Boolean</span></span>

## <span data-ttu-id="b52e5-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b52e5-146">NOTES</span></span>

<span data-ttu-id="b52e5-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b52e5-147">ALIASES</span></span>

<span data-ttu-id="b52e5-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b52e5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b52e5-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b52e5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b52e5-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b52e5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b52e5-151">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b52e5-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b52e5-152">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b52e5-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b52e5-153">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b52e5-154">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="b52e5-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b52e5-155">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b52e5-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b52e5-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b52e5-157">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b52e5-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b52e5-158">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b52e5-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b52e5-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b52e5-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b52e5-160">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b52e5-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b52e5-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b52e5-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b52e5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b52e5-162">RELATED LINKS</span></span>

