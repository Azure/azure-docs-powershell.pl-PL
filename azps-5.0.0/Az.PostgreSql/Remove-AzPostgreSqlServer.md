---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
ms.openlocfilehash: 6b0544bb2394b4d69c496ec4f2502360ddf173bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225828"
---
# <span data-ttu-id="12b1e-101">Remove-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="12b1e-101">Remove-AzPostgreSqlServer</span></span>

## <span data-ttu-id="12b1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="12b1e-103">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="12b1e-103">Deletes a server.</span></span>

## <span data-ttu-id="12b1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12b1e-104">SYNTAX</span></span>

### <span data-ttu-id="12b1e-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="12b1e-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12b1e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12b1e-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12b1e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="12b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="12b1e-108">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="12b1e-108">Deletes a server.</span></span>

## <span data-ttu-id="12b1e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="12b1e-110">Przykład 1: Usuwanie serwera PostgreSql przez przydzielonej nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="12b1e-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="12b1e-111">To polecenie cmdlet usuwa serwer PostgreSql przez przydzielone do niego nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="12b1e-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="12b1e-112">Przykład 2: Usuwanie serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="12b1e-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer"
PS C:\> Remove-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="12b1e-113">Te polecenia cmdlet usuwają PostgreSql serwer na podstawie tożsamości.</span><span class="sxs-lookup"><span data-stu-id="12b1e-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="12b1e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12b1e-114">PARAMETERS</span></span>

### <span data-ttu-id="12b1e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12b1e-115">-AsJob</span></span>
<span data-ttu-id="12b1e-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="12b1e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="12b1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b1e-117">-DefaultProfile</span></span>
<span data-ttu-id="12b1e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12b1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b1e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12b1e-119">-InputObject</span></span>
<span data-ttu-id="12b1e-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="12b1e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12b1e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12b1e-121">-Name</span></span>
<span data-ttu-id="12b1e-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="12b1e-122">The name of the server.</span></span>

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

### <span data-ttu-id="12b1e-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="12b1e-123">-NoWait</span></span>
<span data-ttu-id="12b1e-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="12b1e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12b1e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12b1e-125">-PassThru</span></span>
<span data-ttu-id="12b1e-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="12b1e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12b1e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b1e-127">-ResourceGroupName</span></span>
<span data-ttu-id="12b1e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12b1e-128">The name of the resource group.</span></span>
<span data-ttu-id="12b1e-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="12b1e-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="12b1e-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12b1e-130">-SubscriptionId</span></span>
<span data-ttu-id="12b1e-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="12b1e-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="12b1e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12b1e-132">-Confirm</span></span>
<span data-ttu-id="12b1e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b1e-134">-WhatIf</span></span>
<span data-ttu-id="12b1e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b1e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b1e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12b1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b1e-137">CommonParameters</span></span>
<span data-ttu-id="12b1e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b1e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12b1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b1e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12b1e-140">INPUTS</span></span>

### <span data-ttu-id="12b1e-141">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="12b1e-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="12b1e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12b1e-142">OUTPUTS</span></span>

### <span data-ttu-id="12b1e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12b1e-143">System.Boolean</span></span>

## <span data-ttu-id="12b1e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12b1e-144">NOTES</span></span>

<span data-ttu-id="12b1e-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="12b1e-145">ALIASES</span></span>

<span data-ttu-id="12b1e-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12b1e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12b1e-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="12b1e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12b1e-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12b1e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12b1e-149">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="12b1e-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12b1e-150">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="12b1e-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="12b1e-151">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="12b1e-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="12b1e-152">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="12b1e-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="12b1e-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="12b1e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12b1e-154">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="12b1e-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="12b1e-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12b1e-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="12b1e-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="12b1e-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="12b1e-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="12b1e-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="12b1e-158">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="12b1e-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="12b1e-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="12b1e-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="12b1e-160">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="12b1e-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="12b1e-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12b1e-161">RELATED LINKS</span></span>

