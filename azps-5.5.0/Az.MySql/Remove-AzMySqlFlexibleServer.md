---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
ms.openlocfilehash: 8e16ee1ad3a8d8b695a433af8c9194ad460c3138
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180043"
---
# <span data-ttu-id="efef2-101">Remove-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="efef2-101">Remove-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="efef2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efef2-102">SYNOPSIS</span></span>
<span data-ttu-id="efef2-103">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="efef2-103">Deletes a server.</span></span>

## <span data-ttu-id="efef2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efef2-104">SYNTAX</span></span>

### <span data-ttu-id="efef2-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="efef2-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efef2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="efef2-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efef2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="efef2-107">DESCRIPTION</span></span>
<span data-ttu-id="efef2-108">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="efef2-108">Deletes a server.</span></span>

## <span data-ttu-id="efef2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efef2-109">EXAMPLES</span></span>

### <span data-ttu-id="efef2-110">Przykład 1. Usuwanie serwera MySql według nazwy serwera i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="efef2-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="efef2-111">To polecenie cmdlet usuwa serwer MySql według nazwy serwera i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efef2-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="efef2-112">Przykład 2. Usuwanie serwera MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="efef2-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Remove-AzMySqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="efef2-113">Te polecenia cmdlet usuwają serwer MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="efef2-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="efef2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efef2-114">PARAMETERS</span></span>

### <span data-ttu-id="efef2-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="efef2-115">-AsJob</span></span>
<span data-ttu-id="efef2-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="efef2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="efef2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efef2-117">-DefaultProfile</span></span>
<span data-ttu-id="efef2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efef2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efef2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efef2-119">-InputObject</span></span>
<span data-ttu-id="efef2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="efef2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efef2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="efef2-121">-Name</span></span>
<span data-ttu-id="efef2-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="efef2-122">The name of the server.</span></span>

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

### <span data-ttu-id="efef2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="efef2-123">-NoWait</span></span>
<span data-ttu-id="efef2-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="efef2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efef2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efef2-125">-PassThru</span></span>
<span data-ttu-id="efef2-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="efef2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="efef2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efef2-127">-ResourceGroupName</span></span>
<span data-ttu-id="efef2-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efef2-128">The name of the resource group.</span></span>
<span data-ttu-id="efef2-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="efef2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="efef2-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efef2-130">-SubscriptionId</span></span>
<span data-ttu-id="efef2-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="efef2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="efef2-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efef2-132">-Confirm</span></span>
<span data-ttu-id="efef2-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efef2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efef2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efef2-134">-WhatIf</span></span>
<span data-ttu-id="efef2-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efef2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efef2-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efef2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efef2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efef2-137">CommonParameters</span></span>
<span data-ttu-id="efef2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efef2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efef2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efef2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efef2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efef2-140">INPUTS</span></span>

### <span data-ttu-id="efef2-141">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="efef2-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="efef2-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efef2-142">OUTPUTS</span></span>

### <span data-ttu-id="efef2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efef2-143">System.Boolean</span></span>

## <span data-ttu-id="efef2-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efef2-144">NOTES</span></span>

<span data-ttu-id="efef2-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="efef2-145">ALIASES</span></span>

<span data-ttu-id="efef2-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="efef2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efef2-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="efef2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efef2-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efef2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efef2-149">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="efef2-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efef2-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="efef2-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="efef2-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="efef2-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="efef2-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efef2-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="efef2-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="efef2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efef2-154">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="efef2-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="efef2-155">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="efef2-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="efef2-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efef2-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="efef2-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="efef2-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="efef2-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="efef2-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="efef2-159">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="efef2-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="efef2-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="efef2-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="efef2-161">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="efef2-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="efef2-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efef2-162">RELATED LINKS</span></span>

