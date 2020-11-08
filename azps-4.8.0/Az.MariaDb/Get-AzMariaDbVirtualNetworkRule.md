---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220775"
---
# <span data-ttu-id="957d3-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="957d3-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="957d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="957d3-102">SYNOPSIS</span></span>
<span data-ttu-id="957d3-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="957d3-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="957d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="957d3-104">SYNTAX</span></span>

### <span data-ttu-id="957d3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="957d3-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="957d3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="957d3-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="957d3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="957d3-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="957d3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="957d3-108">DESCRIPTION</span></span>
<span data-ttu-id="957d3-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="957d3-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="957d3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="957d3-110">EXAMPLES</span></span>

### <span data-ttu-id="957d3-111">Przykład 1: Lista wszystkich reguł sieci wirtualnej w obszarze MariaDB</span><span class="sxs-lookup"><span data-stu-id="957d3-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="957d3-112">To polecenie wyświetla listę wszystkich reguł sieci wirtualnej pod MariaDB.</span><span class="sxs-lookup"><span data-stu-id="957d3-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="957d3-113">Przykład 2: Pobierz regułę sieci wirtualnej pod MariaDB</span><span class="sxs-lookup"><span data-stu-id="957d3-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="957d3-114">To polecenie pobiera regułę sieci wirtualnej pod MariaDB.</span><span class="sxs-lookup"><span data-stu-id="957d3-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="957d3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="957d3-115">PARAMETERS</span></span>

### <span data-ttu-id="957d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957d3-116">-DefaultProfile</span></span>
<span data-ttu-id="957d3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="957d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="957d3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="957d3-118">-InputObject</span></span>
<span data-ttu-id="957d3-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="957d3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="957d3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="957d3-120">-Name</span></span>
<span data-ttu-id="957d3-121">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="957d3-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="957d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="957d3-122">-PassThru</span></span>
<span data-ttu-id="957d3-123">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="957d3-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="957d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="957d3-125">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="957d3-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="957d3-126">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="957d3-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="957d3-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="957d3-127">-ServerName</span></span>
<span data-ttu-id="957d3-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="957d3-128">The name of the server.</span></span>

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

### <span data-ttu-id="957d3-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="957d3-129">-SubscriptionId</span></span>
<span data-ttu-id="957d3-130">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="957d3-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="957d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957d3-131">CommonParameters</span></span>
<span data-ttu-id="957d3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957d3-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="957d3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957d3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="957d3-134">INPUTS</span></span>

### <span data-ttu-id="957d3-135">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="957d3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="957d3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="957d3-136">OUTPUTS</span></span>

### <span data-ttu-id="957d3-137">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="957d3-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="957d3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="957d3-138">NOTES</span></span>

<span data-ttu-id="957d3-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="957d3-139">ALIASES</span></span>

<span data-ttu-id="957d3-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="957d3-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="957d3-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="957d3-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="957d3-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="957d3-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="957d3-143">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="957d3-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="957d3-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="957d3-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="957d3-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="957d3-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="957d3-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="957d3-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="957d3-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="957d3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="957d3-148">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="957d3-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="957d3-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="957d3-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="957d3-150">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="957d3-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="957d3-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="957d3-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="957d3-152">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="957d3-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="957d3-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="957d3-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="957d3-154">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="957d3-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="957d3-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="957d3-155">RELATED LINKS</span></span>

