---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restart-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
ms.openlocfilehash: 3dfdf0129e8324220b20872964b68f324cb53cf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003729"
---
# <span data-ttu-id="dea92-101">Restart-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="dea92-101">Restart-AzMySqlServer</span></span>

## <span data-ttu-id="dea92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea92-102">SYNOPSIS</span></span>
<span data-ttu-id="dea92-103">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-103">Restarts a server.</span></span>

## <span data-ttu-id="dea92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dea92-104">SYNTAX</span></span>

### <span data-ttu-id="dea92-105">Ponowne uruchamianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dea92-105">Restart (Default)</span></span>
```
Restart-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dea92-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dea92-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dea92-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dea92-107">DESCRIPTION</span></span>
<span data-ttu-id="dea92-108">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-108">Restarts a server.</span></span>

## <span data-ttu-id="dea92-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dea92-109">EXAMPLES</span></span>

### <span data-ttu-id="dea92-110">Przykład 1. Ponowne uruchamianie serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="dea92-110">Example 1: Restart MySql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="dea92-111">To polecenie cmdlet powoduje ponowne uruchomienie serwera MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-111">This cmdlet restarts MySql server by resource group and server name.</span></span>

### <span data-ttu-id="dea92-112">Przykład 2. Ponowne uruchamianie serwera MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="dea92-112">Example 2: Restart MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/restart"
PS C:\> Restart-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="dea92-113">Te polecenia cmdlet ponownie uruchamiają serwer MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dea92-113">These cmdlets restart MySql server by identity.</span></span>

## <span data-ttu-id="dea92-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dea92-114">PARAMETERS</span></span>

### <span data-ttu-id="dea92-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="dea92-115">-AsJob</span></span>
<span data-ttu-id="dea92-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="dea92-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dea92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea92-117">-DefaultProfile</span></span>
<span data-ttu-id="dea92-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dea92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dea92-119">-InputObject</span></span>
<span data-ttu-id="dea92-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dea92-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dea92-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dea92-121">-Name</span></span>
<span data-ttu-id="dea92-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-122">The name of the server.</span></span>

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

### <span data-ttu-id="dea92-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dea92-123">-NoWait</span></span>
<span data-ttu-id="dea92-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="dea92-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dea92-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dea92-125">-PassThru</span></span>
<span data-ttu-id="dea92-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="dea92-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dea92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea92-127">-ResourceGroupName</span></span>
<span data-ttu-id="dea92-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dea92-128">The name of the resource group.</span></span>
<span data-ttu-id="dea92-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="dea92-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dea92-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dea92-130">-SubscriptionId</span></span>
<span data-ttu-id="dea92-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dea92-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dea92-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dea92-132">-Confirm</span></span>
<span data-ttu-id="dea92-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dea92-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea92-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea92-134">-WhatIf</span></span>
<span data-ttu-id="dea92-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea92-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dea92-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dea92-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea92-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea92-137">CommonParameters</span></span>
<span data-ttu-id="dea92-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea92-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea92-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dea92-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea92-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dea92-140">INPUTS</span></span>

### <span data-ttu-id="dea92-141">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dea92-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="dea92-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dea92-142">OUTPUTS</span></span>

### <span data-ttu-id="dea92-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dea92-143">System.Boolean</span></span>

## <span data-ttu-id="dea92-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dea92-144">NOTES</span></span>

<span data-ttu-id="dea92-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="dea92-145">ALIASES</span></span>

<span data-ttu-id="dea92-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dea92-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dea92-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dea92-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dea92-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dea92-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dea92-149">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="dea92-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dea92-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dea92-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dea92-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dea92-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dea92-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="dea92-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dea92-154">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="dea92-155">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dea92-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dea92-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dea92-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dea92-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="dea92-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="dea92-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="dea92-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dea92-159">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="dea92-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dea92-160">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dea92-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dea92-161">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dea92-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dea92-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dea92-162">RELATED LINKS</span></span>

