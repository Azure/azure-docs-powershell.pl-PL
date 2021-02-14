---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: dacaab524db0403d4f7c1ac2df9b215e920afa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203352"
---
# <span data-ttu-id="92286-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="92286-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="92286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92286-102">SYNOPSIS</span></span>
<span data-ttu-id="92286-103">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-103">Restarts a server.</span></span>

## <span data-ttu-id="92286-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92286-104">SYNTAX</span></span>

### <span data-ttu-id="92286-105">Ponowne uruchamianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="92286-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92286-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92286-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92286-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="92286-107">DESCRIPTION</span></span>
<span data-ttu-id="92286-108">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-108">Restarts a server.</span></span>

## <span data-ttu-id="92286-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92286-109">EXAMPLES</span></span>

### <span data-ttu-id="92286-110">Przykład 1. Ponowne uruchamianie serwera według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="92286-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="92286-111">Ponowne uruchamianie serwera według nazwy</span><span class="sxs-lookup"><span data-stu-id="92286-111">Restart the server by name</span></span>

### <span data-ttu-id="92286-112">Przykład 2. Ponowne uruchamianie serwera według tożsamości</span><span class="sxs-lookup"><span data-stu-id="92286-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="92286-113">Ponowne uruchamianie serwera według tożsamości</span><span class="sxs-lookup"><span data-stu-id="92286-113">Restart the server by identity</span></span>

## <span data-ttu-id="92286-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92286-114">PARAMETERS</span></span>

### <span data-ttu-id="92286-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="92286-115">-AsJob</span></span>
<span data-ttu-id="92286-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="92286-116">Run the command as a job</span></span>

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

### <span data-ttu-id="92286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92286-117">-DefaultProfile</span></span>
<span data-ttu-id="92286-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92286-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92286-119">-InputObject</span></span>
<span data-ttu-id="92286-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="92286-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92286-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92286-121">-Name</span></span>
<span data-ttu-id="92286-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-122">The name of the server.</span></span>

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

### <span data-ttu-id="92286-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92286-123">-NoWait</span></span>
<span data-ttu-id="92286-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="92286-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92286-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92286-125">-PassThru</span></span>
<span data-ttu-id="92286-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="92286-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92286-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92286-127">-ResourceGroupName</span></span>
<span data-ttu-id="92286-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92286-128">The name of the resource group.</span></span>
<span data-ttu-id="92286-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="92286-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="92286-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92286-130">-SubscriptionId</span></span>
<span data-ttu-id="92286-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="92286-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="92286-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92286-132">-Confirm</span></span>
<span data-ttu-id="92286-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="92286-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92286-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92286-134">-WhatIf</span></span>
<span data-ttu-id="92286-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92286-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92286-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="92286-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92286-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92286-137">CommonParameters</span></span>
<span data-ttu-id="92286-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92286-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92286-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92286-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92286-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92286-140">INPUTS</span></span>

### <span data-ttu-id="92286-141">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="92286-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="92286-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92286-142">OUTPUTS</span></span>

### <span data-ttu-id="92286-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92286-143">System.Boolean</span></span>

## <span data-ttu-id="92286-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92286-144">NOTES</span></span>

<span data-ttu-id="92286-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="92286-145">ALIASES</span></span>

<span data-ttu-id="92286-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="92286-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92286-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="92286-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92286-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92286-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92286-149">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="92286-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92286-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="92286-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92286-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="92286-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="92286-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="92286-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92286-154">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="92286-155">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="92286-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="92286-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92286-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92286-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="92286-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="92286-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="92286-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="92286-159">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="92286-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="92286-160">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="92286-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92286-161">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92286-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="92286-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92286-162">RELATED LINKS</span></span>

