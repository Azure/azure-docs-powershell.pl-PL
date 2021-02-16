---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190218"
---
# <span data-ttu-id="ec9f9-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ec9f9-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="ec9f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9f9-103">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-103">Restarts a server.</span></span>

## <span data-ttu-id="ec9f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec9f9-104">SYNTAX</span></span>

### <span data-ttu-id="ec9f9-105">Nazwa_serwera (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ec9f9-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec9f9-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="ec9f9-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec9f9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec9f9-107">DESCRIPTION</span></span>
<span data-ttu-id="ec9f9-108">Powoduje ponowne uruchomienie serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-108">Restarts a server.</span></span>

## <span data-ttu-id="ec9f9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec9f9-109">EXAMPLES</span></span>

### <span data-ttu-id="ec9f9-110">Przykład 1. Ponowne uruchamianie bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="ec9f9-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="ec9f9-111">To polecenie powoduje ponowne uruchomienie bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="ec9f9-112">Przykład 2. Ponowne uruchamianie bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="ec9f9-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="ec9f9-113">To polecenie powoduje ponowne uruchomienie bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="ec9f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec9f9-114">PARAMETERS</span></span>

### <span data-ttu-id="ec9f9-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ec9f9-115">-AsJob</span></span>
<span data-ttu-id="ec9f9-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ec9f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ec9f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9f9-117">-DefaultProfile</span></span>
<span data-ttu-id="ec9f9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec9f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec9f9-119">-InputObject</span></span>
<span data-ttu-id="ec9f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9f9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec9f9-121">-Name</span></span>
<span data-ttu-id="ec9f9-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9f9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec9f9-123">-NoWait</span></span>
<span data-ttu-id="ec9f9-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ec9f9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec9f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec9f9-125">-PassThru</span></span>
<span data-ttu-id="ec9f9-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec9f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec9f9-128">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ec9f9-129">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9f9-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec9f9-130">-SubscriptionId</span></span>
<span data-ttu-id="ec9f9-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9f9-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec9f9-132">-Confirm</span></span>
<span data-ttu-id="ec9f9-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec9f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9f9-134">-WhatIf</span></span>
<span data-ttu-id="ec9f9-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec9f9-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec9f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9f9-137">CommonParameters</span></span>
<span data-ttu-id="ec9f9-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9f9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec9f9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9f9-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec9f9-140">INPUTS</span></span>

### <span data-ttu-id="ec9f9-141">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ec9f9-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ec9f9-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec9f9-142">OUTPUTS</span></span>

### <span data-ttu-id="ec9f9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec9f9-143">System.Boolean</span></span>

## <span data-ttu-id="ec9f9-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec9f9-144">NOTES</span></span>

<span data-ttu-id="ec9f9-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ec9f9-145">ALIASES</span></span>

<span data-ttu-id="ec9f9-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ec9f9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec9f9-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec9f9-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec9f9-149">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec9f9-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec9f9-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ec9f9-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ec9f9-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ec9f9-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ec9f9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec9f9-154">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ec9f9-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ec9f9-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ec9f9-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ec9f9-158">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ec9f9-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ec9f9-160">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ec9f9-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ec9f9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec9f9-161">RELATED LINKS</span></span>

