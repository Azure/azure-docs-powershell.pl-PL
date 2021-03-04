---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/stop-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d51946f9d358a7a7ccffff5e4621248d7c89fa9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953569"
---
# <span data-ttu-id="c8fc8-101">Stop-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="c8fc8-101">Stop-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="c8fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fc8-103">Zatrzymuje serwer.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-103">Stops a server.</span></span>

## <span data-ttu-id="c8fc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8fc8-104">SYNTAX</span></span>

### <span data-ttu-id="c8fc8-105">Zatrzymaj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c8fc8-105">Stop (Default)</span></span>
```
Stop-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8fc8-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8fc8-106">StopViaIdentity</span></span>
```
Stop-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8fc8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="c8fc8-108">Zatrzymuje serwer.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-108">Stops a server.</span></span>

## <span data-ttu-id="c8fc8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="c8fc8-110">Przykład 1. Zatrzymywanie serwera według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="c8fc8-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="c8fc8-111">Zatrzymywanie serwera według nazwy</span><span class="sxs-lookup"><span data-stu-id="c8fc8-111">Stop the server by name</span></span>

### <span data-ttu-id="c8fc8-112">Przykład 2. Zatrzymywanie serwera według tożsamości</span><span class="sxs-lookup"><span data-stu-id="c8fc8-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/stop"
PS C:\> Stop-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="c8fc8-113">Zatrzymywanie serwera przez tożsamość</span><span class="sxs-lookup"><span data-stu-id="c8fc8-113">Stop the server by identity</span></span>

## <span data-ttu-id="c8fc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="c8fc8-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c8fc8-115">-AsJob</span></span>
<span data-ttu-id="c8fc8-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c8fc8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c8fc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8fc8-117">-DefaultProfile</span></span>
<span data-ttu-id="c8fc8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8fc8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8fc8-119">-InputObject</span></span>
<span data-ttu-id="c8fc8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8fc8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c8fc8-121">-Name</span></span>
<span data-ttu-id="c8fc8-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fc8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c8fc8-123">-NoWait</span></span>
<span data-ttu-id="c8fc8-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c8fc8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c8fc8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8fc8-125">-PassThru</span></span>
<span data-ttu-id="c8fc8-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8fc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8fc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="c8fc8-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-128">The name of the resource group.</span></span>
<span data-ttu-id="c8fc8-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c8fc8-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8fc8-130">-SubscriptionId</span></span>
<span data-ttu-id="c8fc8-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8fc8-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8fc8-132">-Confirm</span></span>
<span data-ttu-id="c8fc8-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8fc8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8fc8-134">-WhatIf</span></span>
<span data-ttu-id="c8fc8-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8fc8-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8fc8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fc8-137">CommonParameters</span></span>
<span data-ttu-id="c8fc8-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fc8-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8fc8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fc8-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8fc8-140">INPUTS</span></span>

### <span data-ttu-id="c8fc8-141">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c8fc8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="c8fc8-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8fc8-142">OUTPUTS</span></span>

### <span data-ttu-id="c8fc8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8fc8-143">System.Boolean</span></span>

## <span data-ttu-id="c8fc8-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8fc8-144">NOTES</span></span>

<span data-ttu-id="c8fc8-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c8fc8-145">ALIASES</span></span>

<span data-ttu-id="c8fc8-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8fc8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8fc8-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8fc8-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8fc8-149">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c8fc8-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8fc8-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c8fc8-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c8fc8-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c8fc8-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c8fc8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8fc8-154">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c8fc8-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c8fc8-156">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="c8fc8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c8fc8-158">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c8fc8-159">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c8fc8-160">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8fc8-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c8fc8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8fc8-161">RELATED LINKS</span></span>

