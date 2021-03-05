---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 718443cc31972f1d1d53a5b5802dc50c1ac31df0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982321"
---
# <span data-ttu-id="ec119-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec119-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="ec119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec119-102">SYNOPSIS</span></span>
<span data-ttu-id="ec119-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="ec119-103">Gets information about a server.</span></span>

## <span data-ttu-id="ec119-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec119-104">SYNTAX</span></span>

### <span data-ttu-id="ec119-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ec119-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec119-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ec119-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec119-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec119-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec119-108">Lista</span><span class="sxs-lookup"><span data-stu-id="ec119-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec119-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec119-109">DESCRIPTION</span></span>
<span data-ttu-id="ec119-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="ec119-110">Gets information about a server.</span></span>

## <span data-ttu-id="ec119-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec119-111">EXAMPLES</span></span>

### <span data-ttu-id="ec119-112">Przykład 1. Uzyskiwanie serwera PostgreSql z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="ec119-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ec119-113">To polecenie cmdlet pobiera serwer PostgreSql z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="ec119-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="ec119-114">Przykład 2. Uzyskiwanie serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="ec119-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ec119-115">To polecenie cmdlet pobiera serwer PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="ec119-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="ec119-116">Przykład 3. Lista wszystkich serwerów PostgreSql w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ec119-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ec119-117">To polecenie cmdlet wyświetla listę wszystkich serwerów PostgreSql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec119-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="ec119-118">Przykład 4. Uzyskiwanie serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec119-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ec119-119">Te listy polecenia cmdlet pobierają serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ec119-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="ec119-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec119-120">PARAMETERS</span></span>

### <span data-ttu-id="ec119-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec119-121">-DefaultProfile</span></span>
<span data-ttu-id="ec119-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec119-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec119-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec119-123">-InputObject</span></span>
<span data-ttu-id="ec119-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ec119-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec119-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec119-125">-Name</span></span>
<span data-ttu-id="ec119-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ec119-126">The name of the server.</span></span>

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

### <span data-ttu-id="ec119-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec119-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec119-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec119-128">The name of the resource group.</span></span>
<span data-ttu-id="ec119-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ec119-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec119-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec119-130">-SubscriptionId</span></span>
<span data-ttu-id="ec119-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ec119-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ec119-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec119-132">CommonParameters</span></span>
<span data-ttu-id="ec119-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec119-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec119-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec119-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec119-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec119-135">INPUTS</span></span>

### <span data-ttu-id="ec119-136">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ec119-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ec119-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec119-137">OUTPUTS</span></span>

### <span data-ttu-id="ec119-138">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ec119-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ec119-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec119-139">NOTES</span></span>

<span data-ttu-id="ec119-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ec119-140">ALIASES</span></span>

<span data-ttu-id="ec119-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec119-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec119-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ec119-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec119-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec119-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec119-144">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ec119-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec119-145">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ec119-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ec119-146">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ec119-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ec119-147">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ec119-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ec119-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ec119-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec119-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec119-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ec119-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec119-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ec119-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ec119-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="ec119-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ec119-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ec119-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ec119-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ec119-154">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ec119-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ec119-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ec119-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ec119-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec119-156">RELATED LINKS</span></span>

