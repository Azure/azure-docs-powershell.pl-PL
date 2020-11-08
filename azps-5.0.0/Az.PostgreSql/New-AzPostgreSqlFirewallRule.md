---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232040"
---
# <span data-ttu-id="342cc-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="342cc-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="342cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="342cc-102">SYNOPSIS</span></span>
<span data-ttu-id="342cc-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="342cc-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="342cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="342cc-104">SYNTAX</span></span>

### <span data-ttu-id="342cc-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="342cc-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="342cc-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="342cc-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="342cc-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="342cc-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="342cc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="342cc-108">DESCRIPTION</span></span>
<span data-ttu-id="342cc-109">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="342cc-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="342cc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="342cc-110">EXAMPLES</span></span>

### <span data-ttu-id="342cc-111">Przykład 1: Tworzenie nowej reguły zapory serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="342cc-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="342cc-112">Te polecenia cmdlet tworzą regułę zapory serwera PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="342cc-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="342cc-113">Przykład 2: Tworzenie nowej reguły zapory PostgreSql przy użyciu funkcji-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="342cc-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="342cc-114">Te polecenia cmdlet tworzą PostgreSqlą regułę zapory przy użyciu funkcji-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="342cc-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="342cc-115">Przykład 3: Utwórz nową regułę zapory PostgreSql, aby zezwolić na wszystkie adresy IP</span><span class="sxs-lookup"><span data-stu-id="342cc-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="342cc-116">Te polecenia cmdlet tworzą nową regułę zapory PostgreSql zezwalającą na wszystkie adresy IP.</span><span class="sxs-lookup"><span data-stu-id="342cc-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="342cc-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="342cc-117">PARAMETERS</span></span>

### <span data-ttu-id="342cc-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="342cc-118">-AllowAll</span></span>
<span data-ttu-id="342cc-119">Prezentuj, aby zezwolić na wszystkie adresy IP zakresu od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="342cc-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="342cc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="342cc-120">-AsJob</span></span>
<span data-ttu-id="342cc-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="342cc-121">Run the command as a job</span></span>

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

### <span data-ttu-id="342cc-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="342cc-122">-ClientIPAddress</span></span>
<span data-ttu-id="342cc-123">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="342cc-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="342cc-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="342cc-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="342cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342cc-125">-DefaultProfile</span></span>
<span data-ttu-id="342cc-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="342cc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342cc-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="342cc-127">-EndIPAddress</span></span>
<span data-ttu-id="342cc-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="342cc-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="342cc-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="342cc-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="342cc-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="342cc-130">-Name</span></span>
<span data-ttu-id="342cc-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="342cc-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="342cc-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="342cc-132">-NoWait</span></span>
<span data-ttu-id="342cc-133">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="342cc-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="342cc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342cc-134">-ResourceGroupName</span></span>
<span data-ttu-id="342cc-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="342cc-135">The name of the resource group.</span></span>
<span data-ttu-id="342cc-136">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="342cc-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="342cc-137">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="342cc-137">-ServerName</span></span>
<span data-ttu-id="342cc-138">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="342cc-138">The name of the server.</span></span>

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

### <span data-ttu-id="342cc-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="342cc-139">-StartIPAddress</span></span>
<span data-ttu-id="342cc-140">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="342cc-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="342cc-141">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="342cc-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="342cc-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="342cc-142">-SubscriptionId</span></span>
<span data-ttu-id="342cc-143">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="342cc-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="342cc-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="342cc-144">-Confirm</span></span>
<span data-ttu-id="342cc-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="342cc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="342cc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="342cc-146">-WhatIf</span></span>
<span data-ttu-id="342cc-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="342cc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="342cc-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="342cc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="342cc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342cc-149">CommonParameters</span></span>
<span data-ttu-id="342cc-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342cc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342cc-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="342cc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342cc-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="342cc-152">INPUTS</span></span>

## <span data-ttu-id="342cc-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="342cc-153">OUTPUTS</span></span>

### <span data-ttu-id="342cc-154">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="342cc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="342cc-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="342cc-155">NOTES</span></span>

<span data-ttu-id="342cc-156">PISUJE</span><span class="sxs-lookup"><span data-stu-id="342cc-156">ALIASES</span></span>

## <span data-ttu-id="342cc-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="342cc-157">RELATED LINKS</span></span>

