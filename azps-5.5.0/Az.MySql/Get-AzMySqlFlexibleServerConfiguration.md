---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203375"
---
# <span data-ttu-id="23949-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="23949-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="23949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23949-102">SYNOPSIS</span></span>
<span data-ttu-id="23949-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="23949-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23949-104">SYNTAX</span></span>

### <span data-ttu-id="23949-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="23949-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23949-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="23949-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23949-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23949-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23949-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="23949-108">DESCRIPTION</span></span>
<span data-ttu-id="23949-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="23949-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23949-110">EXAMPLES</span></span>

### <span data-ttu-id="23949-111">Przykład 1. Lista wszystkich konfiguracji na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="23949-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="23949-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="23949-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="23949-113">Przykład 2. Uzyskiwanie określonej konfiguracji mysql według nazwy</span><span class="sxs-lookup"><span data-stu-id="23949-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="23949-114">To polecenie cmdlet określa konfigurację mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="23949-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="23949-115">Przykład 3. Konfiguracja listy według tożsamości</span><span class="sxs-lookup"><span data-stu-id="23949-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="23949-116">To polecenie cmdlet jest określane przez tożsamość w konfiguracji mysql.</span><span class="sxs-lookup"><span data-stu-id="23949-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="23949-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23949-117">PARAMETERS</span></span>

### <span data-ttu-id="23949-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23949-118">-DefaultProfile</span></span>
<span data-ttu-id="23949-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23949-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23949-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23949-120">-InputObject</span></span>
<span data-ttu-id="23949-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="23949-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23949-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23949-122">-Name</span></span>
<span data-ttu-id="23949-123">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="23949-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23949-124">-ResourceGroupName</span></span>
<span data-ttu-id="23949-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23949-125">The name of the resource group.</span></span>
<span data-ttu-id="23949-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="23949-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="23949-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23949-127">-ServerName</span></span>
<span data-ttu-id="23949-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-128">The name of the server.</span></span>

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

### <span data-ttu-id="23949-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23949-129">-SubscriptionId</span></span>
<span data-ttu-id="23949-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="23949-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="23949-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23949-131">CommonParameters</span></span>
<span data-ttu-id="23949-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23949-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23949-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23949-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23949-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23949-134">INPUTS</span></span>

### <span data-ttu-id="23949-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="23949-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="23949-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23949-136">OUTPUTS</span></span>

### <span data-ttu-id="23949-137">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="23949-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="23949-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23949-138">NOTES</span></span>

<span data-ttu-id="23949-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="23949-139">ALIASES</span></span>

<span data-ttu-id="23949-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="23949-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23949-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="23949-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23949-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23949-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23949-143">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="23949-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23949-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="23949-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="23949-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="23949-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="23949-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="23949-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23949-148">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="23949-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="23949-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="23949-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23949-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="23949-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="23949-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="23949-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="23949-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="23949-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="23949-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="23949-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="23949-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="23949-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="23949-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="23949-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23949-156">RELATED LINKS</span></span>

