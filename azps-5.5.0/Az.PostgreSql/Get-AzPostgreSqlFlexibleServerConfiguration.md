---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179162"
---
# <span data-ttu-id="ff3a0-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff3a0-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="ff3a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3a0-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ff3a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff3a0-104">SYNTAX</span></span>

### <span data-ttu-id="ff3a0-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ff3a0-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff3a0-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ff3a0-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff3a0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff3a0-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff3a0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff3a0-108">DESCRIPTION</span></span>
<span data-ttu-id="ff3a0-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ff3a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff3a0-110">EXAMPLES</span></span>

### <span data-ttu-id="ff3a0-111">Przykład 1. Uzyskiwanie określonej konfiguracji PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="ff3a0-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="ff3a0-112">To polecenie cmdlet uzyskuje określoną konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="ff3a0-113">Przykład 2. Lista wszystkich konfiguracji na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ff3a0-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="ff3a0-114">To polecenie cmdlet wyświetla listę wszystkich konfiguracji na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="ff3a0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff3a0-115">PARAMETERS</span></span>

### <span data-ttu-id="ff3a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3a0-116">-DefaultProfile</span></span>
<span data-ttu-id="ff3a0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff3a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff3a0-118">-InputObject</span></span>
<span data-ttu-id="ff3a0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff3a0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff3a0-120">-Name</span></span>
<span data-ttu-id="ff3a0-121">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ff3a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff3a0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-123">The name of the resource group.</span></span>
<span data-ttu-id="ff3a0-124">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ff3a0-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff3a0-125">-ServerName</span></span>
<span data-ttu-id="ff3a0-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-126">The name of the server.</span></span>

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

### <span data-ttu-id="ff3a0-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff3a0-127">-SubscriptionId</span></span>
<span data-ttu-id="ff3a0-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ff3a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3a0-129">CommonParameters</span></span>
<span data-ttu-id="ff3a0-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3a0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff3a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3a0-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3a0-132">INPUTS</span></span>

### <span data-ttu-id="ff3a0-133">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ff3a0-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ff3a0-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3a0-134">OUTPUTS</span></span>

### <span data-ttu-id="ff3a0-135">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ff3a0-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="ff3a0-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff3a0-136">NOTES</span></span>

<span data-ttu-id="ff3a0-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ff3a0-137">ALIASES</span></span>

<span data-ttu-id="ff3a0-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ff3a0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff3a0-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff3a0-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff3a0-141">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ff3a0-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff3a0-142">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ff3a0-143">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ff3a0-144">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ff3a0-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ff3a0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff3a0-146">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ff3a0-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ff3a0-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="ff3a0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ff3a0-150">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ff3a0-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ff3a0-152">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ff3a0-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff3a0-153">RELATED LINKS</span></span>

