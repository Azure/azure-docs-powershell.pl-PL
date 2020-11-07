---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 361379d418b34e6a4d30c03ff03a85e8bc091484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709531"
---
# <span data-ttu-id="acb96-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="acb96-101">Get-AzFirewall</span></span>

## <span data-ttu-id="acb96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acb96-102">SYNOPSIS</span></span>
<span data-ttu-id="acb96-103">Pobiera zaporę Azure.</span><span class="sxs-lookup"><span data-stu-id="acb96-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="acb96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acb96-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acb96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="acb96-105">DESCRIPTION</span></span>
<span data-ttu-id="acb96-106">Polecenie cmdlet **Get-AzFirewall umożliwia pobranie** co najmniej jednej zapory w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="acb96-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="acb96-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acb96-107">EXAMPLES</span></span>

### <span data-ttu-id="acb96-108">1: pobieranie wszystkich zapór w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="acb96-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
```

<span data-ttu-id="acb96-109">W tym przykładzie są pobierane wszystkie zapory w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="acb96-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="acb96-110">2: pobieranie zapory za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="acb96-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
```

<span data-ttu-id="acb96-111">W tym przykładzie jest pobierana Zapora o nazwie "azFw" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="acb96-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="acb96-112">3: pobieranie wszystkich zapór przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="acb96-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
```

<span data-ttu-id="acb96-113">W tym przykładzie są pobierane wszystkie zapory rozpoczynające się od "azFw".</span><span class="sxs-lookup"><span data-stu-id="acb96-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="acb96-114">4: pobieranie zapory, a następnie dodawanie kolekcji reguł aplikacji do zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="acb96-115">W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł aplikacji przez połączenie metody AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="acb96-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="acb96-116">5: pobieranie zapory, a następnie dodawanie kolekcji reguł sieci do zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="acb96-117">W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł sieci przez połączenie metody AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="acb96-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="acb96-118">6: pobieranie zapory, a następnie pobieranie kolekcji reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="acb96-119">W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetApplicationRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="acb96-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="acb96-120">W nazwie kolekcji reguł dla metody GetApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="acb96-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="acb96-121">7: pobieranie zapory, a następnie pobieranie kolekcji reguł sieci według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="acb96-122">W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetNetworkRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="acb96-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="acb96-123">W nazwie kolekcji reguł dla metody GetNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="acb96-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="acb96-124">8: pobieranie zapory, a następnie Usuwanie kolekcji reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="acb96-125">W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveApplicationRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="acb96-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="acb96-126">W nazwie kolekcji reguł dla metody RemoveApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="acb96-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="acb96-127">9: pobieranie zapory, a następnie Usuwanie kolekcji reguł sieci według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="acb96-128">W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveNetworkRuleCollectionByName na obiekcie firewall.</span><span class="sxs-lookup"><span data-stu-id="acb96-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="acb96-129">W nazwie kolekcji reguł dla metody RemoveNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="acb96-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="acb96-130">10: pobieranie zapory, a następnie przydzielenie zapory</span><span class="sxs-lookup"><span data-stu-id="acb96-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="acb96-131">W tym przykładzie jest pobierana Zapora i połączenia przydzielone na zaporze w celu uruchomienia usługi firewall przy użyciu konfiguracji (aplikacji i kolekcji reguł sieci) skojarzonych z zaporą.</span><span class="sxs-lookup"><span data-stu-id="acb96-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="acb96-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acb96-132">PARAMETERS</span></span>

### <span data-ttu-id="acb96-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb96-133">-DefaultProfile</span></span>
<span data-ttu-id="acb96-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="acb96-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb96-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acb96-135">-Name</span></span>
<span data-ttu-id="acb96-136">Określa nazwę zapory, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acb96-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="acb96-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb96-137">-ResourceGroupName</span></span>
<span data-ttu-id="acb96-138">Określa nazwę grupy zasobów, do której należy Zapora.</span><span class="sxs-lookup"><span data-stu-id="acb96-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="acb96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb96-139">CommonParameters</span></span>
<span data-ttu-id="acb96-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb96-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acb96-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb96-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acb96-142">INPUTS</span></span>

### <span data-ttu-id="acb96-143">System. String</span><span class="sxs-lookup"><span data-stu-id="acb96-143">System.String</span></span>

## <span data-ttu-id="acb96-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acb96-144">OUTPUTS</span></span>

### <span data-ttu-id="acb96-145">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="acb96-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="acb96-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. PowerShell</span><span class="sxs-lookup"><span data-stu-id="acb96-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="acb96-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acb96-147">NOTES</span></span>

## <span data-ttu-id="acb96-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acb96-148">RELATED LINKS</span></span>

[<span data-ttu-id="acb96-149">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="acb96-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="acb96-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="acb96-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="acb96-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="acb96-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
