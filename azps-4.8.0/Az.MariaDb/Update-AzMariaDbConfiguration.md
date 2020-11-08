---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222492"
---
# <span data-ttu-id="69313-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="69313-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="69313-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69313-102">SYNOPSIS</span></span>
<span data-ttu-id="69313-103">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="69313-104">Zamiast tego użyj Update-AzMariaDbServer, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="69313-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="69313-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69313-105">SYNTAX</span></span>

### <span data-ttu-id="69313-106">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69313-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69313-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69313-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69313-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69313-108">DESCRIPTION</span></span>
<span data-ttu-id="69313-109">Umożliwia zaktualizowanie konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="69313-110">Zamiast tego użyj Update-AzMariaDberver, jeśli chcesz zaktualizować AdministratorLoginPassword, SKU itd.</span><span class="sxs-lookup"><span data-stu-id="69313-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="69313-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69313-111">EXAMPLES</span></span>

### <span data-ttu-id="69313-112">Przykład 1: aktualizowanie konfiguracji MariaDB</span><span class="sxs-lookup"><span data-stu-id="69313-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="69313-113">To polecenie aktualizuje konfigurację MariaDB.</span><span class="sxs-lookup"><span data-stu-id="69313-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="69313-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69313-114">PARAMETERS</span></span>

### <span data-ttu-id="69313-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69313-115">-AsJob</span></span>
<span data-ttu-id="69313-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="69313-116">Run the command as a job</span></span>

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

### <span data-ttu-id="69313-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69313-117">-DefaultProfile</span></span>
<span data-ttu-id="69313-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69313-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69313-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69313-119">-InputObject</span></span>
<span data-ttu-id="69313-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="69313-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69313-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69313-121">-Name</span></span>
<span data-ttu-id="69313-122">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="69313-123">-NoWait</span></span>
<span data-ttu-id="69313-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="69313-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69313-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69313-125">-ResourceGroupName</span></span>
<span data-ttu-id="69313-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="69313-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="69313-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="69313-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="69313-128">-ServerName</span></span>
<span data-ttu-id="69313-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-130">-Source</span><span class="sxs-lookup"><span data-stu-id="69313-130">-Source</span></span>
<span data-ttu-id="69313-131">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="69313-131">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="69313-132">-SubscriptionId</span></span>
<span data-ttu-id="69313-133">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69313-133">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-134">-Value</span><span class="sxs-lookup"><span data-stu-id="69313-134">-Value</span></span>
<span data-ttu-id="69313-135">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="69313-135">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69313-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69313-136">-Confirm</span></span>
<span data-ttu-id="69313-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69313-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69313-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69313-138">-WhatIf</span></span>
<span data-ttu-id="69313-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69313-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69313-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69313-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69313-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69313-141">CommonParameters</span></span>
<span data-ttu-id="69313-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69313-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69313-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69313-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69313-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69313-144">INPUTS</span></span>

### <span data-ttu-id="69313-145">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="69313-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="69313-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69313-146">OUTPUTS</span></span>

### <span data-ttu-id="69313-147">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="69313-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="69313-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69313-148">NOTES</span></span>

<span data-ttu-id="69313-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="69313-149">ALIASES</span></span>

<span data-ttu-id="69313-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69313-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69313-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="69313-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69313-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69313-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69313-153">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="69313-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69313-154">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="69313-155">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="69313-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="69313-156">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="69313-157">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="69313-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69313-158">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="69313-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="69313-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="69313-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="69313-160">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="69313-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="69313-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="69313-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="69313-162">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="69313-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="69313-163">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69313-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="69313-164">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69313-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="69313-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69313-165">RELATED LINKS</span></span>

