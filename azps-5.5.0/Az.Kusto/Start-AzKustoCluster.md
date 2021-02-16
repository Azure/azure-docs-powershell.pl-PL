---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194259"
---
# <span data-ttu-id="7cb41-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="7cb41-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="7cb41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb41-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb41-103">Uruchamia klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="7cb41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7cb41-104">SYNTAX</span></span>

### <span data-ttu-id="7cb41-105">Start (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7cb41-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cb41-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cb41-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cb41-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7cb41-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb41-108">Uruchamia klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="7cb41-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7cb41-109">EXAMPLES</span></span>

### <span data-ttu-id="7cb41-110">Przykład 1. Uruchamianie klastrów Kusto</span><span class="sxs-lookup"><span data-stu-id="7cb41-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="7cb41-111">Powyższe polecenie uruchamia klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="7cb41-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cb41-112">PARAMETERS</span></span>

### <span data-ttu-id="7cb41-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb41-113">-AsJob</span></span>
<span data-ttu-id="7cb41-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7cb41-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7cb41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb41-115">-DefaultProfile</span></span>
<span data-ttu-id="7cb41-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb41-117">-InputObject</span></span>
<span data-ttu-id="7cb41-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7cb41-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb41-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7cb41-119">-Name</span></span>
<span data-ttu-id="7cb41-120">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb41-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cb41-121">-NoWait</span></span>
<span data-ttu-id="7cb41-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7cb41-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cb41-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cb41-123">-PassThru</span></span>
<span data-ttu-id="7cb41-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="7cb41-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7cb41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb41-125">-ResourceGroupName</span></span>
<span data-ttu-id="7cb41-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb41-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cb41-127">-SubscriptionId</span></span>
<span data-ttu-id="7cb41-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb41-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7cb41-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7cb41-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb41-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cb41-130">-Confirm</span></span>
<span data-ttu-id="7cb41-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cb41-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb41-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb41-132">-WhatIf</span></span>
<span data-ttu-id="7cb41-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cb41-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb41-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7cb41-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb41-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb41-135">CommonParameters</span></span>
<span data-ttu-id="7cb41-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb41-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb41-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cb41-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb41-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cb41-138">INPUTS</span></span>

### <span data-ttu-id="7cb41-139">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7cb41-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7cb41-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cb41-140">OUTPUTS</span></span>

### <span data-ttu-id="7cb41-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cb41-141">System.Boolean</span></span>

## <span data-ttu-id="7cb41-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7cb41-142">NOTES</span></span>

<span data-ttu-id="7cb41-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7cb41-143">ALIASES</span></span>

<span data-ttu-id="7cb41-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7cb41-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cb41-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7cb41-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cb41-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cb41-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cb41-147">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7cb41-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cb41-148">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7cb41-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7cb41-149">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7cb41-150">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="7cb41-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7cb41-151">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7cb41-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7cb41-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cb41-153">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb41-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7cb41-154">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7cb41-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7cb41-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7cb41-156">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb41-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7cb41-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7cb41-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7cb41-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cb41-158">RELATED LINKS</span></span>

