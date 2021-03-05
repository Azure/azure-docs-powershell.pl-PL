---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 2675c304913e16f6d62f7b1f9067a7e4280422bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963969"
---
# <span data-ttu-id="fe616-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-101">Set-AzFirewall</span></span>

## <span data-ttu-id="fe616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe616-102">SYNOPSIS</span></span>
<span data-ttu-id="fe616-103">Zapisuje zmodyfikowaną zaporę.</span><span class="sxs-lookup"><span data-stu-id="fe616-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="fe616-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe616-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe616-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe616-105">DESCRIPTION</span></span>
<span data-ttu-id="fe616-106">Polecenie **cmdlet Set-AzFirewall** aktualizuje Zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe616-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="fe616-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe616-107">EXAMPLES</span></span>

### <span data-ttu-id="fe616-108">1. Aktualizowanie priorytetu zbioru reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="fe616-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="fe616-109">W tym przykładzie priorytet istniejącej kolekcji reguł zapory platformy Azure jest aktualizowany.</span><span class="sxs-lookup"><span data-stu-id="fe616-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="fe616-110">Zakładając, że zapora platformy Azure "AzureFirewall" w grupie zasobów "rg" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia później zmienią priorytet tego zbioru reguł i zaktualizują Zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe616-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="fe616-111">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="fe616-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="fe616-112">2. Tworzenie zapory platformy Azure i ustawianie zbioru reguł aplikacji później</span><span class="sxs-lookup"><span data-stu-id="fe616-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-113">W tym przykładzie Zapora jest tworzona najpierw bez żadnych kolekcji reguł aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe616-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="fe616-114">Później są tworzone reguły aplikacji i zbiór reguł aplikacji, a następnie obiekt Zapory jest modyfikowany w pamięci, bez wpływu na rzeczywistą konfigurację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="fe616-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="fe616-115">Aby zmiany mają być odzwierciedlane w chmurze, Set-AzFirewall musi zostać wywołana.</span><span class="sxs-lookup"><span data-stu-id="fe616-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="fe616-116">3. Aktualizowanie trybu operacji "Threat Intel" zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="fe616-117">W tym przykładzie aktualizacja trybu operacji Threat Intel zapory platformy Azure "AzureFirewall" w grupie zasobów "rg".</span><span class="sxs-lookup"><span data-stu-id="fe616-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="fe616-118">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="fe616-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="fe616-119">4. Przydzielanie transakcji i przydzielanie zapory</span><span class="sxs-lookup"><span data-stu-id="fe616-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="fe616-120">W tym przykładzie jest pobierana zapora, lokalizuje zaporę i zapisuje ją.</span><span class="sxs-lookup"><span data-stu-id="fe616-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="fe616-121">Polecenie Deallocate usuwa uruchamianą usługę, ale zachowuje konfigurację zapory.</span><span class="sxs-lookup"><span data-stu-id="fe616-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="fe616-122">Aby zmiany mają być odzwierciedlane w chmurze, Set-AzFirewall musi zostać wywołana.</span><span class="sxs-lookup"><span data-stu-id="fe616-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="fe616-123">Jeśli użytkownik chce ponownie uruchomić usługę, należy uruchomić metodę Allocate w zaporze.</span><span class="sxs-lookup"><span data-stu-id="fe616-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="fe616-124">Nowy adres VNet i publiczny adres IP muszą znajdować się w tej samej grupie zasobów co zapora.</span><span class="sxs-lookup"><span data-stu-id="fe616-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="fe616-125">Również w celu odzwierciedlenia zmian w chmurze Set-AzFirewall musi zostać wywołana.</span><span class="sxs-lookup"><span data-stu-id="fe616-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="fe616-126">5. Przydzielanie przy użyciu publicznego adresu IP zarządzania na scenariusze wymuszonego rozdzielania</span><span class="sxs-lookup"><span data-stu-id="fe616-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="fe616-127">W tym przykładzie zapora z publicznym adresem IP zarządzania i podsiecią zarządzania jest przydzielana w scenariuszach z wymuszonym rozdzielaniem.</span><span class="sxs-lookup"><span data-stu-id="fe616-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="fe616-128">Sieć VNet musi zawierać podsieci o nazwie "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="fe616-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="fe616-129">6. Dodawanie publicznego adresu IP do zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-130">W tym przykładzie publiczny adres IP "azFwPublicIp1" dołączony do zapory.</span><span class="sxs-lookup"><span data-stu-id="fe616-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="fe616-131">7. Usuwanie publicznego adresu IP z Zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-132">W tym przykładzie publiczny adres IP "azFwPublicIp1" jako odłączony od Zapory.</span><span class="sxs-lookup"><span data-stu-id="fe616-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="fe616-133">8. Zmienianie publicznego adresu IP zarządzania w Zaporze platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-134">W tym przykładzie publiczny adres IP zarządzania zapory zostanie zmieniony na "AzFwMgmtPublicIp2".</span><span class="sxs-lookup"><span data-stu-id="fe616-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="fe616-135">9. Dodawanie konfiguracji systemu DNS do zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-136">W tym przykładzie konfiguracja serwera proxy DNS i serwera DNS jest dołączona do zapory.</span><span class="sxs-lookup"><span data-stu-id="fe616-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="fe616-137">10. Aktualizowanie miejsca docelowego istniejącej reguły w zbiorze reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="fe616-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="fe616-138">W tym przykładzie jest aktualizowana docelowa istniejąca reguła w zbiorze reguł zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe616-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="fe616-139">Dzięki temu można automatycznie aktualizować reguły, gdy adresy IP zmieniają się dynamicznie.</span><span class="sxs-lookup"><span data-stu-id="fe616-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="fe616-140">11. Zezwalanie na aktywne protokół FTP w zaporze platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe616-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="fe616-141">W tym przykładzie aktywny protokół FTP jest dozwolony na zaporze.</span><span class="sxs-lookup"><span data-stu-id="fe616-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="fe616-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe616-142">PARAMETERS</span></span>

### <span data-ttu-id="fe616-143">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fe616-143">-AsJob</span></span>
<span data-ttu-id="fe616-144">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fe616-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe616-145">— AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-145">-AzureFirewall</span></span>
<span data-ttu-id="fe616-146">The AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe616-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe616-147">-DefaultProfile</span></span>
<span data-ttu-id="fe616-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe616-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe616-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe616-149">-Confirm</span></span>
<span data-ttu-id="fe616-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe616-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe616-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe616-151">-WhatIf</span></span>
<span data-ttu-id="fe616-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe616-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe616-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe616-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe616-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe616-154">CommonParameters</span></span>
<span data-ttu-id="fe616-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe616-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe616-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe616-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe616-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe616-157">INPUTS</span></span>

### <span data-ttu-id="fe616-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="fe616-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe616-159">OUTPUTS</span></span>

### <span data-ttu-id="fe616-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="fe616-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe616-161">NOTES</span></span>

## <span data-ttu-id="fe616-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe616-162">RELATED LINKS</span></span>

[<span data-ttu-id="fe616-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="fe616-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="fe616-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fe616-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
