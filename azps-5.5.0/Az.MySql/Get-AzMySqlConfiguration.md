---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194051"
---
# <span data-ttu-id="93403-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="93403-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="93403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93403-102">SYNOPSIS</span></span>
<span data-ttu-id="93403-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="93403-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93403-104">SYNTAX</span></span>

### <span data-ttu-id="93403-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="93403-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93403-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="93403-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93403-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93403-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="93403-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="93403-108">DESCRIPTION</span></span>
<span data-ttu-id="93403-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="93403-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93403-110">EXAMPLES</span></span>

### <span data-ttu-id="93403-111">Przykład 1. Lista wszystkich konfiguracji na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="93403-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="93403-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="93403-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="93403-113">Przykład 2. Uzyskiwanie określonej konfiguracji programu MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="93403-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="93403-114">To polecenie cmdlet określa konfigurację mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="93403-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="93403-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93403-115">PARAMETERS</span></span>

### <span data-ttu-id="93403-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93403-116">-DefaultProfile</span></span>
<span data-ttu-id="93403-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93403-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93403-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93403-118">-InputObject</span></span>
<span data-ttu-id="93403-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="93403-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93403-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93403-120">-Name</span></span>
<span data-ttu-id="93403-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="93403-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93403-122">-ResourceGroupName</span></span>
<span data-ttu-id="93403-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93403-123">The name of the resource group.</span></span>
<span data-ttu-id="93403-124">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="93403-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="93403-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93403-125">-ServerName</span></span>
<span data-ttu-id="93403-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-126">The name of the server.</span></span>

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

### <span data-ttu-id="93403-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93403-127">-SubscriptionId</span></span>
<span data-ttu-id="93403-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="93403-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="93403-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93403-129">CommonParameters</span></span>
<span data-ttu-id="93403-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93403-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93403-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93403-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93403-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93403-132">INPUTS</span></span>

### <span data-ttu-id="93403-133">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="93403-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="93403-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93403-134">OUTPUTS</span></span>

### <span data-ttu-id="93403-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="93403-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="93403-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93403-136">NOTES</span></span>

<span data-ttu-id="93403-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="93403-137">ALIASES</span></span>

<span data-ttu-id="93403-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="93403-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93403-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="93403-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93403-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93403-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93403-141">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="93403-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93403-142">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="93403-143">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="93403-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="93403-144">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="93403-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="93403-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93403-146">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="93403-147">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="93403-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="93403-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93403-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="93403-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="93403-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="93403-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="93403-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="93403-151">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="93403-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="93403-152">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="93403-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="93403-153">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93403-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="93403-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93403-154">RELATED LINKS</span></span>

