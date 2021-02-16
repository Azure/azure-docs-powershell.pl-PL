---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193882"
---
# <span data-ttu-id="f7dc7-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7dc7-101">Get-AzFirewall</span></span>

## <span data-ttu-id="f7dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dc7-103">Otrzymuje zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="f7dc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7dc7-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7dc7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="f7dc7-106">Polecenie **cmdlet Get-AzFirewall** pobiera jedną lub więcej zapór w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="f7dc7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="f7dc7-108">1. Pobieranie wszystkich zapór w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="f7dc7-108">1:  Retrieve all Firewalls in a resource group</span></span>
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
Zones                      : {}

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
Zones                      : {}
```

<span data-ttu-id="f7dc7-109">W tym przykładzie są pobierane wszystkie zapory w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="f7dc7-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="f7dc7-110">2. Pobieranie zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="f7dc7-110">2:  Retrieve a Firewall by name</span></span>
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
Zones                      : {}
```

<span data-ttu-id="f7dc7-111">W tym przykładzie jest pobierana zapora o nazwie "azFw" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="f7dc7-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="f7dc7-112">3. Pobieranie wszystkich zapór za pomocą filtrowania</span><span class="sxs-lookup"><span data-stu-id="f7dc7-112">3:  Retrieve all Firewalls with filtering</span></span>
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
Zones                      : {}

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
Zones                      : {}
```

<span data-ttu-id="f7dc7-113">W tym przykładzie są pobierane wszystkie zapory, które zaczynają się od "azFw"</span><span class="sxs-lookup"><span data-stu-id="f7dc7-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="f7dc7-114">4. Pobieranie zapory, a następnie dodawanie zbioru reguł aplikacji do Zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="f7dc7-115">W tym przykładzie jest pobierana zapora, a następnie do zapory jest dodawania zbioru reguł aplikacji przez wywoływanie metody AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="f7dc7-116">5. Pobieranie zapory, a następnie dodawanie zbioru reguł sieciowych do Zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="f7dc7-117">W tym przykładzie jest pobierana zapora, a następnie do tej zapory jest dodawania zbioru reguł sieciowych przez wywoływanie metody AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="f7dc7-118">6. Pobieranie zapory, a następnie pobieranie zbioru reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="f7dc7-119">W tym przykładzie jest pobierana zapora, a następnie pobierana jest kolekcja reguł według nazwy (metoda wywoływania: GetApplicationRuleCollectionByName) na obiekcie zapory.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="f7dc7-120">Nazwa zbioru reguł metody GetApplicationRuleCollectionByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="f7dc7-121">7. Pobieranie zapory, a następnie pobieranie zbioru reguł sieciowych według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="f7dc7-122">W tym przykładzie jest pobierana zapora, a następnie pobierana jest kolekcja reguł według nazwy ( metoda wywoływania właściwości GetNetworkRuleCollectionByName) na obiekcie zapory.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="f7dc7-123">Nazwa zbioru reguł metody GetNetworkRuleCollectionByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="f7dc7-124">8. Pobieranie zapory, a następnie usuwanie zbioru reguł aplikacji według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="f7dc7-125">W tym przykładzie jest pobierana zapora, a następnie usuwana jest kolekcja reguł według nazwy ( metoda wywoływania: RemoveApplicationRuleCollectionByName) na obiekcie zapory.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="f7dc7-126">Nazwa zbioru reguł metody RemoveApplicationRuleCollectionByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="f7dc7-127">9. Pobieranie zapory, a następnie usuwanie zbioru reguł sieciowych według nazwy z zapory</span><span class="sxs-lookup"><span data-stu-id="f7dc7-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="f7dc7-128">W tym przykładzie jest pobierana zapora, a następnie usuwana jest kolekcja reguł według nazwy , wywoływanie metody RemoveNetworkRuleCollectionByName na obiekcie zapory.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="f7dc7-129">Nazwa zbioru reguł metody RemoveNetworkRuleCollectionByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="f7dc7-130">10. Pobieranie zapory i przydzielanie jej</span><span class="sxs-lookup"><span data-stu-id="f7dc7-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="f7dc7-131">W tym przykładzie jest pobierana zapora i wywołania funkcji Przydziel na zaporze w celu uruchomienia usługi zapory przy użyciu konfiguracji (aplikacji i kolekcji reguł sieciowych) skojarzonej z zaporą.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="f7dc7-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7dc7-132">PARAMETERS</span></span>

### <span data-ttu-id="f7dc7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dc7-133">-DefaultProfile</span></span>
<span data-ttu-id="f7dc7-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc7-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f7dc7-135">-Name</span></span>
<span data-ttu-id="f7dc7-136">Określa nazwę zapory, do która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f7dc7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dc7-137">-ResourceGroupName</span></span>
<span data-ttu-id="f7dc7-138">Określa nazwę grupy zasobów, do której należy Zapora.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="f7dc7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dc7-139">CommonParameters</span></span>
<span data-ttu-id="f7dc7-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7dc7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dc7-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7dc7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dc7-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7dc7-142">INPUTS</span></span>

### <span data-ttu-id="f7dc7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f7dc7-143">System.String</span></span>

## <span data-ttu-id="f7dc7-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7dc7-144">OUTPUTS</span></span>

### <span data-ttu-id="f7dc7-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f7dc7-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="f7dc7-146">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f7dc7-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f7dc7-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7dc7-147">NOTES</span></span>

## <span data-ttu-id="f7dc7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7dc7-148">RELATED LINKS</span></span>

[<span data-ttu-id="f7dc7-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7dc7-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f7dc7-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7dc7-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="f7dc7-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7dc7-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
