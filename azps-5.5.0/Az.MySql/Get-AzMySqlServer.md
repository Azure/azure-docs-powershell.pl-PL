---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192123"
---
# <span data-ttu-id="2ffb2-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="2ffb2-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="2ffb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ffb2-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffb2-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-103">Gets information about a server.</span></span>

## <span data-ttu-id="2ffb2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ffb2-104">SYNTAX</span></span>

### <span data-ttu-id="2ffb2-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2ffb2-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ffb2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2ffb2-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ffb2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ffb2-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ffb2-108">Lista</span><span class="sxs-lookup"><span data-stu-id="2ffb2-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ffb2-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ffb2-109">DESCRIPTION</span></span>
<span data-ttu-id="2ffb2-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-110">Gets information about a server.</span></span>

## <span data-ttu-id="2ffb2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ffb2-111">EXAMPLES</span></span>

### <span data-ttu-id="2ffb2-112">Przykład 1. Pobierz serwer MySql z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="2ffb2-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2ffb2-113">To polecenie cmdlet pobiera serwer MySql z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="2ffb2-114">Przykład 2. Uzyskiwanie serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="2ffb2-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2ffb2-115">To polecenie cmdlet pobiera serwer MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="2ffb2-116">Przykład 3. Lista wszystkich serwerów MySql w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="2ffb2-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2ffb2-117">To polecenie cmdlet wyświetla listę wszystkich serwerów MySql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="2ffb2-118">Przykład 4. Uzyskiwanie serwera MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="2ffb2-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2ffb2-119">Te listy polecenia cmdlet pobierają serwer MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="2ffb2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ffb2-120">PARAMETERS</span></span>

### <span data-ttu-id="2ffb2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffb2-121">-DefaultProfile</span></span>
<span data-ttu-id="2ffb2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ffb2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ffb2-123">-InputObject</span></span>
<span data-ttu-id="2ffb2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ffb2-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ffb2-125">-Name</span></span>
<span data-ttu-id="2ffb2-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-126">The name of the server.</span></span>

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

### <span data-ttu-id="2ffb2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffb2-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ffb2-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-128">The name of the resource group.</span></span>
<span data-ttu-id="2ffb2-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ffb2-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ffb2-130">-SubscriptionId</span></span>
<span data-ttu-id="2ffb2-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ffb2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffb2-132">CommonParameters</span></span>
<span data-ttu-id="2ffb2-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffb2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ffb2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffb2-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ffb2-135">INPUTS</span></span>

### <span data-ttu-id="2ffb2-136">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2ffb2-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2ffb2-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ffb2-137">OUTPUTS</span></span>

### <span data-ttu-id="2ffb2-138">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="2ffb2-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2ffb2-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ffb2-139">NOTES</span></span>

<span data-ttu-id="2ffb2-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2ffb2-140">ALIASES</span></span>

<span data-ttu-id="2ffb2-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ffb2-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ffb2-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ffb2-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ffb2-144">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2ffb2-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ffb2-145">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2ffb2-146">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2ffb2-147">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2ffb2-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2ffb2-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ffb2-149">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2ffb2-150">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2ffb2-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ffb2-152">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ffb2-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2ffb2-154">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2ffb2-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ffb2-156">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ffb2-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2ffb2-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ffb2-157">RELATED LINKS</span></span>

