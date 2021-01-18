---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503173"
---
# <span data-ttu-id="f4cae-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-101">Set-AzFirewall</span></span>

## <span data-ttu-id="f4cae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4cae-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cae-103">Umożliwia zapisanie zmodyfikowanej zapory.</span><span class="sxs-lookup"><span data-stu-id="f4cae-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="f4cae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4cae-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4cae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4cae-105">DESCRIPTION</span></span>
<span data-ttu-id="f4cae-106">Polecenie cmdlet **Set-AzFirewall** aktualizuje zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cae-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="f4cae-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4cae-107">EXAMPLES</span></span>

### <span data-ttu-id="f4cae-108">1: priorytet aktualizacji kolekcji reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="f4cae-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="f4cae-109">W tym przykładzie Zaktualizowano priorytet istniejącej kolekcji reguł w zaporze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cae-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="f4cae-110">Zakładając, że Zapora platformy Azure "AzureFirewall" w grupie zasobów "RG" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia zmienią priorytet kolekcji reguł, a następnie zaktualizują zaporę systemu Azure później.</span><span class="sxs-lookup"><span data-stu-id="f4cae-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="f4cae-111">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f4cae-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="f4cae-112">2: Tworzenie zapory na platformie Azure i Konfigurowanie kolekcji reguł aplikacji później</span><span class="sxs-lookup"><span data-stu-id="f4cae-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-113">W tym przykładzie Zapora jest tworzona jako pierwsza bez żadnych kolekcji reguł aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4cae-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="f4cae-114">Po utworzeniu zestawu reguł aplikacji i kolekcji reguł aplikacji obiekt firewall jest modyfikowany w pamięci bez wpływu na rzeczywistą konfigurację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="f4cae-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="f4cae-115">Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="f4cae-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="f4cae-116">3: Aktualizacja zagrożeń tryb działania usługi Zapora platformy Intel</span><span class="sxs-lookup"><span data-stu-id="f4cae-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="f4cae-117">W tym przykładzie zostanie zaktualizowany zagrożony tryb działania usługi Zapora Azure "AzureFirewall" w grupie zasobów "RG".</span><span class="sxs-lookup"><span data-stu-id="f4cae-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="f4cae-118">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f4cae-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="f4cae-119">4: cofnięcie i przydzielenie zapory</span><span class="sxs-lookup"><span data-stu-id="f4cae-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="f4cae-120">W tym przykładzie jest pobierana Zapora, deprzydział zapory i zapisanie jej.</span><span class="sxs-lookup"><span data-stu-id="f4cae-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="f4cae-121">Polecenie deallocate umożliwia usunięcie uruchomionej usługi, ale zachowuje konfigurację zapory.</span><span class="sxs-lookup"><span data-stu-id="f4cae-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="f4cae-122">Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="f4cae-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="f4cae-123">Jeśli użytkownik chce ponownie uruchomić usługę, należy wywołać metodę allocate na zaporze.</span><span class="sxs-lookup"><span data-stu-id="f4cae-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="f4cae-124">Nowa sieć wirtualna i publiczny adres IP muszą znajdować się w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f4cae-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="f4cae-125">Ponownie, aby zmiany były odzwierciedlane w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="f4cae-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="f4cae-126">5: przydzielanie za pomocą publicznego adresu IP zarządzania scenariuszami wymuszonego tunelowania</span><span class="sxs-lookup"><span data-stu-id="f4cae-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="f4cae-127">W tym przykładzie przydzielona jest Zapora z publicznym adresem IP i podsiecią zarządzania dla scenariuszy wymuszonych tunelowania.</span><span class="sxs-lookup"><span data-stu-id="f4cae-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="f4cae-128">Sieć wirtualna musi zawierać podsieć o nazwie "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="f4cae-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="f4cae-129">6: Dodawanie publicznego adresu IP do zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f4cae-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-130">W tym przykładzie publiczny adres IP "azFwPublicIp1" jest dołączony do zapory.</span><span class="sxs-lookup"><span data-stu-id="f4cae-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="f4cae-131">7: usuwanie publicznego adresu IP z zapory systemu Azure</span><span class="sxs-lookup"><span data-stu-id="f4cae-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-132">W tym przykładzie publiczny adres IP "azFwPublicIp1" został odłączony od zapory.</span><span class="sxs-lookup"><span data-stu-id="f4cae-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="f4cae-133">8: Zmienianie publicznego adresu IP zarządzania na zaporze platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f4cae-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-134">W tym przykładzie publiczny adres IP dla zarządzania zaporą zostanie zmieniony na "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="f4cae-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="f4cae-135">9: Dodawanie konfiguracji DNS do zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f4cae-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-136">W tym przykładzie do zapory jest dołączona konfiguracja serwera proxy DNS i serwer DNS.</span><span class="sxs-lookup"><span data-stu-id="f4cae-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="f4cae-137">10: aktualizowanie miejsca docelowego istniejącej reguły w kolekcji reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="f4cae-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="f4cae-138">W tym przykładzie jest aktualizowana lokalizacja docelowa istniejącej reguły w kolekcji reguł zapory systemu Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cae-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="f4cae-139">Dzięki temu można automatycznie aktualizować reguły, gdy adresy IP zmieniają się dynamicznie.</span><span class="sxs-lookup"><span data-stu-id="f4cae-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="f4cae-140">11: Zezwalaj na aktywną usługę FTP w zaporze platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f4cae-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="f4cae-141">W tym przykładzie w zaporze jest dozwolony aktywny protokół FTP.</span><span class="sxs-lookup"><span data-stu-id="f4cae-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="f4cae-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4cae-142">PARAMETERS</span></span>

### <span data-ttu-id="f4cae-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4cae-143">-AsJob</span></span>
<span data-ttu-id="f4cae-144">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f4cae-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4cae-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-145">-AzureFirewall</span></span>
<span data-ttu-id="f4cae-146">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="f4cae-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cae-147">-DefaultProfile</span></span>
<span data-ttu-id="f4cae-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cae-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4cae-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4cae-149">-Confirm</span></span>
<span data-ttu-id="f4cae-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4cae-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4cae-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cae-151">-WhatIf</span></span>
<span data-ttu-id="f4cae-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4cae-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4cae-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4cae-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cae-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cae-154">CommonParameters</span></span>
<span data-ttu-id="f4cae-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cae-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cae-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cae-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cae-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cae-157">INPUTS</span></span>

### <span data-ttu-id="f4cae-158">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f4cae-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4cae-159">OUTPUTS</span></span>

### <span data-ttu-id="f4cae-160">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f4cae-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4cae-161">NOTES</span></span>

## <span data-ttu-id="f4cae-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4cae-162">RELATED LINKS</span></span>

[<span data-ttu-id="f4cae-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f4cae-164">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f4cae-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f4cae-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
