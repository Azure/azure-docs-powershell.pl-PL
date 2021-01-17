---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342289"
---
# <span data-ttu-id="64ee5-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="64ee5-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="64ee5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="64ee5-103">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="64ee5-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="64ee5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64ee5-104">SYNTAX</span></span>

### <span data-ttu-id="64ee5-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="64ee5-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64ee5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64ee5-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64ee5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="64ee5-108">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="64ee5-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="64ee5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64ee5-109">EXAMPLES</span></span>

### <span data-ttu-id="64ee5-110">Przykład 1: usuwanie istniejącej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="64ee5-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="64ee5-111">Powyższe polecenie usunie Kusto bazę danych o nazwie "mykustodatabase" w klastrze "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="64ee5-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="64ee5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64ee5-112">PARAMETERS</span></span>

### <span data-ttu-id="64ee5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64ee5-113">-AsJob</span></span>
<span data-ttu-id="64ee5-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="64ee5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="64ee5-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="64ee5-115">-ClusterName</span></span>
<span data-ttu-id="64ee5-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="64ee5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ee5-117">-DefaultProfile</span></span>
<span data-ttu-id="64ee5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64ee5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ee5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64ee5-119">-InputObject</span></span>
<span data-ttu-id="64ee5-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="64ee5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64ee5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64ee5-121">-Name</span></span>
<span data-ttu-id="64ee5-122">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ee5-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="64ee5-123">-NoWait</span></span>
<span data-ttu-id="64ee5-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="64ee5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64ee5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64ee5-125">-PassThru</span></span>
<span data-ttu-id="64ee5-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="64ee5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64ee5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ee5-127">-ResourceGroupName</span></span>
<span data-ttu-id="64ee5-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="64ee5-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="64ee5-129">-SubscriptionId</span></span>
<span data-ttu-id="64ee5-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64ee5-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64ee5-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="64ee5-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64ee5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64ee5-132">-Confirm</span></span>
<span data-ttu-id="64ee5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64ee5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64ee5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64ee5-134">-WhatIf</span></span>
<span data-ttu-id="64ee5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64ee5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64ee5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64ee5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64ee5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ee5-137">CommonParameters</span></span>
<span data-ttu-id="64ee5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ee5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ee5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64ee5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ee5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64ee5-140">INPUTS</span></span>

### <span data-ttu-id="64ee5-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="64ee5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="64ee5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64ee5-142">OUTPUTS</span></span>

### <span data-ttu-id="64ee5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64ee5-143">System.Boolean</span></span>

## <span data-ttu-id="64ee5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64ee5-144">NOTES</span></span>

<span data-ttu-id="64ee5-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="64ee5-145">ALIASES</span></span>

<span data-ttu-id="64ee5-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64ee5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64ee5-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="64ee5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64ee5-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64ee5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64ee5-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="64ee5-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64ee5-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="64ee5-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="64ee5-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="64ee5-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="64ee5-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="64ee5-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="64ee5-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="64ee5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64ee5-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64ee5-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="64ee5-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="64ee5-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="64ee5-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64ee5-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="64ee5-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64ee5-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64ee5-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="64ee5-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="64ee5-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64ee5-160">RELATED LINKS</span></span>

