---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012010"
---
# <span data-ttu-id="6348d-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="6348d-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="6348d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6348d-102">SYNOPSIS</span></span>
<span data-ttu-id="6348d-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="6348d-103">Gets information about a server.</span></span>

## <span data-ttu-id="6348d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6348d-104">SYNTAX</span></span>

### <span data-ttu-id="6348d-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6348d-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6348d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6348d-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6348d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6348d-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6348d-108">Lista</span><span class="sxs-lookup"><span data-stu-id="6348d-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6348d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6348d-109">DESCRIPTION</span></span>
<span data-ttu-id="6348d-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="6348d-110">Gets information about a server.</span></span>

## <span data-ttu-id="6348d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6348d-111">EXAMPLES</span></span>

### <span data-ttu-id="6348d-112">Przykład 1. Pobierz serwer MySql z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="6348d-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="6348d-113">To polecenie cmdlet pobiera serwery MySql z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="6348d-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="6348d-114">Przykład 2. Uzyskiwanie serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="6348d-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="6348d-115">To polecenie cmdlet pobiera serwery MySql według nazw serwerów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="6348d-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="6348d-116">Przykład 3. Lista wszystkich serwerów MySql w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6348d-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="6348d-117">To polecenie cmdlet wyświetla listę wszystkich serwerów MySql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6348d-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="6348d-118">Przykład 4. Uzyskiwanie serwera MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="6348d-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="6348d-119">Te listy polecenia cmdlet pobierają serwery MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6348d-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="6348d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6348d-120">PARAMETERS</span></span>

### <span data-ttu-id="6348d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6348d-121">-DefaultProfile</span></span>
<span data-ttu-id="6348d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6348d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6348d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6348d-123">-InputObject</span></span>
<span data-ttu-id="6348d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6348d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6348d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6348d-125">-Name</span></span>
<span data-ttu-id="6348d-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="6348d-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6348d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6348d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6348d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6348d-128">The name of the resource group.</span></span>
<span data-ttu-id="6348d-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6348d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6348d-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6348d-130">-SubscriptionId</span></span>
<span data-ttu-id="6348d-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6348d-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6348d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6348d-132">CommonParameters</span></span>
<span data-ttu-id="6348d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6348d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6348d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6348d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6348d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6348d-135">INPUTS</span></span>

### <span data-ttu-id="6348d-136">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6348d-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6348d-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6348d-137">OUTPUTS</span></span>

### <span data-ttu-id="6348d-138">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6348d-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="6348d-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6348d-139">NOTES</span></span>

<span data-ttu-id="6348d-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6348d-140">ALIASES</span></span>

<span data-ttu-id="6348d-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6348d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6348d-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6348d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6348d-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6348d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6348d-144">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6348d-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6348d-145">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="6348d-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6348d-146">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6348d-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6348d-147">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6348d-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6348d-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6348d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6348d-149">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="6348d-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="6348d-150">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6348d-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6348d-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6348d-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6348d-152">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6348d-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="6348d-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="6348d-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6348d-154">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="6348d-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6348d-155">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6348d-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6348d-156">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6348d-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6348d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6348d-157">RELATED LINKS</span></span>

