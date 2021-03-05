---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e06447fc72dc8dc3bc09768360039a561b1b862a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995443"
---
# <span data-ttu-id="6e65b-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e65b-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="6e65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e65b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e65b-103">Tworzy nową regułę zapory dla serwera elastycznego MySQL</span><span class="sxs-lookup"><span data-stu-id="6e65b-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="6e65b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6e65b-104">SYNTAX</span></span>

### <span data-ttu-id="6e65b-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="6e65b-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e65b-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="6e65b-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e65b-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e65b-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e65b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6e65b-108">DESCRIPTION</span></span>
<span data-ttu-id="6e65b-109">Tworzy nową regułę zapory dla serwera elastycznego MySQL</span><span class="sxs-lookup"><span data-stu-id="6e65b-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="6e65b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6e65b-110">EXAMPLES</span></span>

### <span data-ttu-id="6e65b-111">Przykład 1. Tworzenie nowej reguły zapory serwera MySql</span><span class="sxs-lookup"><span data-stu-id="6e65b-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="6e65b-112">To polecenie cmdlet tworzy regułę zapory serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="6e65b-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="6e65b-113">Przykład 2. Tworzenie nowej reguły zapory MySql przy użyciu ciągu -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6e65b-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="6e65b-114">Te polecenia cmdlet tworzą regułę zapory MySql przy użyciu clientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6e65b-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="6e65b-115">Przykład 3. Tworzenie nowej reguły zapory mysql w celu zezwalania na wszystkie ip</span><span class="sxs-lookup"><span data-stu-id="6e65b-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="6e65b-116">To polecenie cmdlet tworzy nową regułę zapory mysql, aby zezwolić na wszystkie ip.</span><span class="sxs-lookup"><span data-stu-id="6e65b-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="6e65b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e65b-117">PARAMETERS</span></span>

### <span data-ttu-id="6e65b-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="6e65b-118">-AllowAll</span></span>
<span data-ttu-id="6e65b-119">Prezentuj, aby zezwolić na wszystkie zakresy adresów IP od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="6e65b-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="6e65b-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6e65b-120">-AsJob</span></span>
<span data-ttu-id="6e65b-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6e65b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6e65b-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e65b-122">-ClientIPAddress</span></span>
<span data-ttu-id="6e65b-123">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6e65b-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6e65b-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e65b-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e65b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e65b-125">-DefaultProfile</span></span>
<span data-ttu-id="6e65b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e65b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e65b-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e65b-127">-EndIPAddress</span></span>
<span data-ttu-id="6e65b-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6e65b-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6e65b-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e65b-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e65b-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6e65b-130">-Name</span></span>
<span data-ttu-id="6e65b-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6e65b-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="6e65b-132">Jeśli nie zostanie określona, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="6e65b-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="6e65b-133">Jeśli jest obecna nazwa AllowAll, domyślną nazwą AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="6e65b-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="6e65b-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6e65b-134">-NoWait</span></span>
<span data-ttu-id="6e65b-135">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6e65b-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e65b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e65b-136">-ResourceGroupName</span></span>
<span data-ttu-id="6e65b-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e65b-137">The name of the resource group.</span></span>
<span data-ttu-id="6e65b-138">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6e65b-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6e65b-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e65b-139">-ServerName</span></span>
<span data-ttu-id="6e65b-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="6e65b-140">The name of the server.</span></span>

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

### <span data-ttu-id="6e65b-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e65b-141">-StartIPAddress</span></span>
<span data-ttu-id="6e65b-142">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6e65b-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6e65b-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e65b-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e65b-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e65b-144">-SubscriptionId</span></span>
<span data-ttu-id="6e65b-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6e65b-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6e65b-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e65b-146">-Confirm</span></span>
<span data-ttu-id="6e65b-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6e65b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e65b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e65b-148">-WhatIf</span></span>
<span data-ttu-id="6e65b-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e65b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e65b-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6e65b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e65b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e65b-151">CommonParameters</span></span>
<span data-ttu-id="6e65b-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e65b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e65b-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e65b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e65b-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e65b-154">INPUTS</span></span>

## <span data-ttu-id="6e65b-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e65b-155">OUTPUTS</span></span>

### <span data-ttu-id="6e65b-156">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e65b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="6e65b-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6e65b-157">NOTES</span></span>

<span data-ttu-id="6e65b-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6e65b-158">ALIASES</span></span>

## <span data-ttu-id="6e65b-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e65b-159">RELATED LINKS</span></span>

