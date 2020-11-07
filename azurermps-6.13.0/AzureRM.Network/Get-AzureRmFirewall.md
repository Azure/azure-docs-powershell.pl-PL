---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719089"
---
# <span data-ttu-id="ea6e2-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ea6e2-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="ea6e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6e2-103">Pobiera zaporę Azure.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea6e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea6e2-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea6e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ea6e2-106">Polecenie cmdlet **Get-AzureRmFirewall umożliwia pobranie** co najmniej jednej zapory w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="ea6e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="ea6e2-108">1: pobieranie wszystkich zapór w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ea6e2-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="ea6e2-109">W tym przykładzie są pobierane wszystkie zapory w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="ea6e2-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="ea6e2-110">2: pobieranie zapory za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="ea6e2-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="ea6e2-111">W tym przykładzie jest pobierana Zapora o nazwie "azFw" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="ea6e2-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="ea6e2-112">3: pobieranie zapory, a następnie dodawanie kolekcji reguł aplikacji do zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="ea6e2-113">W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł aplikacji przez połączenie metody AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="ea6e2-114">4: pobieranie zapory, a następnie dodawanie kolekcji reguł sieci do zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="ea6e2-115">W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł sieci przez połączenie metody AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="ea6e2-116">5: pobieranie zapory, a następnie pobieranie kolekcji reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="ea6e2-117">W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetApplicationRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ea6e2-118">W nazwie kolekcji reguł dla metody GetApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ea6e2-119">6: pobieranie zapory, a następnie pobieranie kolekcji reguł sieci według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="ea6e2-120">W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetNetworkRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ea6e2-121">W nazwie kolekcji reguł dla metody GetNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ea6e2-122">7: pobieranie zapory, a następnie Usuwanie kolekcji reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="ea6e2-123">W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveApplicationRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ea6e2-124">W nazwie kolekcji reguł dla metody RemoveApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ea6e2-125">8: pobieranie zapory, a następnie Usuwanie kolekcji reguł sieci według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="ea6e2-126">W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveNetworkRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ea6e2-127">W nazwie kolekcji reguł dla metody RemoveNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ea6e2-128">9: pobieranie zapory, a następnie przydzielenie zapory</span><span class="sxs-lookup"><span data-stu-id="ea6e2-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="ea6e2-129">W tym przykładzie jest pobierana Zapora i połączenia przydzielone na zaporze w celu uruchomienia usługi firewall przy użyciu konfiguracji (aplikacji i kolekcji reguł sieci) skojarzonych z zaporą.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="ea6e2-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea6e2-130">PARAMETERS</span></span>

### <span data-ttu-id="ea6e2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6e2-131">-DefaultProfile</span></span>
<span data-ttu-id="ea6e2-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6e2-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea6e2-133">-Name</span></span>
<span data-ttu-id="ea6e2-134">Określa nazwę zapory, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6e2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6e2-135">-ResourceGroupName</span></span>
<span data-ttu-id="ea6e2-136">Określa nazwę grupy zasobów, do której należy Zapora.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6e2-137">CommonParameters</span></span>
<span data-ttu-id="ea6e2-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6e2-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6e2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6e2-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea6e2-140">INPUTS</span></span>

### <span data-ttu-id="ea6e2-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ea6e2-141">None</span></span>
<span data-ttu-id="ea6e2-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ea6e2-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea6e2-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea6e2-143">OUTPUTS</span></span>

### <span data-ttu-id="ea6e2-144">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ea6e2-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ea6e2-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea6e2-145">NOTES</span></span>

## <span data-ttu-id="ea6e2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea6e2-146">RELATED LINKS</span></span>

[<span data-ttu-id="ea6e2-147">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ea6e2-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="ea6e2-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ea6e2-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="ea6e2-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ea6e2-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
