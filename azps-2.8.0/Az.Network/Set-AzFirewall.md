---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 6d0935b0b2c5296a5d45d25c56cd7feb9e269a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869564"
---
# <span data-ttu-id="2b6c3-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-101">Set-AzFirewall</span></span>

## <span data-ttu-id="2b6c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6c3-103">Umożliwia zapisanie zmodyfikowanej zapory.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="2b6c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b6c3-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6c3-106">Polecenie cmdlet **Set-AzFirewall** aktualizuje zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="2b6c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b6c3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6c3-108">1: priorytet aktualizacji kolekcji reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="2b6c3-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="2b6c3-109">W tym przykładzie Zaktualizowano priorytet istniejącej kolekcji reguł w zaporze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="2b6c3-110">Zakładając, że Zapora platformy Azure "AzureFirewall" w grupie zasobów "RG" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia zmienią priorytet kolekcji reguł, a następnie zaktualizują zaporę systemu Azure później.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="2b6c3-111">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="2b6c3-112">2: Tworzenie zapory na platformie Azure i Konfigurowanie kolekcji reguł aplikacji później</span><span class="sxs-lookup"><span data-stu-id="2b6c3-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="2b6c3-113">W tym przykładzie Zapora jest tworzona jako pierwsza bez żadnych kolekcji reguł aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="2b6c3-114">Po utworzeniu zestawu reguł aplikacji i kolekcji reguł aplikacji obiekt firewall jest modyfikowany w pamięci bez wpływu na rzeczywistą konfigurację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="2b6c3-115">Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="2b6c3-116">3: Aktualizacja zagrożeń tryb działania usługi Zapora platformy Intel</span><span class="sxs-lookup"><span data-stu-id="2b6c3-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="2b6c3-117">W tym przykładzie zostanie zaktualizowany zagrożony tryb działania usługi Zapora Azure "AzureFirewall" w grupie zasobów "RG".</span><span class="sxs-lookup"><span data-stu-id="2b6c3-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="2b6c3-118">Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="2b6c3-119">4: cofnięcie i przydzielenie zapory</span><span class="sxs-lookup"><span data-stu-id="2b6c3-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```

<span data-ttu-id="2b6c3-120">W tym przykładzie jest pobierana Zapora, deprzydział zapory i zapisanie jej.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="2b6c3-121">Polecenie deallocate umożliwia usunięcie uruchomionej usługi, ale zachowuje konfigurację zapory.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="2b6c3-122">Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="2b6c3-123">Jeśli użytkownik chce ponownie uruchomić usługę, należy wywołać metodę allocate na zaporze.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="2b6c3-124">Nowa sieć wirtualna i publiczny adres IP muszą znajdować się w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="2b6c3-125">Ponownie, aby zmiany były odzwierciedlane w chmurze, należy najpierw wywołać Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="2b6c3-126">5: Dodawanie publicznego adresu IP do zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2b6c3-126">5:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="2b6c3-127">W tym przykładzie publiczny adres IP "azFwPublicIp1" jest dołączony do zapory.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-127">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="2b6c3-128">6: usuwanie publicznego adresu IP z zapory systemu Azure</span><span class="sxs-lookup"><span data-stu-id="2b6c3-128">6:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="2b6c3-129">W tym przykładzie publiczny adres IP "azFwPublicIp1" został odłączony od zapory.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-129">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

## <span data-ttu-id="2b6c3-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b6c3-130">PARAMETERS</span></span>

### <span data-ttu-id="2b6c3-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b6c3-131">-AsJob</span></span>
<span data-ttu-id="2b6c3-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2b6c3-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b6c3-133">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-133">-AzureFirewall</span></span>
<span data-ttu-id="2b6c3-134">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-134">The AzureFirewall</span></span>

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

### <span data-ttu-id="2b6c3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6c3-135">-DefaultProfile</span></span>
<span data-ttu-id="2b6c3-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b6c3-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b6c3-137">-Confirm</span></span>
<span data-ttu-id="2b6c3-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6c3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6c3-139">-WhatIf</span></span>
<span data-ttu-id="2b6c3-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b6c3-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6c3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6c3-142">CommonParameters</span></span>
<span data-ttu-id="2b6c3-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6c3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6c3-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6c3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6c3-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b6c3-145">INPUTS</span></span>

### <span data-ttu-id="2b6c3-146">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="2b6c3-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b6c3-147">OUTPUTS</span></span>

### <span data-ttu-id="2b6c3-148">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="2b6c3-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b6c3-149">NOTES</span></span>

## <span data-ttu-id="2b6c3-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b6c3-150">RELATED LINKS</span></span>

[<span data-ttu-id="2b6c3-151">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-151">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="2b6c3-152">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="2b6c3-153">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2b6c3-153">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
