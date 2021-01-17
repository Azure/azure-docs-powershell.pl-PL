---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324105"
---
# <span data-ttu-id="88b4c-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="88b4c-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="88b4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="88b4c-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="88b4c-103">Gets information about a server.</span></span>

## <span data-ttu-id="88b4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88b4c-104">SYNTAX</span></span>

### <span data-ttu-id="88b4c-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88b4c-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88b4c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="88b4c-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88b4c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88b4c-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88b4c-108">Lista</span><span class="sxs-lookup"><span data-stu-id="88b4c-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="88b4c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="88b4c-109">DESCRIPTION</span></span>
<span data-ttu-id="88b4c-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="88b4c-110">Gets information about a server.</span></span>

## <span data-ttu-id="88b4c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88b4c-111">EXAMPLES</span></span>

### <span data-ttu-id="88b4c-112">Przykład 1: wyświetlanie wszystkich MariaDB w obszarze abonamentów</span><span class="sxs-lookup"><span data-stu-id="88b4c-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="88b4c-113">To polecenie wyświetla listę wszystkich MariaDB w obszarze abonamentów.</span><span class="sxs-lookup"><span data-stu-id="88b4c-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="88b4c-114">Przykład 2: Lista wszystkich MariaDB w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="88b4c-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="88b4c-115">To polecenie wyświetla listę wszystkich MariaDB w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="88b4c-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="88b4c-116">Przykład 3: uzyskiwanie MariaDB</span><span class="sxs-lookup"><span data-stu-id="88b4c-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="88b4c-117">To polecenie pobiera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="88b4c-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="88b4c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88b4c-118">PARAMETERS</span></span>

### <span data-ttu-id="88b4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b4c-119">-DefaultProfile</span></span>
<span data-ttu-id="88b4c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88b4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b4c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88b4c-121">-InputObject</span></span>
<span data-ttu-id="88b4c-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="88b4c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88b4c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88b4c-123">-Name</span></span>
<span data-ttu-id="88b4c-124">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="88b4c-124">The name of the server.</span></span>

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

### <span data-ttu-id="88b4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="88b4c-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="88b4c-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="88b4c-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="88b4c-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="88b4c-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="88b4c-128">-SubscriptionId</span></span>
<span data-ttu-id="88b4c-129">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88b4c-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="88b4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b4c-130">CommonParameters</span></span>
<span data-ttu-id="88b4c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b4c-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b4c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b4c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88b4c-133">INPUTS</span></span>

### <span data-ttu-id="88b4c-134">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="88b4c-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="88b4c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88b4c-135">OUTPUTS</span></span>

### <span data-ttu-id="88b4c-136">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="88b4c-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="88b4c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88b4c-137">NOTES</span></span>

<span data-ttu-id="88b4c-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="88b4c-138">ALIASES</span></span>

<span data-ttu-id="88b4c-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88b4c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88b4c-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="88b4c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88b4c-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88b4c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88b4c-142">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="88b4c-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88b4c-143">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="88b4c-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="88b4c-144">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="88b4c-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="88b4c-145">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="88b4c-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="88b4c-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="88b4c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88b4c-147">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="88b4c-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="88b4c-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="88b4c-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="88b4c-149">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="88b4c-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="88b4c-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="88b4c-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="88b4c-151">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="88b4c-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="88b4c-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88b4c-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="88b4c-153">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88b4c-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="88b4c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88b4c-154">RELATED LINKS</span></span>

