---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501469"
---
# <span data-ttu-id="506f8-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="506f8-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="506f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="506f8-102">SYNOPSIS</span></span>
<span data-ttu-id="506f8-103">Zatrzymuje klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="506f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="506f8-104">SYNTAX</span></span>

### <span data-ttu-id="506f8-105">Zatrzymaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="506f8-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="506f8-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="506f8-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="506f8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="506f8-107">DESCRIPTION</span></span>
<span data-ttu-id="506f8-108">Zatrzymuje klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="506f8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="506f8-109">EXAMPLES</span></span>

### <span data-ttu-id="506f8-110">Przykład 1: zatrzymywanie klastra programu Kusto</span><span class="sxs-lookup"><span data-stu-id="506f8-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="506f8-111">Powyższe polecenie zatrzymuje klaster Kusto</span><span class="sxs-lookup"><span data-stu-id="506f8-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="506f8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="506f8-112">PARAMETERS</span></span>

### <span data-ttu-id="506f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="506f8-113">-AsJob</span></span>
<span data-ttu-id="506f8-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="506f8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="506f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506f8-115">-DefaultProfile</span></span>
<span data-ttu-id="506f8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506f8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="506f8-117">-InputObject</span></span>
<span data-ttu-id="506f8-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="506f8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="506f8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="506f8-119">-Name</span></span>
<span data-ttu-id="506f8-120">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506f8-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="506f8-121">-NoWait</span></span>
<span data-ttu-id="506f8-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="506f8-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="506f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="506f8-123">-PassThru</span></span>
<span data-ttu-id="506f8-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="506f8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="506f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="506f8-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506f8-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="506f8-127">-SubscriptionId</span></span>
<span data-ttu-id="506f8-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="506f8-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="506f8-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506f8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="506f8-130">-Confirm</span></span>
<span data-ttu-id="506f8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="506f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506f8-132">-WhatIf</span></span>
<span data-ttu-id="506f8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="506f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506f8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="506f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506f8-135">CommonParameters</span></span>
<span data-ttu-id="506f8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506f8-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="506f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506f8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="506f8-138">INPUTS</span></span>

### <span data-ttu-id="506f8-139">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="506f8-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="506f8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="506f8-140">OUTPUTS</span></span>

### <span data-ttu-id="506f8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="506f8-141">System.Boolean</span></span>

## <span data-ttu-id="506f8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="506f8-142">NOTES</span></span>

<span data-ttu-id="506f8-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="506f8-143">ALIASES</span></span>

<span data-ttu-id="506f8-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="506f8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="506f8-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="506f8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="506f8-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="506f8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="506f8-147">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="506f8-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="506f8-148">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="506f8-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="506f8-149">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="506f8-150">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="506f8-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="506f8-151">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="506f8-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="506f8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="506f8-153">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="506f8-154">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="506f8-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="506f8-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="506f8-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="506f8-156">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="506f8-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="506f8-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="506f8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="506f8-158">RELATED LINKS</span></span>

