---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338725"
---
# <span data-ttu-id="18c75-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="18c75-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="18c75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18c75-102">SYNOPSIS</span></span>
<span data-ttu-id="18c75-103">Usuwa principalAssignment klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="18c75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18c75-104">SYNTAX</span></span>

### <span data-ttu-id="18c75-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="18c75-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18c75-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18c75-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18c75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18c75-107">DESCRIPTION</span></span>
<span data-ttu-id="18c75-108">Usuwa principalAssignment klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="18c75-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18c75-109">EXAMPLES</span></span>

### <span data-ttu-id="18c75-110">Przykład 1: Usuwanie istniejącego PrincipalAssignment klastra Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="18c75-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="18c75-111">Powyższe polecenie usuwa PrincipalAssignment o nazwie "kustoprincipal1" w Kusto klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="18c75-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="18c75-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18c75-112">PARAMETERS</span></span>

### <span data-ttu-id="18c75-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18c75-113">-AsJob</span></span>
<span data-ttu-id="18c75-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="18c75-114">Run the command as a job</span></span>

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

### <span data-ttu-id="18c75-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="18c75-115">-ClusterName</span></span>
<span data-ttu-id="18c75-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="18c75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c75-117">-DefaultProfile</span></span>
<span data-ttu-id="18c75-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18c75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c75-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="18c75-119">-InputObject</span></span>
<span data-ttu-id="18c75-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="18c75-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18c75-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="18c75-121">-NoWait</span></span>
<span data-ttu-id="18c75-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="18c75-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18c75-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18c75-123">-PassThru</span></span>
<span data-ttu-id="18c75-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="18c75-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="18c75-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="18c75-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="18c75-126">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="18c75-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="18c75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c75-127">-ResourceGroupName</span></span>
<span data-ttu-id="18c75-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="18c75-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="18c75-129">-SubscriptionId</span></span>
<span data-ttu-id="18c75-130">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18c75-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18c75-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="18c75-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18c75-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18c75-132">-Confirm</span></span>
<span data-ttu-id="18c75-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c75-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c75-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c75-134">-WhatIf</span></span>
<span data-ttu-id="18c75-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c75-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c75-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18c75-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c75-137">CommonParameters</span></span>
<span data-ttu-id="18c75-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c75-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18c75-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c75-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18c75-140">INPUTS</span></span>

### <span data-ttu-id="18c75-141">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="18c75-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="18c75-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18c75-142">OUTPUTS</span></span>

### <span data-ttu-id="18c75-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18c75-143">System.Boolean</span></span>

## <span data-ttu-id="18c75-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18c75-144">NOTES</span></span>

<span data-ttu-id="18c75-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="18c75-145">ALIASES</span></span>

<span data-ttu-id="18c75-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18c75-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18c75-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="18c75-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18c75-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18c75-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18c75-149">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="18c75-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18c75-150">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="18c75-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="18c75-151">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="18c75-152">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="18c75-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="18c75-153">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="18c75-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="18c75-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18c75-155">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18c75-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="18c75-156">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="18c75-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="18c75-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="18c75-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="18c75-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18c75-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18c75-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="18c75-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18c75-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18c75-160">RELATED LINKS</span></span>

