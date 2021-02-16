---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190226"
---
# <span data-ttu-id="5cef1-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cef1-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="5cef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cef1-102">SYNOPSIS</span></span>
<span data-ttu-id="5cef1-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="5cef1-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5cef1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5cef1-104">SYNTAX</span></span>

### <span data-ttu-id="5cef1-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="5cef1-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5cef1-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5cef1-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5cef1-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cef1-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cef1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5cef1-108">DESCRIPTION</span></span>
<span data-ttu-id="5cef1-109">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="5cef1-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5cef1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5cef1-110">EXAMPLES</span></span>

### <span data-ttu-id="5cef1-111">Przykład 1. Tworzenie reguły zapory w obszarze bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="5cef1-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="5cef1-112">To polecenie tworzy regułę zapory w obszarze bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5cef1-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="5cef1-113">Przykład 2. Tworzenie nowej reguły zapory MariaDB przy użyciu ciągu -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5cef1-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5cef1-114">Te polecenia cmdlet tworzą regułę zapory MariaDB przy użyciu -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5cef1-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5cef1-115">Przykład 3. Tworzenie nowej reguły zapory MariaDB w celu zezwalania na wszystkie ip</span><span class="sxs-lookup"><span data-stu-id="5cef1-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5cef1-116">To polecenie cmdlet tworzy nową regułę zapory MariaDB, aby zezwolić na wszystkie ip.</span><span class="sxs-lookup"><span data-stu-id="5cef1-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5cef1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cef1-117">PARAMETERS</span></span>

### <span data-ttu-id="5cef1-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5cef1-118">-AllowAll</span></span>
<span data-ttu-id="5cef1-119">Prezentuj, aby zezwolić na wszystkie zakresy adresów IP od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="5cef1-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5cef1-120">-AsJob</span></span>
<span data-ttu-id="5cef1-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5cef1-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5cef1-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cef1-122">-ClientIPAddress</span></span>
<span data-ttu-id="5cef1-123">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="5cef1-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5cef1-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="5cef1-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cef1-125">-DefaultProfile</span></span>
<span data-ttu-id="5cef1-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cef1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cef1-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cef1-127">-EndIPAddress</span></span>
<span data-ttu-id="5cef1-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="5cef1-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5cef1-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="5cef1-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5cef1-130">-Name</span></span>
<span data-ttu-id="5cef1-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="5cef1-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="5cef1-132">Jeśli nie zostanie określona, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="5cef1-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="5cef1-133">Jeśli jest obecna nazwa AllowAll, domyślną nazwą AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="5cef1-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5cef1-134">-NoWait</span></span>
<span data-ttu-id="5cef1-135">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5cef1-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cef1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cef1-136">-ResourceGroupName</span></span>
<span data-ttu-id="5cef1-137">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="5cef1-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5cef1-138">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5cef1-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cef1-139">-ServerName</span></span>
<span data-ttu-id="5cef1-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="5cef1-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5cef1-141">-StartIPAddress</span></span>
<span data-ttu-id="5cef1-142">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="5cef1-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5cef1-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="5cef1-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cef1-144">-SubscriptionId</span></span>
<span data-ttu-id="5cef1-145">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5cef1-145">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef1-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cef1-146">-Confirm</span></span>
<span data-ttu-id="5cef1-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5cef1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cef1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cef1-148">-WhatIf</span></span>
<span data-ttu-id="5cef1-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cef1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cef1-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5cef1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cef1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cef1-151">CommonParameters</span></span>
<span data-ttu-id="5cef1-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cef1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cef1-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cef1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cef1-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cef1-154">INPUTS</span></span>

## <span data-ttu-id="5cef1-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cef1-155">OUTPUTS</span></span>

### <span data-ttu-id="5cef1-156">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cef1-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="5cef1-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5cef1-157">NOTES</span></span>

<span data-ttu-id="5cef1-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5cef1-158">ALIASES</span></span>

## <span data-ttu-id="5cef1-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cef1-159">RELATED LINKS</span></span>

