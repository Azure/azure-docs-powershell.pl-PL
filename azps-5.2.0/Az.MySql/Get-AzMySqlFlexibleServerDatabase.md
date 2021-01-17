---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358976"
---
# <span data-ttu-id="a9af1-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="a9af1-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="a9af1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9af1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9af1-103">Pobiera informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a9af1-103">Gets information about a database.</span></span>

## <span data-ttu-id="a9af1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9af1-104">SYNTAX</span></span>

### <span data-ttu-id="a9af1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a9af1-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9af1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a9af1-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9af1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9af1-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9af1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9af1-108">DESCRIPTION</span></span>
<span data-ttu-id="a9af1-109">Pobiera informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a9af1-109">Gets information about a database.</span></span>

## <span data-ttu-id="a9af1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9af1-110">EXAMPLES</span></span>

### <span data-ttu-id="a9af1-111">Przykład 1: uzyskiwanie bazy danych MySql według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="a9af1-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="a9af1-112">To polecenie cmdlet umożliwia pobieranie serwera MySql według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9af1-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="a9af1-113">Przykład 2: pobieranie baz danych MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="a9af1-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="a9af1-114">To polecenie cmdlet umożliwia pobieranie serwera MySql przy użyciu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="a9af1-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="a9af1-115">Przykład 3: Lista wszystkich baz danych MySql na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="a9af1-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="a9af1-116">To polecenie cmdlet wyświetla listę wszystkich serwerów MySql znajdujących się w określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="a9af1-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="a9af1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9af1-117">PARAMETERS</span></span>

### <span data-ttu-id="a9af1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9af1-118">-DefaultProfile</span></span>
<span data-ttu-id="a9af1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9af1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9af1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9af1-120">-InputObject</span></span>
<span data-ttu-id="a9af1-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a9af1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a9af1-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9af1-122">-Name</span></span>
<span data-ttu-id="a9af1-123">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a9af1-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9af1-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9af1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9af1-125">The name of the resource group.</span></span>
<span data-ttu-id="a9af1-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a9af1-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9af1-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a9af1-127">-ServerName</span></span>
<span data-ttu-id="a9af1-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a9af1-128">The name of the server.</span></span>

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

### <span data-ttu-id="a9af1-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a9af1-129">-SubscriptionId</span></span>
<span data-ttu-id="a9af1-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a9af1-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9af1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9af1-131">CommonParameters</span></span>
<span data-ttu-id="a9af1-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9af1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9af1-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9af1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9af1-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9af1-134">INPUTS</span></span>

### <span data-ttu-id="a9af1-135">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a9af1-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a9af1-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9af1-136">OUTPUTS</span></span>

### <span data-ttu-id="a9af1-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="a9af1-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="a9af1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9af1-138">NOTES</span></span>

<span data-ttu-id="a9af1-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a9af1-139">ALIASES</span></span>

<span data-ttu-id="a9af1-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9af1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9af1-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a9af1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9af1-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9af1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9af1-143">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a9af1-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9af1-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a9af1-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9af1-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a9af1-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9af1-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="a9af1-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9af1-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a9af1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9af1-148">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="a9af1-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a9af1-149">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9af1-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9af1-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9af1-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a9af1-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a9af1-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9af1-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a9af1-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9af1-153">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a9af1-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9af1-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a9af1-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a9af1-155">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9af1-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9af1-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9af1-156">RELATED LINKS</span></span>

