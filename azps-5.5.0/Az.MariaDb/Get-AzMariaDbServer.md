---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190235"
---
# <span data-ttu-id="ff851-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ff851-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="ff851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff851-102">SYNOPSIS</span></span>
<span data-ttu-id="ff851-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="ff851-103">Gets information about a server.</span></span>

## <span data-ttu-id="ff851-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff851-104">SYNTAX</span></span>

### <span data-ttu-id="ff851-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ff851-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff851-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ff851-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff851-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff851-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff851-108">Lista</span><span class="sxs-lookup"><span data-stu-id="ff851-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff851-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff851-109">DESCRIPTION</span></span>
<span data-ttu-id="ff851-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="ff851-110">Gets information about a server.</span></span>

## <span data-ttu-id="ff851-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff851-111">EXAMPLES</span></span>

### <span data-ttu-id="ff851-112">Przykład 1. Lista wszystkich plików MariaDB w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff851-112">Example 1: List all MariaDB under a subscriptions</span></span>
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

<span data-ttu-id="ff851-113">To polecenie wyświetla listę wszystkich baz danych MariaDB w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ff851-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="ff851-114">Przykład 2. Lista wszystkich plików MariaDB w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ff851-114">Example 2: List all MariaDB under a resource group</span></span>
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

<span data-ttu-id="ff851-115">To polecenie wyświetla listę wszystkich danych MariaDB w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff851-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="ff851-116">Przykład 3. Uzyskiwanie bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="ff851-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="ff851-117">To polecenie pobiera plik MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ff851-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="ff851-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff851-118">PARAMETERS</span></span>

### <span data-ttu-id="ff851-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff851-119">-DefaultProfile</span></span>
<span data-ttu-id="ff851-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff851-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff851-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff851-121">-InputObject</span></span>
<span data-ttu-id="ff851-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ff851-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff851-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff851-123">-Name</span></span>
<span data-ttu-id="ff851-124">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ff851-124">The name of the server.</span></span>

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

### <span data-ttu-id="ff851-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff851-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff851-126">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ff851-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ff851-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ff851-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff851-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff851-128">-SubscriptionId</span></span>
<span data-ttu-id="ff851-129">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff851-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ff851-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff851-130">CommonParameters</span></span>
<span data-ttu-id="ff851-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff851-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff851-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff851-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff851-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff851-133">INPUTS</span></span>

### <span data-ttu-id="ff851-134">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ff851-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ff851-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff851-135">OUTPUTS</span></span>

### <span data-ttu-id="ff851-136">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ff851-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ff851-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff851-137">NOTES</span></span>

<span data-ttu-id="ff851-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ff851-138">ALIASES</span></span>

<span data-ttu-id="ff851-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff851-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff851-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ff851-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff851-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff851-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff851-142">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ff851-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff851-143">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff851-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ff851-144">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ff851-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ff851-145">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ff851-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ff851-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ff851-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff851-147">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ff851-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ff851-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ff851-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ff851-149">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ff851-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ff851-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ff851-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ff851-151">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ff851-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ff851-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff851-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ff851-153">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff851-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ff851-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff851-154">RELATED LINKS</span></span>

