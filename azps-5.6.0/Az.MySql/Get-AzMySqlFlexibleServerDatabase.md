---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: b060657d9e8d69ebddf639847de7718ec626fdb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991033"
---
# <span data-ttu-id="0b315-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="0b315-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="0b315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b315-102">SYNOPSIS</span></span>
<span data-ttu-id="0b315-103">Pobiera informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0b315-103">Gets information about a database.</span></span>

## <span data-ttu-id="0b315-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b315-104">SYNTAX</span></span>

### <span data-ttu-id="0b315-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0b315-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b315-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0b315-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b315-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0b315-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b315-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b315-108">DESCRIPTION</span></span>
<span data-ttu-id="0b315-109">Pobiera informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0b315-109">Gets information about a database.</span></span>

## <span data-ttu-id="0b315-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b315-110">EXAMPLES</span></span>

### <span data-ttu-id="0b315-111">Przykład 1. Uzyskiwanie bazy danych MySql według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="0b315-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="0b315-112">To polecenie cmdlet pobiera serwer MySql według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b315-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="0b315-113">Przykład 2. Uzyskiwanie baz danych MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="0b315-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="0b315-114">To polecenie cmdlet uzyskuje serwer MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0b315-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="0b315-115">Przykład 3. Lista wszystkich baz danych MySql na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="0b315-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="0b315-116">To polecenie cmdlet wyświetla listę wszystkich serwerów MySql w określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="0b315-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="0b315-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b315-117">PARAMETERS</span></span>

### <span data-ttu-id="0b315-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b315-118">-DefaultProfile</span></span>
<span data-ttu-id="0b315-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b315-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b315-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b315-120">-InputObject</span></span>
<span data-ttu-id="0b315-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0b315-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b315-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b315-122">-Name</span></span>
<span data-ttu-id="0b315-123">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b315-123">The name of the database.</span></span>

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

### <span data-ttu-id="0b315-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b315-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b315-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b315-125">The name of the resource group.</span></span>
<span data-ttu-id="0b315-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0b315-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b315-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b315-127">-ServerName</span></span>
<span data-ttu-id="0b315-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0b315-128">The name of the server.</span></span>

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

### <span data-ttu-id="0b315-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b315-129">-SubscriptionId</span></span>
<span data-ttu-id="0b315-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0b315-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b315-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b315-131">CommonParameters</span></span>
<span data-ttu-id="0b315-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b315-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b315-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b315-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b315-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b315-134">INPUTS</span></span>

### <span data-ttu-id="0b315-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0b315-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0b315-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b315-136">OUTPUTS</span></span>

### <span data-ttu-id="0b315-137">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iDatabase</span><span class="sxs-lookup"><span data-stu-id="0b315-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="0b315-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b315-138">NOTES</span></span>

<span data-ttu-id="0b315-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0b315-139">ALIASES</span></span>

<span data-ttu-id="0b315-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b315-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b315-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0b315-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b315-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b315-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b315-143">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0b315-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b315-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0b315-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0b315-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b315-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0b315-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0b315-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0b315-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0b315-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b315-148">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="0b315-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0b315-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0b315-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0b315-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b315-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0b315-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0b315-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="0b315-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0b315-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0b315-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0b315-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0b315-154">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0b315-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0b315-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b315-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0b315-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b315-156">RELATED LINKS</span></span>

