---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498886"
---
# <span data-ttu-id="76a5a-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="76a5a-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="76a5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="76a5a-103">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="76a5a-104">Zamiast tego użyj Update-AzMySqlServer, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="76a5a-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="76a5a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76a5a-105">SYNTAX</span></span>

### <span data-ttu-id="76a5a-106">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76a5a-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76a5a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76a5a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76a5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="76a5a-109">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="76a5a-110">Zamiast tego użyj Update-AzMySqlServer, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="76a5a-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="76a5a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76a5a-111">EXAMPLES</span></span>

### <span data-ttu-id="76a5a-112">Przykład 1: aktualizowanie konfiguracji MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="76a5a-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="76a5a-113">To polecenie cmdlet powoduje zaktualizowanie konfiguracji MySql za pomocą nazwy.</span><span class="sxs-lookup"><span data-stu-id="76a5a-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="76a5a-114">Przykład 2: aktualizowanie konfiguracji MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="76a5a-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="76a5a-115">Te polecenia cmdlet aktualizują konfigurację MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="76a5a-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="76a5a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76a5a-116">PARAMETERS</span></span>

### <span data-ttu-id="76a5a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76a5a-117">-AsJob</span></span>
<span data-ttu-id="76a5a-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="76a5a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="76a5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a5a-119">-DefaultProfile</span></span>
<span data-ttu-id="76a5a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76a5a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a5a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76a5a-121">-InputObject</span></span>
<span data-ttu-id="76a5a-122">Parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="76a5a-122">Identity Parameter.</span></span>
<span data-ttu-id="76a5a-123">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="76a5a-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76a5a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76a5a-124">-Name</span></span>
<span data-ttu-id="76a5a-125">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="76a5a-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76a5a-126">-NoWait</span></span>
<span data-ttu-id="76a5a-127">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="76a5a-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76a5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="76a5a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76a5a-129">The name of the resource group.</span></span>
<span data-ttu-id="76a5a-130">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="76a5a-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76a5a-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="76a5a-131">-ServerName</span></span>
<span data-ttu-id="76a5a-132">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-132">The name of the server.</span></span>

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

### <span data-ttu-id="76a5a-133">-Source</span><span class="sxs-lookup"><span data-stu-id="76a5a-133">-Source</span></span>
<span data-ttu-id="76a5a-134">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="76a5a-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="76a5a-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="76a5a-135">-SubscriptionId</span></span>
<span data-ttu-id="76a5a-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="76a5a-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="76a5a-137">-Value</span><span class="sxs-lookup"><span data-stu-id="76a5a-137">-Value</span></span>
<span data-ttu-id="76a5a-138">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="76a5a-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="76a5a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76a5a-139">-Confirm</span></span>
<span data-ttu-id="76a5a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a5a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a5a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a5a-141">-WhatIf</span></span>
<span data-ttu-id="76a5a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a5a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a5a-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76a5a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a5a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a5a-144">CommonParameters</span></span>
<span data-ttu-id="76a5a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a5a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a5a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a5a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a5a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76a5a-147">INPUTS</span></span>

### <span data-ttu-id="76a5a-148">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="76a5a-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="76a5a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76a5a-149">OUTPUTS</span></span>

### <span data-ttu-id="76a5a-150">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="76a5a-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="76a5a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76a5a-151">NOTES</span></span>

<span data-ttu-id="76a5a-152">PISUJE</span><span class="sxs-lookup"><span data-stu-id="76a5a-152">ALIASES</span></span>

<span data-ttu-id="76a5a-153">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76a5a-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76a5a-154">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="76a5a-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76a5a-155">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76a5a-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76a5a-156">INPUTobject <IMySqlIdentity> : parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="76a5a-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="76a5a-157">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="76a5a-158">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="76a5a-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="76a5a-159">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="76a5a-160">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="76a5a-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76a5a-161">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="76a5a-162">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="76a5a-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="76a5a-163">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76a5a-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76a5a-164">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="76a5a-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="76a5a-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="76a5a-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="76a5a-166">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="76a5a-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="76a5a-167">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="76a5a-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76a5a-168">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="76a5a-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="76a5a-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76a5a-169">RELATED LINKS</span></span>

