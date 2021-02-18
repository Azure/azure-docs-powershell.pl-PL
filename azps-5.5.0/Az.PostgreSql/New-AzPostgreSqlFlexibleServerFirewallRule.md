---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e11a68066c0e481cddbbabe786b975c4cd7460b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193146"
---
# <span data-ttu-id="11dd0-101">New-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11dd0-101">New-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="11dd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="11dd0-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="11dd0-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="11dd0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11dd0-104">SYNTAX</span></span>

### <span data-ttu-id="11dd0-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="11dd0-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11dd0-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="11dd0-106">AllowAll</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11dd0-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="11dd0-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11dd0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11dd0-108">DESCRIPTION</span></span>
<span data-ttu-id="11dd0-109">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="11dd0-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="11dd0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11dd0-110">EXAMPLES</span></span>

### <span data-ttu-id="11dd0-111">Przykład 1. Tworzenie nowej reguły zapory serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="11dd0-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="11dd0-112">To polecenie cmdlet tworzy regułę zapory serwera PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="11dd0-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="11dd0-113">Przykład 2. Tworzenie nowej reguły zapory PostgreSql przy użyciu reguły -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="11dd0-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="11dd0-114">Te polecenia cmdlet tworzą regułę zapory PostgreSql przy użyciu reguły -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="11dd0-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="11dd0-115">Przykład 3. Tworzenie nowej reguły zapory pogresqlowej w celu umożliwienia wszystkim ip</span><span class="sxs-lookup"><span data-stu-id="11dd0-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="11dd0-116">To polecenie cmdlet tworzy nową regułę zapory postgresql, aby zezwolić na wszystkie ip.</span><span class="sxs-lookup"><span data-stu-id="11dd0-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="11dd0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11dd0-117">PARAMETERS</span></span>

### <span data-ttu-id="11dd0-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="11dd0-118">-AllowAll</span></span>
<span data-ttu-id="11dd0-119">Prezentuj, aby zezwolić na wszystkie zakresy adresów IP od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="11dd0-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="11dd0-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11dd0-120">-AsJob</span></span>
<span data-ttu-id="11dd0-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="11dd0-121">Run the command as a job</span></span>

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

### <span data-ttu-id="11dd0-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="11dd0-122">-ClientIPAddress</span></span>
<span data-ttu-id="11dd0-123">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="11dd0-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="11dd0-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="11dd0-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="11dd0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11dd0-125">-DefaultProfile</span></span>
<span data-ttu-id="11dd0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11dd0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11dd0-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="11dd0-127">-EndIPAddress</span></span>
<span data-ttu-id="11dd0-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="11dd0-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="11dd0-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="11dd0-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="11dd0-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11dd0-130">-Name</span></span>
<span data-ttu-id="11dd0-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="11dd0-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="11dd0-132">Jeśli nie zostanie określona, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="11dd0-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="11dd0-133">Jeśli jest obecna nazwa AllowAll, domyślną nazwą AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="11dd0-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="11dd0-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11dd0-134">-NoWait</span></span>
<span data-ttu-id="11dd0-135">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="11dd0-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11dd0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11dd0-136">-ResourceGroupName</span></span>
<span data-ttu-id="11dd0-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11dd0-137">The name of the resource group.</span></span>
<span data-ttu-id="11dd0-138">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="11dd0-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11dd0-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11dd0-139">-ServerName</span></span>
<span data-ttu-id="11dd0-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="11dd0-140">The name of the server.</span></span>

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

### <span data-ttu-id="11dd0-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="11dd0-141">-StartIPAddress</span></span>
<span data-ttu-id="11dd0-142">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="11dd0-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="11dd0-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="11dd0-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="11dd0-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11dd0-144">-SubscriptionId</span></span>
<span data-ttu-id="11dd0-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="11dd0-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11dd0-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11dd0-146">-Confirm</span></span>
<span data-ttu-id="11dd0-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11dd0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11dd0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11dd0-148">-WhatIf</span></span>
<span data-ttu-id="11dd0-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11dd0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11dd0-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11dd0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11dd0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11dd0-151">CommonParameters</span></span>
<span data-ttu-id="11dd0-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11dd0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11dd0-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11dd0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11dd0-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11dd0-154">INPUTS</span></span>

## <span data-ttu-id="11dd0-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11dd0-155">OUTPUTS</span></span>

### <span data-ttu-id="11dd0-156">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="11dd0-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="11dd0-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11dd0-157">NOTES</span></span>

<span data-ttu-id="11dd0-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="11dd0-158">ALIASES</span></span>

## <span data-ttu-id="11dd0-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11dd0-159">RELATED LINKS</span></span>

