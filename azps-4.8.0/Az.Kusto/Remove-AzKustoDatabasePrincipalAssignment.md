---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062683"
---
# <span data-ttu-id="ba364-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="ba364-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="ba364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba364-102">SYNOPSIS</span></span>
<span data-ttu-id="ba364-103">Usuwa principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="ba364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba364-104">SYNTAX</span></span>

### <span data-ttu-id="ba364-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ba364-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba364-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba364-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba364-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba364-107">DESCRIPTION</span></span>
<span data-ttu-id="ba364-108">Usuwa principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="ba364-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba364-109">EXAMPLES</span></span>

### <span data-ttu-id="ba364-110">Przykład 1. Usuń istniejącą Kusto bazy danych PrincipalAssignment według nazwy</span><span class="sxs-lookup"><span data-stu-id="ba364-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="ba364-111">Powyższe polecenie usunie PrincipalAssignment o nazwie "kustoprincipal1" w bazie danych Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="ba364-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="ba364-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba364-112">PARAMETERS</span></span>

### <span data-ttu-id="ba364-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba364-113">-AsJob</span></span>
<span data-ttu-id="ba364-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ba364-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ba364-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ba364-115">-ClusterName</span></span>
<span data-ttu-id="ba364-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba364-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba364-117">-DatabaseName</span></span>
<span data-ttu-id="ba364-118">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba364-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba364-119">-DefaultProfile</span></span>
<span data-ttu-id="ba364-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba364-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba364-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba364-121">-InputObject</span></span>
<span data-ttu-id="ba364-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ba364-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba364-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ba364-123">-NoWait</span></span>
<span data-ttu-id="ba364-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ba364-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba364-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba364-125">-PassThru</span></span>
<span data-ttu-id="ba364-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ba364-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba364-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ba364-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="ba364-128">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ba364-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="ba364-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba364-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba364-130">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba364-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ba364-131">-SubscriptionId</span></span>
<span data-ttu-id="ba364-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba364-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba364-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ba364-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba364-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba364-134">-Confirm</span></span>
<span data-ttu-id="ba364-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba364-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba364-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba364-136">-WhatIf</span></span>
<span data-ttu-id="ba364-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba364-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba364-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba364-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba364-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba364-139">CommonParameters</span></span>
<span data-ttu-id="ba364-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba364-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba364-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba364-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba364-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba364-142">INPUTS</span></span>

### <span data-ttu-id="ba364-143">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ba364-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ba364-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba364-144">OUTPUTS</span></span>

### <span data-ttu-id="ba364-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba364-145">System.Boolean</span></span>

## <span data-ttu-id="ba364-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba364-146">NOTES</span></span>

<span data-ttu-id="ba364-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ba364-147">ALIASES</span></span>

<span data-ttu-id="ba364-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba364-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba364-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ba364-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba364-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba364-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba364-151">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ba364-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba364-152">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ba364-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ba364-153">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ba364-154">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ba364-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ba364-155">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ba364-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ba364-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba364-157">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ba364-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ba364-158">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ba364-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ba364-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ba364-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ba364-160">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba364-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ba364-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ba364-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba364-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba364-162">RELATED LINKS</span></span>

