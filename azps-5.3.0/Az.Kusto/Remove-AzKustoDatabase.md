---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501479"
---
# <span data-ttu-id="cdec4-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="cdec4-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="cdec4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdec4-102">SYNOPSIS</span></span>
<span data-ttu-id="cdec4-103">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="cdec4-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="cdec4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdec4-104">SYNTAX</span></span>

### <span data-ttu-id="cdec4-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cdec4-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cdec4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdec4-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cdec4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cdec4-107">DESCRIPTION</span></span>
<span data-ttu-id="cdec4-108">Usuwa bazę danych o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="cdec4-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="cdec4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdec4-109">EXAMPLES</span></span>

### <span data-ttu-id="cdec4-110">Przykład 1: usuwanie istniejącej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="cdec4-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="cdec4-111">Powyższe polecenie usunie Kusto bazę danych o nazwie "mykustodatabase" w klastrze "testnewkustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="cdec4-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="cdec4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdec4-112">PARAMETERS</span></span>

### <span data-ttu-id="cdec4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdec4-113">-AsJob</span></span>
<span data-ttu-id="cdec4-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cdec4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cdec4-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="cdec4-115">-ClusterName</span></span>
<span data-ttu-id="cdec4-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdec4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdec4-117">-DefaultProfile</span></span>
<span data-ttu-id="cdec4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdec4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdec4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cdec4-119">-InputObject</span></span>
<span data-ttu-id="cdec4-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cdec4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cdec4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdec4-121">-Name</span></span>
<span data-ttu-id="cdec4-122">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-122">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdec4-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cdec4-123">-NoWait</span></span>
<span data-ttu-id="cdec4-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cdec4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cdec4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdec4-125">-PassThru</span></span>
<span data-ttu-id="cdec4-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="cdec4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cdec4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdec4-127">-ResourceGroupName</span></span>
<span data-ttu-id="cdec4-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdec4-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cdec4-129">-SubscriptionId</span></span>
<span data-ttu-id="cdec4-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdec4-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdec4-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cdec4-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cdec4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdec4-132">-Confirm</span></span>
<span data-ttu-id="cdec4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdec4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdec4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdec4-134">-WhatIf</span></span>
<span data-ttu-id="cdec4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdec4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdec4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cdec4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdec4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdec4-137">CommonParameters</span></span>
<span data-ttu-id="cdec4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdec4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdec4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdec4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdec4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdec4-140">INPUTS</span></span>

### <span data-ttu-id="cdec4-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cdec4-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cdec4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdec4-142">OUTPUTS</span></span>

### <span data-ttu-id="cdec4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdec4-143">System.Boolean</span></span>

## <span data-ttu-id="cdec4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdec4-144">NOTES</span></span>

<span data-ttu-id="cdec4-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cdec4-145">ALIASES</span></span>

<span data-ttu-id="cdec4-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdec4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cdec4-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cdec4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdec4-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cdec4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cdec4-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cdec4-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdec4-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cdec4-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cdec4-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cdec4-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="cdec4-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cdec4-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cdec4-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cdec4-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdec4-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cdec4-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cdec4-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cdec4-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cdec4-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cdec4-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cdec4-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdec4-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cdec4-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cdec4-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cdec4-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdec4-160">RELATED LINKS</span></span>

