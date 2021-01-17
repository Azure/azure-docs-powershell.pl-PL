---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378506"
---
# <span data-ttu-id="64b4e-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="64b4e-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="64b4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="64b4e-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="64b4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64b4e-104">SYNTAX</span></span>

### <span data-ttu-id="64b4e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="64b4e-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64b4e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="64b4e-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64b4e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64b4e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="64b4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="64b4e-108">DESCRIPTION</span></span>
<span data-ttu-id="64b4e-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="64b4e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64b4e-110">EXAMPLES</span></span>

### <span data-ttu-id="64b4e-111">Przykład 1: wyświetlanie wszystkich konfiguracji na serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="64b4e-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="64b4e-112">To polecenie cmdlet wyświetla wszystkie konfiguracje określone na serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="64b4e-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="64b4e-113">Przykład 2: Uzyskaj określoną konfigurację PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="64b4e-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="64b4e-114">To polecenie cmdlet pobiera określoną konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="64b4e-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="64b4e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64b4e-115">PARAMETERS</span></span>

### <span data-ttu-id="64b4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b4e-116">-DefaultProfile</span></span>
<span data-ttu-id="64b4e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64b4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b4e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64b4e-118">-InputObject</span></span>
<span data-ttu-id="64b4e-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="64b4e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b4e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64b4e-120">-Name</span></span>
<span data-ttu-id="64b4e-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="64b4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="64b4e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64b4e-123">The name of the resource group.</span></span>
<span data-ttu-id="64b4e-124">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="64b4e-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="64b4e-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="64b4e-125">-ServerName</span></span>
<span data-ttu-id="64b4e-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-126">The name of the server.</span></span>

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

### <span data-ttu-id="64b4e-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="64b4e-127">-SubscriptionId</span></span>
<span data-ttu-id="64b4e-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="64b4e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="64b4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b4e-129">CommonParameters</span></span>
<span data-ttu-id="64b4e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b4e-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64b4e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b4e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64b4e-132">INPUTS</span></span>

### <span data-ttu-id="64b4e-133">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="64b4e-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="64b4e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64b4e-134">OUTPUTS</span></span>

### <span data-ttu-id="64b4e-135">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="64b4e-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="64b4e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64b4e-136">NOTES</span></span>

<span data-ttu-id="64b4e-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="64b4e-137">ALIASES</span></span>

<span data-ttu-id="64b4e-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64b4e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64b4e-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="64b4e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64b4e-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64b4e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64b4e-141">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="64b4e-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64b4e-142">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="64b4e-143">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="64b4e-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="64b4e-144">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="64b4e-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="64b4e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64b4e-146">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="64b4e-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="64b4e-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64b4e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="64b4e-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="64b4e-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="64b4e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="64b4e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="64b4e-150">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="64b4e-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="64b4e-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="64b4e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="64b4e-152">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64b4e-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="64b4e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64b4e-153">RELATED LINKS</span></span>

