---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062685"
---
# <span data-ttu-id="d2986-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="d2986-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="d2986-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2986-102">SYNOPSIS</span></span>
<span data-ttu-id="d2986-103">Umożliwia usunięcie połączenia danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="d2986-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="d2986-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2986-104">SYNTAX</span></span>

### <span data-ttu-id="d2986-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d2986-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2986-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2986-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2986-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2986-107">DESCRIPTION</span></span>
<span data-ttu-id="d2986-108">Umożliwia usunięcie połączenia danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="d2986-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="d2986-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2986-109">EXAMPLES</span></span>

### <span data-ttu-id="d2986-110">Przykład 1. Usuń istniejące połączenie danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="d2986-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="d2986-111">Powyższe polecenie usunie połączenie danych o nazwie "mykustodataconnection" w bazie danych "mykustodatabase" istniejącego klastra "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d2986-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="d2986-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2986-112">PARAMETERS</span></span>

### <span data-ttu-id="d2986-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2986-113">-AsJob</span></span>
<span data-ttu-id="d2986-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d2986-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d2986-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d2986-115">-ClusterName</span></span>
<span data-ttu-id="d2986-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2986-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2986-117">-DatabaseName</span></span>
<span data-ttu-id="d2986-118">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2986-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2986-119">-DefaultProfile</span></span>
<span data-ttu-id="d2986-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2986-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2986-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2986-121">-InputObject</span></span>
<span data-ttu-id="d2986-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d2986-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2986-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2986-123">-Name</span></span>
<span data-ttu-id="d2986-124">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d2986-124">The name of the data connection.</span></span>

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

### <span data-ttu-id="d2986-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d2986-125">-NoWait</span></span>
<span data-ttu-id="d2986-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d2986-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2986-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2986-127">-PassThru</span></span>
<span data-ttu-id="d2986-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d2986-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2986-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2986-129">-ResourceGroupName</span></span>
<span data-ttu-id="d2986-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2986-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d2986-131">-SubscriptionId</span></span>
<span data-ttu-id="d2986-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2986-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2986-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d2986-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2986-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2986-134">-Confirm</span></span>
<span data-ttu-id="d2986-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2986-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2986-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2986-136">-WhatIf</span></span>
<span data-ttu-id="d2986-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2986-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2986-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2986-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2986-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2986-139">CommonParameters</span></span>
<span data-ttu-id="d2986-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2986-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2986-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2986-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2986-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2986-142">INPUTS</span></span>

### <span data-ttu-id="d2986-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d2986-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d2986-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2986-144">OUTPUTS</span></span>

### <span data-ttu-id="d2986-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2986-145">System.Boolean</span></span>

## <span data-ttu-id="d2986-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2986-146">NOTES</span></span>

<span data-ttu-id="d2986-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d2986-147">ALIASES</span></span>

<span data-ttu-id="d2986-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2986-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2986-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d2986-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2986-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2986-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2986-151">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d2986-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2986-152">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d2986-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d2986-153">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d2986-154">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d2986-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d2986-155">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d2986-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d2986-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2986-157">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2986-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d2986-158">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d2986-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d2986-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2986-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d2986-160">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2986-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2986-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d2986-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2986-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2986-162">RELATED LINKS</span></span>

