---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223379"
---
# <span data-ttu-id="8e733-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e733-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="8e733-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e733-102">SYNOPSIS</span></span>
<span data-ttu-id="8e733-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e733-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e733-104">SYNTAX</span></span>

### <span data-ttu-id="8e733-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8e733-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e733-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8e733-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e733-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e733-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8e733-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e733-108">DESCRIPTION</span></span>
<span data-ttu-id="8e733-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e733-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e733-110">EXAMPLES</span></span>

### <span data-ttu-id="8e733-111">Przykład 1: wyświetlanie wszystkich konfiguracji określonego serwera MySql</span><span class="sxs-lookup"><span data-stu-id="8e733-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="8e733-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji określonego serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="8e733-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="8e733-113">Przykład 2: pobieranie określonej konfiguracji MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="8e733-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="8e733-114">To polecenie cmdlet pobiera określoną konfigurację MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8e733-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="8e733-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e733-115">PARAMETERS</span></span>

### <span data-ttu-id="8e733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e733-116">-DefaultProfile</span></span>
<span data-ttu-id="8e733-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e733-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e733-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e733-118">-InputObject</span></span>
<span data-ttu-id="8e733-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8e733-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e733-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e733-120">-Name</span></span>
<span data-ttu-id="8e733-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="8e733-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e733-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e733-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e733-123">The name of the resource group.</span></span>
<span data-ttu-id="8e733-124">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8e733-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8e733-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8e733-125">-ServerName</span></span>
<span data-ttu-id="8e733-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-126">The name of the server.</span></span>

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

### <span data-ttu-id="8e733-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8e733-127">-SubscriptionId</span></span>
<span data-ttu-id="8e733-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8e733-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8e733-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e733-129">CommonParameters</span></span>
<span data-ttu-id="8e733-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e733-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e733-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e733-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e733-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e733-132">INPUTS</span></span>

### <span data-ttu-id="8e733-133">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8e733-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8e733-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e733-134">OUTPUTS</span></span>

### <span data-ttu-id="8e733-135">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e733-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="8e733-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e733-136">NOTES</span></span>

<span data-ttu-id="8e733-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8e733-137">ALIASES</span></span>

<span data-ttu-id="8e733-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e733-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e733-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8e733-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e733-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e733-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e733-141">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8e733-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e733-142">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8e733-143">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8e733-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8e733-144">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8e733-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8e733-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e733-146">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8e733-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8e733-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e733-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8e733-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8e733-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8e733-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8e733-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8e733-150">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8e733-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8e733-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8e733-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8e733-152">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e733-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8e733-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e733-153">RELATED LINKS</span></span>

