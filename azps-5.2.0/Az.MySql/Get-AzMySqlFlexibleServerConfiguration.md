---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330253"
---
# <span data-ttu-id="a587e-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a587e-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a587e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a587e-102">SYNOPSIS</span></span>
<span data-ttu-id="a587e-103">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a587e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a587e-104">SYNTAX</span></span>

### <span data-ttu-id="a587e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a587e-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a587e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a587e-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a587e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a587e-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a587e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a587e-108">DESCRIPTION</span></span>
<span data-ttu-id="a587e-109">Pobiera informacje o konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a587e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a587e-110">EXAMPLES</span></span>

### <span data-ttu-id="a587e-111">Przykład 1: wyświetlanie wszystkich konfiguracji określonego serwera MySql</span><span class="sxs-lookup"><span data-stu-id="a587e-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a587e-112">To polecenie cmdlet wyświetla listę wszystkich konfiguracji określonego serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="a587e-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="a587e-113">Przykład 2: pobieranie określonej konfiguracji MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="a587e-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a587e-114">To polecenie cmdlet pobiera określoną konfigurację MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a587e-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="a587e-115">Przykład 3: konfiguracja listy według tożsamości</span><span class="sxs-lookup"><span data-stu-id="a587e-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a587e-116">To polecenie cmdlet umożliwia określenie konfiguracji MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a587e-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="a587e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a587e-117">PARAMETERS</span></span>

### <span data-ttu-id="a587e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a587e-118">-DefaultProfile</span></span>
<span data-ttu-id="a587e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a587e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a587e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a587e-120">-InputObject</span></span>
<span data-ttu-id="a587e-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a587e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a587e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a587e-122">-Name</span></span>
<span data-ttu-id="a587e-123">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a587e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a587e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a587e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a587e-125">The name of the resource group.</span></span>
<span data-ttu-id="a587e-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a587e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a587e-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a587e-127">-ServerName</span></span>
<span data-ttu-id="a587e-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-128">The name of the server.</span></span>

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

### <span data-ttu-id="a587e-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a587e-129">-SubscriptionId</span></span>
<span data-ttu-id="a587e-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a587e-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a587e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a587e-131">CommonParameters</span></span>
<span data-ttu-id="a587e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a587e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a587e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a587e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a587e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a587e-134">INPUTS</span></span>

### <span data-ttu-id="a587e-135">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a587e-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a587e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a587e-136">OUTPUTS</span></span>

### <span data-ttu-id="a587e-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a587e-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a587e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a587e-138">NOTES</span></span>

<span data-ttu-id="a587e-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a587e-139">ALIASES</span></span>

<span data-ttu-id="a587e-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a587e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a587e-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a587e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a587e-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a587e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a587e-143">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a587e-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a587e-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a587e-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a587e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a587e-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a587e-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a587e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a587e-148">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a587e-149">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a587e-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a587e-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a587e-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a587e-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a587e-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a587e-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a587e-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a587e-153">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a587e-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a587e-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a587e-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a587e-155">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a587e-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a587e-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a587e-156">RELATED LINKS</span></span>

