---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190242"
---
# <span data-ttu-id="bc166-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc166-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="bc166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc166-102">SYNOPSIS</span></span>
<span data-ttu-id="bc166-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc166-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="bc166-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc166-104">SYNTAX</span></span>

### <span data-ttu-id="bc166-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="bc166-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="bc166-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bc166-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="bc166-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc166-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="bc166-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc166-108">DESCRIPTION</span></span>
<span data-ttu-id="bc166-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc166-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="bc166-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc166-110">EXAMPLES</span></span>

### <span data-ttu-id="bc166-111">Przykład 1. Lista wszystkich reguł sieci wirtualnej w ramach bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="bc166-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="bc166-112">To polecenie wyświetla listę wszystkich reguł sieci wirtualnej w obszarze Bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bc166-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="bc166-113">Przykład 2. Uzyskiwanie reguły sieci wirtualnej w ramach bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="bc166-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="bc166-114">To polecenie pobiera regułę sieci wirtualnej w obszarze bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bc166-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="bc166-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc166-115">PARAMETERS</span></span>

### <span data-ttu-id="bc166-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc166-116">-DefaultProfile</span></span>
<span data-ttu-id="bc166-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc166-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc166-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc166-118">-InputObject</span></span>
<span data-ttu-id="bc166-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bc166-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc166-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc166-120">-Name</span></span>
<span data-ttu-id="bc166-121">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc166-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc166-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc166-122">-PassThru</span></span>
<span data-ttu-id="bc166-123">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bc166-123">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc166-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc166-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc166-125">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="bc166-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bc166-126">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bc166-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bc166-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc166-127">-ServerName</span></span>
<span data-ttu-id="bc166-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bc166-128">The name of the server.</span></span>

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

### <span data-ttu-id="bc166-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc166-129">-SubscriptionId</span></span>
<span data-ttu-id="bc166-130">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc166-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bc166-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc166-131">CommonParameters</span></span>
<span data-ttu-id="bc166-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc166-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc166-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc166-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc166-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc166-134">INPUTS</span></span>

### <span data-ttu-id="bc166-135">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="bc166-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="bc166-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc166-136">OUTPUTS</span></span>

### <span data-ttu-id="bc166-137">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc166-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="bc166-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc166-138">NOTES</span></span>

<span data-ttu-id="bc166-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bc166-139">ALIASES</span></span>

<span data-ttu-id="bc166-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bc166-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc166-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bc166-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc166-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc166-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc166-143">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bc166-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc166-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="bc166-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bc166-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bc166-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bc166-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bc166-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bc166-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bc166-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc166-148">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bc166-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bc166-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="bc166-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bc166-150">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bc166-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bc166-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bc166-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bc166-152">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bc166-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bc166-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc166-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="bc166-154">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bc166-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bc166-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc166-155">RELATED LINKS</span></span>

