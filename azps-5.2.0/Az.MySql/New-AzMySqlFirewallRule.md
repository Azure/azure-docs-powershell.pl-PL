---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 67ef03656b97514d1d39ae72f0f0d52d5b302619
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336346"
---
# <span data-ttu-id="0350f-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0350f-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="0350f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0350f-102">SYNOPSIS</span></span>
<span data-ttu-id="0350f-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0350f-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0350f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0350f-104">SYNTAX</span></span>

### <span data-ttu-id="0350f-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0350f-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0350f-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="0350f-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0350f-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0350f-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0350f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0350f-108">DESCRIPTION</span></span>
<span data-ttu-id="0350f-109">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0350f-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0350f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0350f-110">EXAMPLES</span></span>

### <span data-ttu-id="0350f-111">Przykład 1. Tworzenie nowej reguły zapory serwera MySql</span><span class="sxs-lookup"><span data-stu-id="0350f-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0350f-112">Te polecenia cmdlet tworzą regułę zapory serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="0350f-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="0350f-113">Przykład 2: Tworzenie nowej reguły zapory MySql przy użyciu polecenia-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0350f-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="0350f-114">Te polecenia cmdlet tworzą regułę zapory MySql przy użyciu funkcji-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0350f-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="0350f-115">Przykład 3: Tworzenie nowej reguły zapory MySql w celu umożliwienia obsługi wszystkich adresów IP</span><span class="sxs-lookup"><span data-stu-id="0350f-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="0350f-116">Te polecenia cmdlet umożliwiają utworzenie nowej reguły zapory MySql w celu umożliwienia obsługi wszystkich adresów IP.</span><span class="sxs-lookup"><span data-stu-id="0350f-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="0350f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0350f-117">PARAMETERS</span></span>

### <span data-ttu-id="0350f-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="0350f-118">-AllowAll</span></span>
<span data-ttu-id="0350f-119">Prezentuj, aby zezwolić na wszystkie adresy IP zakresu od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="0350f-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="0350f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0350f-120">-AsJob</span></span>
<span data-ttu-id="0350f-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0350f-121">Run the command as a job</span></span>

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

### <span data-ttu-id="0350f-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0350f-122">-ClientIPAddress</span></span>
<span data-ttu-id="0350f-123">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0350f-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0350f-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0350f-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0350f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0350f-125">-DefaultProfile</span></span>
<span data-ttu-id="0350f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0350f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0350f-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="0350f-127">-EndIPAddress</span></span>
<span data-ttu-id="0350f-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0350f-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0350f-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0350f-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0350f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0350f-130">-Name</span></span>
<span data-ttu-id="0350f-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0350f-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="0350f-132">Jeśli nie określono tego parametru, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="0350f-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="0350f-133">Jeśli AllowAll jest obecny, nazwa domyślna to AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="0350f-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="0350f-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0350f-134">-NoWait</span></span>
<span data-ttu-id="0350f-135">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0350f-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0350f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0350f-136">-ResourceGroupName</span></span>
<span data-ttu-id="0350f-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0350f-137">The name of the resource group.</span></span>
<span data-ttu-id="0350f-138">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0350f-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0350f-139">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0350f-139">-ServerName</span></span>
<span data-ttu-id="0350f-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0350f-140">The name of the server.</span></span>

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

### <span data-ttu-id="0350f-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0350f-141">-StartIPAddress</span></span>
<span data-ttu-id="0350f-142">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0350f-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0350f-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0350f-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0350f-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0350f-144">-SubscriptionId</span></span>
<span data-ttu-id="0350f-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0350f-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0350f-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0350f-146">-Confirm</span></span>
<span data-ttu-id="0350f-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0350f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0350f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0350f-148">-WhatIf</span></span>
<span data-ttu-id="0350f-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0350f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0350f-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0350f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0350f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0350f-151">CommonParameters</span></span>
<span data-ttu-id="0350f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0350f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0350f-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0350f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0350f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0350f-154">INPUTS</span></span>

## <span data-ttu-id="0350f-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0350f-155">OUTPUTS</span></span>

### <span data-ttu-id="0350f-156">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0350f-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0350f-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0350f-157">NOTES</span></span>

<span data-ttu-id="0350f-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0350f-158">ALIASES</span></span>

## <span data-ttu-id="0350f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0350f-159">RELATED LINKS</span></span>

