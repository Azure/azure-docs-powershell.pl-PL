---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331162"
---
# <span data-ttu-id="35fde-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="35fde-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="35fde-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35fde-102">SYNOPSIS</span></span>
<span data-ttu-id="35fde-103">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="35fde-104">Zamiast tego użyj Update-AzPostgreSqlServer, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="35fde-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="35fde-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35fde-105">SYNTAX</span></span>

### <span data-ttu-id="35fde-106">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35fde-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35fde-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35fde-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35fde-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35fde-108">DESCRIPTION</span></span>
<span data-ttu-id="35fde-109">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="35fde-110">Zamiast tego użyj Update-AzPostgreSqlServer, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="35fde-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="35fde-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35fde-111">EXAMPLES</span></span>

### <span data-ttu-id="35fde-112">Przykład 1: aktualizowanie konfiguracji PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="35fde-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="35fde-113">To polecenie cmdlet powoduje zaktualizowanie konfiguracji PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="35fde-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="35fde-114">Przykład 2: aktualizowanie konfiguracji PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="35fde-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="35fde-115">Te polecenia cmdlet aktualizują konfigurację PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="35fde-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="35fde-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35fde-116">PARAMETERS</span></span>

### <span data-ttu-id="35fde-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35fde-117">-AsJob</span></span>
<span data-ttu-id="35fde-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="35fde-118">Run the command as a job</span></span>

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

### <span data-ttu-id="35fde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fde-119">-DefaultProfile</span></span>
<span data-ttu-id="35fde-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35fde-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fde-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35fde-121">-InputObject</span></span>
<span data-ttu-id="35fde-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="35fde-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35fde-123">-Name</span></span>
<span data-ttu-id="35fde-124">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="35fde-125">-NoWait</span></span>
<span data-ttu-id="35fde-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="35fde-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35fde-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35fde-127">-ResourceGroupName</span></span>
<span data-ttu-id="35fde-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35fde-128">The name of the resource group.</span></span>
<span data-ttu-id="35fde-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="35fde-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="35fde-130">-ServerName</span></span>
<span data-ttu-id="35fde-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-132">-Source</span><span class="sxs-lookup"><span data-stu-id="35fde-132">-Source</span></span>
<span data-ttu-id="35fde-133">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="35fde-133">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="35fde-134">-SubscriptionId</span></span>
<span data-ttu-id="35fde-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="35fde-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-136">-Value</span><span class="sxs-lookup"><span data-stu-id="35fde-136">-Value</span></span>
<span data-ttu-id="35fde-137">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="35fde-137">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fde-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35fde-138">-Confirm</span></span>
<span data-ttu-id="35fde-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fde-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35fde-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35fde-140">-WhatIf</span></span>
<span data-ttu-id="35fde-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fde-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35fde-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35fde-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35fde-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fde-143">CommonParameters</span></span>
<span data-ttu-id="35fde-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fde-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fde-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35fde-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fde-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35fde-146">INPUTS</span></span>

### <span data-ttu-id="35fde-147">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="35fde-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="35fde-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35fde-148">OUTPUTS</span></span>

### <span data-ttu-id="35fde-149">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="35fde-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="35fde-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35fde-150">NOTES</span></span>

<span data-ttu-id="35fde-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="35fde-151">ALIASES</span></span>

<span data-ttu-id="35fde-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35fde-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35fde-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="35fde-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35fde-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35fde-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35fde-155">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="35fde-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35fde-156">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="35fde-157">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="35fde-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="35fde-158">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="35fde-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="35fde-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35fde-160">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="35fde-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="35fde-161">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35fde-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35fde-162">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="35fde-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="35fde-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="35fde-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="35fde-164">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="35fde-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="35fde-165">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="35fde-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35fde-166">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="35fde-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="35fde-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35fde-167">RELATED LINKS</span></span>

