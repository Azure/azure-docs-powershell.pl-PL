---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500770"
---
# <span data-ttu-id="21f77-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="21f77-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="21f77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21f77-102">SYNOPSIS</span></span>
<span data-ttu-id="21f77-103">Usuwa regułę sieci wirtualnej o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="21f77-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="21f77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21f77-104">SYNTAX</span></span>

### <span data-ttu-id="21f77-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="21f77-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="21f77-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21f77-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="21f77-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21f77-107">DESCRIPTION</span></span>
<span data-ttu-id="21f77-108">Usuwa regułę sieci wirtualnej o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="21f77-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="21f77-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21f77-109">EXAMPLES</span></span>

### <span data-ttu-id="21f77-110">Przykład 1: Usuwanie reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="21f77-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="21f77-111">To polecenie usuwa regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21f77-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="21f77-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21f77-112">PARAMETERS</span></span>

### <span data-ttu-id="21f77-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21f77-113">-AsJob</span></span>
<span data-ttu-id="21f77-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="21f77-114">Run the command as a job</span></span>

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

### <span data-ttu-id="21f77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f77-115">-DefaultProfile</span></span>
<span data-ttu-id="21f77-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21f77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f77-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21f77-117">-InputObject</span></span>
<span data-ttu-id="21f77-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="21f77-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21f77-119">-Name</span></span>
<span data-ttu-id="21f77-120">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21f77-120">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="21f77-121">-NoWait</span></span>
<span data-ttu-id="21f77-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="21f77-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="21f77-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21f77-123">-PassThru</span></span>
<span data-ttu-id="21f77-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="21f77-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="21f77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f77-125">-ResourceGroupName</span></span>
<span data-ttu-id="21f77-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="21f77-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="21f77-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="21f77-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="21f77-128">-ServerName</span></span>
<span data-ttu-id="21f77-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="21f77-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="21f77-130">-SubscriptionId</span></span>
<span data-ttu-id="21f77-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21f77-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21f77-132">-Confirm</span></span>
<span data-ttu-id="21f77-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f77-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f77-134">-WhatIf</span></span>
<span data-ttu-id="21f77-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f77-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21f77-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f77-137">CommonParameters</span></span>
<span data-ttu-id="21f77-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f77-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21f77-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f77-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21f77-140">INPUTS</span></span>

### <span data-ttu-id="21f77-141">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="21f77-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="21f77-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21f77-142">OUTPUTS</span></span>

### <span data-ttu-id="21f77-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21f77-143">System.Boolean</span></span>

## <span data-ttu-id="21f77-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21f77-144">NOTES</span></span>

<span data-ttu-id="21f77-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="21f77-145">ALIASES</span></span>

<span data-ttu-id="21f77-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21f77-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21f77-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="21f77-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21f77-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="21f77-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21f77-149">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="21f77-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21f77-150">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="21f77-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="21f77-151">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="21f77-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="21f77-152">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="21f77-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="21f77-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="21f77-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21f77-154">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="21f77-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="21f77-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="21f77-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="21f77-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="21f77-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="21f77-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="21f77-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="21f77-158">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="21f77-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="21f77-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21f77-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="21f77-160">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21f77-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="21f77-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21f77-161">RELATED LINKS</span></span>

