---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 97b16f3930eda94e69c3528432ee54927c3eef7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951089"
---
# <span data-ttu-id="b75a2-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b75a2-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="b75a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b75a2-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="b75a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b75a2-104">SYNTAX</span></span>

### <span data-ttu-id="b75a2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b75a2-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b75a2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b75a2-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b75a2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b75a2-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b75a2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b75a2-108">DESCRIPTION</span></span>
<span data-ttu-id="b75a2-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="b75a2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b75a2-110">EXAMPLES</span></span>

### <span data-ttu-id="b75a2-111">Przykład 1. Lista wszystkich konfiguracji na serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="b75a2-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="b75a2-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="b75a2-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="b75a2-113">Przykład 2. Uzyskiwanie określonej konfiguracji PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="b75a2-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="b75a2-114">To polecenie cmdlet uzyskuje określoną konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b75a2-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="b75a2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b75a2-115">PARAMETERS</span></span>

### <span data-ttu-id="b75a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75a2-116">-DefaultProfile</span></span>
<span data-ttu-id="b75a2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b75a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b75a2-118">-InputObject</span></span>
<span data-ttu-id="b75a2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b75a2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b75a2-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b75a2-120">-Name</span></span>
<span data-ttu-id="b75a2-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="b75a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="b75a2-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b75a2-123">The name of the resource group.</span></span>
<span data-ttu-id="b75a2-124">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b75a2-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b75a2-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b75a2-125">-ServerName</span></span>
<span data-ttu-id="b75a2-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-126">The name of the server.</span></span>

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

### <span data-ttu-id="b75a2-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b75a2-127">-SubscriptionId</span></span>
<span data-ttu-id="b75a2-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b75a2-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b75a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75a2-129">CommonParameters</span></span>
<span data-ttu-id="b75a2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75a2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b75a2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75a2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b75a2-132">INPUTS</span></span>

### <span data-ttu-id="b75a2-133">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b75a2-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b75a2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b75a2-134">OUTPUTS</span></span>

### <span data-ttu-id="b75a2-135">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="b75a2-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="b75a2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b75a2-136">NOTES</span></span>

<span data-ttu-id="b75a2-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b75a2-137">ALIASES</span></span>

<span data-ttu-id="b75a2-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b75a2-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b75a2-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b75a2-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b75a2-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b75a2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b75a2-141">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b75a2-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b75a2-142">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b75a2-143">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b75a2-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b75a2-144">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b75a2-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b75a2-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b75a2-146">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b75a2-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b75a2-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b75a2-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b75a2-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b75a2-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="b75a2-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="b75a2-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b75a2-150">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b75a2-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b75a2-151">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b75a2-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b75a2-152">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b75a2-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b75a2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b75a2-153">RELATED LINKS</span></span>

