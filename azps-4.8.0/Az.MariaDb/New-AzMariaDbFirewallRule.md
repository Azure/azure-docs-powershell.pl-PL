---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063487"
---
# <span data-ttu-id="6d89d-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d89d-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="6d89d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d89d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d89d-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6d89d-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6d89d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d89d-104">SYNTAX</span></span>

### <span data-ttu-id="6d89d-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6d89d-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d89d-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="6d89d-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6d89d-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d89d-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d89d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6d89d-108">DESCRIPTION</span></span>
<span data-ttu-id="6d89d-109">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6d89d-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6d89d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d89d-110">EXAMPLES</span></span>

### <span data-ttu-id="6d89d-111">Przykład 1. Tworzenie reguły zapory w obszarze MariaDB</span><span class="sxs-lookup"><span data-stu-id="6d89d-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="6d89d-112">To polecenie powoduje utworzenie reguły zapory pod MariaDB.</span><span class="sxs-lookup"><span data-stu-id="6d89d-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="6d89d-113">Przykład 2: Tworzenie nowej reguły zapory MariaDB przy użyciu funkcji-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6d89d-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="6d89d-114">Te polecenia cmdlet tworzą MariaDBą regułę zapory przy użyciu funkcji-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6d89d-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="6d89d-115">Przykład 3: Utwórz nową regułę zapory MariaDB, aby zezwolić na wszystkie adresy IP</span><span class="sxs-lookup"><span data-stu-id="6d89d-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="6d89d-116">Te polecenia cmdlet tworzą nową regułę zapory MariaDB zezwalającą na wszystkie adresy IP.</span><span class="sxs-lookup"><span data-stu-id="6d89d-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="6d89d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d89d-117">PARAMETERS</span></span>

### <span data-ttu-id="6d89d-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="6d89d-118">-AllowAll</span></span>
<span data-ttu-id="6d89d-119">Prezentuj, aby zezwolić na wszystkie adresy IP zakresu od 0.0.0.0 do 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="6d89d-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="6d89d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d89d-120">-AsJob</span></span>
<span data-ttu-id="6d89d-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6d89d-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6d89d-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d89d-122">-ClientIPAddress</span></span>
<span data-ttu-id="6d89d-123">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6d89d-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6d89d-124">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6d89d-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6d89d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d89d-125">-DefaultProfile</span></span>
<span data-ttu-id="6d89d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d89d-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d89d-127">-EndIPAddress</span></span>
<span data-ttu-id="6d89d-128">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6d89d-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6d89d-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6d89d-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6d89d-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d89d-130">-Name</span></span>
<span data-ttu-id="6d89d-131">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6d89d-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="6d89d-132">Jeśli nie określono tego parametru, wartość domyślna jest niezdefiniowana.</span><span class="sxs-lookup"><span data-stu-id="6d89d-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="6d89d-133">Jeśli AllowAll jest obecny, nazwa domyślna to AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="6d89d-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="6d89d-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6d89d-134">-NoWait</span></span>
<span data-ttu-id="6d89d-135">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6d89d-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d89d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d89d-136">-ResourceGroupName</span></span>
<span data-ttu-id="6d89d-137">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6d89d-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d89d-138">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6d89d-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d89d-139">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6d89d-139">-ServerName</span></span>
<span data-ttu-id="6d89d-140">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="6d89d-140">The name of the server.</span></span>

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

### <span data-ttu-id="6d89d-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d89d-141">-StartIPAddress</span></span>
<span data-ttu-id="6d89d-142">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="6d89d-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6d89d-143">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="6d89d-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6d89d-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6d89d-144">-SubscriptionId</span></span>
<span data-ttu-id="6d89d-145">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6d89d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d89d-146">-Confirm</span></span>
<span data-ttu-id="6d89d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d89d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d89d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d89d-148">-WhatIf</span></span>
<span data-ttu-id="6d89d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d89d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d89d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d89d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d89d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d89d-151">CommonParameters</span></span>
<span data-ttu-id="6d89d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d89d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d89d-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d89d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d89d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d89d-154">INPUTS</span></span>

## <span data-ttu-id="6d89d-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d89d-155">OUTPUTS</span></span>

### <span data-ttu-id="6d89d-156">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d89d-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="6d89d-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d89d-157">NOTES</span></span>

<span data-ttu-id="6d89d-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6d89d-158">ALIASES</span></span>

## <span data-ttu-id="6d89d-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d89d-159">RELATED LINKS</span></span>

