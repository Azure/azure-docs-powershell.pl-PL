---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: ddc8012135ff499d46c4fd93dbfcd1fdcca5f605
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953610"
---
# <span data-ttu-id="61c4a-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="61c4a-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="61c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="61c4a-103">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-103">Restarts a server.</span></span>

## <span data-ttu-id="61c4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61c4a-104">SYNTAX</span></span>

### <span data-ttu-id="61c4a-105">Ponowne uruchamianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="61c4a-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61c4a-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61c4a-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61c4a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="61c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="61c4a-108">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-108">Restarts a server.</span></span>

## <span data-ttu-id="61c4a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="61c4a-110">Przykład 1. Ponowne uruchamianie serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="61c4a-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="61c4a-111">To polecenie cmdlet powoduje ponowne uruchomienie serwera PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="61c4a-112">Przykład 2. Ponowne uruchamianie serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="61c4a-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="61c4a-113">Te polecenia cmdlet ponownie uruchamiają serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="61c4a-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="61c4a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61c4a-114">PARAMETERS</span></span>

### <span data-ttu-id="61c4a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="61c4a-115">-AsJob</span></span>
<span data-ttu-id="61c4a-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="61c4a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="61c4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c4a-117">-DefaultProfile</span></span>
<span data-ttu-id="61c4a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61c4a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61c4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61c4a-119">-InputObject</span></span>
<span data-ttu-id="61c4a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="61c4a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61c4a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="61c4a-121">-Name</span></span>
<span data-ttu-id="61c4a-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c4a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61c4a-123">-NoWait</span></span>
<span data-ttu-id="61c4a-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="61c4a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="61c4a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61c4a-125">-PassThru</span></span>
<span data-ttu-id="61c4a-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="61c4a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="61c4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="61c4a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61c4a-128">The name of the resource group.</span></span>
<span data-ttu-id="61c4a-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="61c4a-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c4a-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61c4a-130">-SubscriptionId</span></span>
<span data-ttu-id="61c4a-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="61c4a-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c4a-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61c4a-132">-Confirm</span></span>
<span data-ttu-id="61c4a-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61c4a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c4a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c4a-134">-WhatIf</span></span>
<span data-ttu-id="61c4a-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61c4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c4a-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61c4a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c4a-137">CommonParameters</span></span>
<span data-ttu-id="61c4a-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c4a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61c4a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c4a-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61c4a-140">INPUTS</span></span>

### <span data-ttu-id="61c4a-141">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="61c4a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="61c4a-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61c4a-142">OUTPUTS</span></span>

### <span data-ttu-id="61c4a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61c4a-143">System.Boolean</span></span>

## <span data-ttu-id="61c4a-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61c4a-144">NOTES</span></span>

<span data-ttu-id="61c4a-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="61c4a-145">ALIASES</span></span>

<span data-ttu-id="61c4a-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61c4a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61c4a-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="61c4a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61c4a-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61c4a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61c4a-149">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="61c4a-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61c4a-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="61c4a-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61c4a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="61c4a-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="61c4a-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="61c4a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61c4a-154">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="61c4a-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="61c4a-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61c4a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="61c4a-156">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="61c4a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="61c4a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="61c4a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="61c4a-158">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="61c4a-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="61c4a-159">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="61c4a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="61c4a-160">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="61c4a-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="61c4a-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61c4a-161">RELATED LINKS</span></span>

