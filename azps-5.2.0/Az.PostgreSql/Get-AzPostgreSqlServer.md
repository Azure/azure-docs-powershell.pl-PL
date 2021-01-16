---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363092"
---
# <span data-ttu-id="7459e-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="7459e-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="7459e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7459e-102">SYNOPSIS</span></span>
<span data-ttu-id="7459e-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="7459e-103">Gets information about a server.</span></span>

## <span data-ttu-id="7459e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7459e-104">SYNTAX</span></span>

### <span data-ttu-id="7459e-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7459e-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7459e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7459e-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7459e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7459e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7459e-108">Lista</span><span class="sxs-lookup"><span data-stu-id="7459e-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7459e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7459e-109">DESCRIPTION</span></span>
<span data-ttu-id="7459e-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="7459e-110">Gets information about a server.</span></span>

## <span data-ttu-id="7459e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7459e-111">EXAMPLES</span></span>

### <span data-ttu-id="7459e-112">Przykład 1: Uzyskaj PostgreSql serwer z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="7459e-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7459e-113">To polecenie cmdlet umożliwia pobieranie serwera PostgreSql z domyślnym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="7459e-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="7459e-114">Przykład 2: Uzyskaj PostgreSql serwer na podstawie grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="7459e-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7459e-115">To polecenie cmdlet pobiera serwer PostgreSql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="7459e-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="7459e-116">Przykład 3: Wyświetla listę wszystkich serwerów PostgreSql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7459e-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7459e-117">To polecenie cmdlet wyświetla listę wszystkich serwerów PostgreSql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7459e-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="7459e-118">Przykład 4: uzyskiwanie serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="7459e-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7459e-119">Te listy poleceń cmdlet uzyskują PostgreSql serwer na podstawie tożsamości.</span><span class="sxs-lookup"><span data-stu-id="7459e-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="7459e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7459e-120">PARAMETERS</span></span>

### <span data-ttu-id="7459e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7459e-121">-DefaultProfile</span></span>
<span data-ttu-id="7459e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7459e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7459e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7459e-123">-InputObject</span></span>
<span data-ttu-id="7459e-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7459e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7459e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7459e-125">-Name</span></span>
<span data-ttu-id="7459e-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7459e-126">The name of the server.</span></span>

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

### <span data-ttu-id="7459e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7459e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7459e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7459e-128">The name of the resource group.</span></span>
<span data-ttu-id="7459e-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7459e-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7459e-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7459e-130">-SubscriptionId</span></span>
<span data-ttu-id="7459e-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7459e-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7459e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7459e-132">CommonParameters</span></span>
<span data-ttu-id="7459e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7459e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7459e-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7459e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7459e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7459e-135">INPUTS</span></span>

### <span data-ttu-id="7459e-136">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7459e-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7459e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7459e-137">OUTPUTS</span></span>

### <span data-ttu-id="7459e-138">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="7459e-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7459e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7459e-139">NOTES</span></span>

<span data-ttu-id="7459e-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7459e-140">ALIASES</span></span>

<span data-ttu-id="7459e-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7459e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7459e-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7459e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7459e-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7459e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7459e-144">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7459e-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7459e-145">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="7459e-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7459e-146">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7459e-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7459e-147">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="7459e-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7459e-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7459e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7459e-149">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7459e-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7459e-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7459e-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7459e-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7459e-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="7459e-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7459e-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7459e-153">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7459e-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7459e-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7459e-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7459e-155">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7459e-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7459e-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7459e-156">RELATED LINKS</span></span>

