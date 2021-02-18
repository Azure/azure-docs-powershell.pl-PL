---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 00ba72ba38cc73f92b0da3c7cdf2f8143a936347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202194"
---
# <span data-ttu-id="4d5b5-101">Remove-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="4d5b5-101">Remove-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="4d5b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5b5-103">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-103">Deletes a server.</span></span>

## <span data-ttu-id="4d5b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d5b5-104">SYNTAX</span></span>

### <span data-ttu-id="4d5b5-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="4d5b5-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d5b5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d5b5-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d5b5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d5b5-107">DESCRIPTION</span></span>
<span data-ttu-id="4d5b5-108">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-108">Deletes a server.</span></span>

## <span data-ttu-id="4d5b5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="4d5b5-110">Przykład 1. Usuwanie serwera PostgreSql według nazwy serwera i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d5b5-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

```

<span data-ttu-id="4d5b5-111">To polecenie cmdlet usuwa serwer PostgreSql według nazwy serwera i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="4d5b5-112">Przykład 2. Usuwanie serwera PostgreSql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="4d5b5-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Remove-AzPostgreSqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="4d5b5-113">Te polecenia cmdlet usuwają serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="4d5b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d5b5-114">PARAMETERS</span></span>

### <span data-ttu-id="4d5b5-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4d5b5-115">-AsJob</span></span>
<span data-ttu-id="4d5b5-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4d5b5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4d5b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5b5-117">-DefaultProfile</span></span>
<span data-ttu-id="4d5b5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d5b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d5b5-119">-InputObject</span></span>
<span data-ttu-id="4d5b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5b5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d5b5-121">-Name</span></span>
<span data-ttu-id="4d5b5-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d5b5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4d5b5-123">-NoWait</span></span>
<span data-ttu-id="4d5b5-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4d5b5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4d5b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d5b5-125">-PassThru</span></span>
<span data-ttu-id="4d5b5-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d5b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d5b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d5b5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-128">The name of the resource group.</span></span>
<span data-ttu-id="4d5b5-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d5b5-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d5b5-130">-SubscriptionId</span></span>
<span data-ttu-id="4d5b5-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d5b5-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d5b5-132">-Confirm</span></span>
<span data-ttu-id="4d5b5-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d5b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d5b5-134">-WhatIf</span></span>
<span data-ttu-id="4d5b5-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d5b5-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d5b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5b5-137">CommonParameters</span></span>
<span data-ttu-id="4d5b5-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5b5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d5b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5b5-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d5b5-140">INPUTS</span></span>

### <span data-ttu-id="4d5b5-141">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4d5b5-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4d5b5-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d5b5-142">OUTPUTS</span></span>

### <span data-ttu-id="4d5b5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d5b5-143">System.Boolean</span></span>

## <span data-ttu-id="4d5b5-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d5b5-144">NOTES</span></span>

<span data-ttu-id="4d5b5-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4d5b5-145">ALIASES</span></span>

<span data-ttu-id="4d5b5-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4d5b5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d5b5-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d5b5-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d5b5-149">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4d5b5-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d5b5-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4d5b5-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4d5b5-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4d5b5-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4d5b5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d5b5-154">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4d5b5-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d5b5-156">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d5b5-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4d5b5-158">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4d5b5-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d5b5-160">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4d5b5-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d5b5-161">RELATED LINKS</span></span>

