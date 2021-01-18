---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500777"
---
# <span data-ttu-id="d1dc4-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d1dc4-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="d1dc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1dc4-103">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-103">Deletes a server.</span></span>

## <span data-ttu-id="d1dc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1dc4-104">SYNTAX</span></span>

### <span data-ttu-id="d1dc4-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d1dc4-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1dc4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1dc4-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1dc4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="d1dc4-108">Usuwa serwer.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-108">Deletes a server.</span></span>

## <span data-ttu-id="d1dc4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1dc4-109">EXAMPLES</span></span>

### <span data-ttu-id="d1dc4-110">Przykład 1: usuwanie MariaDB</span><span class="sxs-lookup"><span data-stu-id="d1dc4-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="d1dc4-111">To polecenie usuwa MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="d1dc4-112">Przykład 2: usuwanie MariaDB</span><span class="sxs-lookup"><span data-stu-id="d1dc4-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="d1dc4-113">To polecenie usuwa MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="d1dc4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1dc4-114">PARAMETERS</span></span>

### <span data-ttu-id="d1dc4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1dc4-115">-AsJob</span></span>
<span data-ttu-id="d1dc4-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d1dc4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d1dc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1dc4-117">-DefaultProfile</span></span>
<span data-ttu-id="d1dc4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1dc4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1dc4-119">-InputObject</span></span>
<span data-ttu-id="d1dc4-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1dc4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1dc4-121">-Name</span></span>
<span data-ttu-id="d1dc4-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc4-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d1dc4-123">-NoWait</span></span>
<span data-ttu-id="d1dc4-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d1dc4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1dc4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1dc4-125">-PassThru</span></span>
<span data-ttu-id="d1dc4-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d1dc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1dc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1dc4-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d1dc4-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d1dc4-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d1dc4-130">-SubscriptionId</span></span>
<span data-ttu-id="d1dc4-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d1dc4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1dc4-132">-Confirm</span></span>
<span data-ttu-id="d1dc4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1dc4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1dc4-134">-WhatIf</span></span>
<span data-ttu-id="d1dc4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1dc4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1dc4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1dc4-137">CommonParameters</span></span>
<span data-ttu-id="d1dc4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1dc4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1dc4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1dc4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1dc4-140">INPUTS</span></span>

### <span data-ttu-id="d1dc4-141">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d1dc4-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d1dc4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1dc4-142">OUTPUTS</span></span>

### <span data-ttu-id="d1dc4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1dc4-143">System.Boolean</span></span>

## <span data-ttu-id="d1dc4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1dc4-144">NOTES</span></span>

<span data-ttu-id="d1dc4-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d1dc4-145">ALIASES</span></span>

<span data-ttu-id="d1dc4-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1dc4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1dc4-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1dc4-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1dc4-149">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d1dc4-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1dc4-150">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1dc4-151">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1dc4-152">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1dc4-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d1dc4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1dc4-154">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1dc4-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d1dc4-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d1dc4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1dc4-158">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1dc4-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d1dc4-160">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1dc4-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1dc4-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1dc4-161">RELATED LINKS</span></span>

