---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: 7b1ed42777dcd24460dabb91cf67160dac709aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985895"
---
# <span data-ttu-id="3783e-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3783e-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="3783e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3783e-102">SYNOPSIS</span></span>
<span data-ttu-id="3783e-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="3783e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3783e-104">SYNTAX</span></span>

### <span data-ttu-id="3783e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3783e-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3783e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3783e-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3783e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3783e-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3783e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3783e-108">DESCRIPTION</span></span>
<span data-ttu-id="3783e-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="3783e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3783e-110">EXAMPLES</span></span>

### <span data-ttu-id="3783e-111">Przykład 1. Lista wszystkich konfiguracji na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="3783e-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="3783e-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="3783e-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="3783e-113">Przykład 2. Uzyskiwanie określonej konfiguracji mysql według nazwy</span><span class="sxs-lookup"><span data-stu-id="3783e-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="3783e-114">To polecenie cmdlet określa konfigurację mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3783e-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="3783e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3783e-115">PARAMETERS</span></span>

### <span data-ttu-id="3783e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3783e-116">-DefaultProfile</span></span>
<span data-ttu-id="3783e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3783e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3783e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3783e-118">-InputObject</span></span>
<span data-ttu-id="3783e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3783e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3783e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3783e-120">-Name</span></span>
<span data-ttu-id="3783e-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3783e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3783e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3783e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3783e-123">The name of the resource group.</span></span>
<span data-ttu-id="3783e-124">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3783e-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3783e-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3783e-125">-ServerName</span></span>
<span data-ttu-id="3783e-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3783e-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3783e-127">-SubscriptionId</span></span>
<span data-ttu-id="3783e-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3783e-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3783e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3783e-129">CommonParameters</span></span>
<span data-ttu-id="3783e-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3783e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3783e-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3783e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3783e-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3783e-132">INPUTS</span></span>

### <span data-ttu-id="3783e-133">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3783e-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3783e-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3783e-134">OUTPUTS</span></span>

### <span data-ttu-id="3783e-135">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iConfiguration</span><span class="sxs-lookup"><span data-stu-id="3783e-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="3783e-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3783e-136">NOTES</span></span>

<span data-ttu-id="3783e-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3783e-137">ALIASES</span></span>

<span data-ttu-id="3783e-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3783e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3783e-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3783e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3783e-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3783e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3783e-141">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3783e-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3783e-142">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3783e-143">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3783e-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3783e-144">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3783e-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3783e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3783e-146">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="3783e-147">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3783e-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3783e-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3783e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3783e-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3783e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3783e-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3783e-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3783e-151">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3783e-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3783e-152">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3783e-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3783e-153">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3783e-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3783e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3783e-154">RELATED LINKS</span></span>

