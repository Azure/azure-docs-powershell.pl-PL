---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 67ef03656b97514d1d39ae72f0f0d52d5b302619
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180067"
---
# <span data-ttu-id="55c99-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55c99-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="55c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c99-102">SYNOPSIS</span></span>
<span data-ttu-id="55c99-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="55c99-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="55c99-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55c99-104">SYNTAX</span></span>

### <span data-ttu-id="55c99-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="55c99-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55c99-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="55c99-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55c99-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="55c99-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55c99-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="55c99-108">DESCRIPTION</span></span>
<span data-ttu-id="55c99-109">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="55c99-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="55c99-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55c99-110">EXAMPLES</span></span>

### <span data-ttu-id="55c99-111">Przykład 1. Tworzenie nowej reguły zapory serwera MySql</span><span class="sxs-lookup"><span data-stu-id="55c99-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="55c99-112">To polecenie cmdlet tworzy regułę zapory serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="55c99-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="55c99-113">Przykład 2. Tworzenie nowej reguły zapory MySql przy użyciu ciągu -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="55c99-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="55c99-114">Te polecenia cmdlet tworzą regułę zapory MySql przy użyciu clientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="55c99-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="55c99-115">Przykład 3. Tworzenie nowej reguły zapory MySql w celu zezwalania na wszystkie ip</span><span class="sxs-lookup"><span data-stu-id="55c99-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="55c99-116">To polecenie cmdlet tworzy nową regułę zapory mysql w celu zezwalania na wszystkie ip.</span><span class="sxs-lookup"><span data-stu-id="55c99-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="55c99-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55c99-117">PARAMETERS</span></span>

### <span data-ttu-id="55c99-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="55c99-118">-AllowAll</span></span>
<span data-ttu-id="55c99-119">Prezentuj, aby zezwolić na wszystkie zakresy adresów IP od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="55c99-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="55c99-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="55c99-120">-AsJob</span></span>
<span data-ttu-id="55c99-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="55c99-121">Run the command as a job</span></span>

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

### <span data-ttu-id="55c99-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="55c99-122">-ClientIPAddress</span></span>
<span data-ttu-id="55c99-123">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="55c99-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="55c99-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="55c99-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="55c99-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c99-125">-DefaultProfile</span></span>
<span data-ttu-id="55c99-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55c99-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c99-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="55c99-127">-EndIPAddress</span></span>
<span data-ttu-id="55c99-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="55c99-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="55c99-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="55c99-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="55c99-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55c99-130">-Name</span></span>
<span data-ttu-id="55c99-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="55c99-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="55c99-132">Jeśli nie zostanie określona, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="55c99-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="55c99-133">Jeśli jest obecna nazwa AllowAll, domyślną nazwą AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="55c99-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="55c99-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55c99-134">-NoWait</span></span>
<span data-ttu-id="55c99-135">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="55c99-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55c99-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c99-136">-ResourceGroupName</span></span>
<span data-ttu-id="55c99-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55c99-137">The name of the resource group.</span></span>
<span data-ttu-id="55c99-138">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="55c99-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55c99-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55c99-139">-ServerName</span></span>
<span data-ttu-id="55c99-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="55c99-140">The name of the server.</span></span>

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

### <span data-ttu-id="55c99-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="55c99-141">-StartIPAddress</span></span>
<span data-ttu-id="55c99-142">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="55c99-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="55c99-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="55c99-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="55c99-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55c99-144">-SubscriptionId</span></span>
<span data-ttu-id="55c99-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="55c99-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55c99-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55c99-146">-Confirm</span></span>
<span data-ttu-id="55c99-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="55c99-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c99-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c99-148">-WhatIf</span></span>
<span data-ttu-id="55c99-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c99-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c99-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="55c99-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c99-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c99-151">CommonParameters</span></span>
<span data-ttu-id="55c99-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c99-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c99-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55c99-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c99-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55c99-154">INPUTS</span></span>

## <span data-ttu-id="55c99-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55c99-155">OUTPUTS</span></span>

### <span data-ttu-id="55c99-156">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55c99-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="55c99-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55c99-157">NOTES</span></span>

<span data-ttu-id="55c99-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="55c99-158">ALIASES</span></span>

## <span data-ttu-id="55c99-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55c99-159">RELATED LINKS</span></span>

