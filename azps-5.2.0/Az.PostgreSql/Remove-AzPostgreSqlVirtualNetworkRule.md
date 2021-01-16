---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331177"
---
# <span data-ttu-id="0094d-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0094d-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="0094d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0094d-102">SYNOPSIS</span></span>
<span data-ttu-id="0094d-103">Usuwa regułę sieci wirtualnej o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="0094d-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="0094d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0094d-104">SYNTAX</span></span>

### <span data-ttu-id="0094d-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0094d-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0094d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0094d-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0094d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0094d-107">DESCRIPTION</span></span>
<span data-ttu-id="0094d-108">Usuwa regułę sieci wirtualnej o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="0094d-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="0094d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0094d-109">EXAMPLES</span></span>

### <span data-ttu-id="0094d-110">Przykład 1: Usuwanie reguły sieci wirtualnej serwera PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="0094d-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="0094d-111">To polecenie cmdlet usuwa regułę sieci wirtualnej serwera PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0094d-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="0094d-112">Przykład 2: Usuwanie reguły sieci wirtualnej serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="0094d-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="0094d-113">Te polecenia cmdlet usuwają zasadę sieci wirtualnej serwera PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0094d-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="0094d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0094d-114">PARAMETERS</span></span>

### <span data-ttu-id="0094d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0094d-115">-AsJob</span></span>
<span data-ttu-id="0094d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0094d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0094d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0094d-117">-DefaultProfile</span></span>
<span data-ttu-id="0094d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0094d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0094d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0094d-119">-InputObject</span></span>
<span data-ttu-id="0094d-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0094d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0094d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0094d-121">-Name</span></span>
<span data-ttu-id="0094d-122">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0094d-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0094d-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0094d-123">-NoWait</span></span>
<span data-ttu-id="0094d-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0094d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0094d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0094d-125">-PassThru</span></span>
<span data-ttu-id="0094d-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="0094d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0094d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0094d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0094d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0094d-128">The name of the resource group.</span></span>
<span data-ttu-id="0094d-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0094d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0094d-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0094d-130">-ServerName</span></span>
<span data-ttu-id="0094d-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0094d-131">The name of the server.</span></span>

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

### <span data-ttu-id="0094d-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0094d-132">-SubscriptionId</span></span>
<span data-ttu-id="0094d-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0094d-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0094d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0094d-134">-Confirm</span></span>
<span data-ttu-id="0094d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0094d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0094d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0094d-136">-WhatIf</span></span>
<span data-ttu-id="0094d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0094d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0094d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0094d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0094d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0094d-139">CommonParameters</span></span>
<span data-ttu-id="0094d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0094d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0094d-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0094d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0094d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0094d-142">INPUTS</span></span>

### <span data-ttu-id="0094d-143">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0094d-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0094d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0094d-144">OUTPUTS</span></span>

### <span data-ttu-id="0094d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0094d-145">System.Boolean</span></span>

## <span data-ttu-id="0094d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0094d-146">NOTES</span></span>

<span data-ttu-id="0094d-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0094d-147">ALIASES</span></span>

<span data-ttu-id="0094d-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0094d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0094d-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0094d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0094d-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0094d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0094d-151">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0094d-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0094d-152">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0094d-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0094d-153">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0094d-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0094d-154">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0094d-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0094d-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0094d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0094d-156">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0094d-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0094d-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0094d-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0094d-158">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0094d-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="0094d-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0094d-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0094d-160">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0094d-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0094d-161">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0094d-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0094d-162">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0094d-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0094d-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0094d-163">RELATED LINKS</span></span>

