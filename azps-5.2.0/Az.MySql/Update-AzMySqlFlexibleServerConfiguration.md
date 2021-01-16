---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360222"
---
# <span data-ttu-id="f148a-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f148a-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="f148a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f148a-102">SYNOPSIS</span></span>
<span data-ttu-id="f148a-103">Aktualizuje informacje na temat konfiguracji serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="f148a-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="f148a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f148a-104">SYNTAX</span></span>

### <span data-ttu-id="f148a-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f148a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f148a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f148a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f148a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f148a-107">DESCRIPTION</span></span>
<span data-ttu-id="f148a-108">Aktualizuje informacje na temat konfiguracji serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="f148a-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="f148a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f148a-109">EXAMPLES</span></span>

### <span data-ttu-id="f148a-110">Przykład 1: aktualizowanie konfiguracji MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="f148a-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="f148a-111">To polecenie cmdlet powoduje zaktualizowanie konfiguracji MySql za pomocą nazwy.</span><span class="sxs-lookup"><span data-stu-id="f148a-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="f148a-112">Przykład 2: aktualizowanie konfiguracji MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f148a-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="f148a-113">Te polecenia cmdlet aktualizują konfigurację MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="f148a-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="f148a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f148a-114">PARAMETERS</span></span>

### <span data-ttu-id="f148a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f148a-115">-AsJob</span></span>
<span data-ttu-id="f148a-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f148a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f148a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f148a-117">-DefaultProfile</span></span>
<span data-ttu-id="f148a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f148a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f148a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f148a-119">-InputObject</span></span>
<span data-ttu-id="f148a-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f148a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f148a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f148a-121">-Name</span></span>
<span data-ttu-id="f148a-122">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="f148a-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f148a-123">-NoWait</span></span>
<span data-ttu-id="f148a-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f148a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f148a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f148a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f148a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f148a-126">The name of the resource group.</span></span>
<span data-ttu-id="f148a-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f148a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f148a-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f148a-128">-ServerName</span></span>
<span data-ttu-id="f148a-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-129">The name of the server.</span></span>

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

### <span data-ttu-id="f148a-130">-Source</span><span class="sxs-lookup"><span data-stu-id="f148a-130">-Source</span></span>
<span data-ttu-id="f148a-131">Źródło wartości aktualizującej.</span><span class="sxs-lookup"><span data-stu-id="f148a-131">The source of the updating value.</span></span>
<span data-ttu-id="f148a-132">Wartość domyślna to zastąpienie przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="f148a-132">The default value is user-override</span></span>

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

### <span data-ttu-id="f148a-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f148a-133">-SubscriptionId</span></span>
<span data-ttu-id="f148a-134">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f148a-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f148a-135">-Value</span><span class="sxs-lookup"><span data-stu-id="f148a-135">-Value</span></span>
<span data-ttu-id="f148a-136">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="f148a-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="f148a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f148a-137">-Confirm</span></span>
<span data-ttu-id="f148a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f148a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f148a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f148a-139">-WhatIf</span></span>
<span data-ttu-id="f148a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f148a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f148a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f148a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f148a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f148a-142">CommonParameters</span></span>
<span data-ttu-id="f148a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f148a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f148a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f148a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f148a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f148a-145">INPUTS</span></span>

### <span data-ttu-id="f148a-146">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f148a-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f148a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f148a-147">OUTPUTS</span></span>

### <span data-ttu-id="f148a-148">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f148a-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="f148a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f148a-149">NOTES</span></span>

<span data-ttu-id="f148a-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f148a-150">ALIASES</span></span>

<span data-ttu-id="f148a-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f148a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f148a-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f148a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f148a-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f148a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f148a-154">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f148a-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f148a-155">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f148a-156">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f148a-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f148a-157">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f148a-158">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f148a-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f148a-159">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f148a-160">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f148a-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f148a-161">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f148a-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f148a-162">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f148a-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f148a-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f148a-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f148a-164">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f148a-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f148a-165">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f148a-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f148a-166">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f148a-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f148a-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f148a-167">RELATED LINKS</span></span>

