---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870664"
---
# <span data-ttu-id="e899c-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e899c-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e899c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e899c-102">SYNOPSIS</span></span>
<span data-ttu-id="e899c-103">Pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="e899c-103">Gets a network security group.</span></span>

## <span data-ttu-id="e899c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e899c-104">SYNTAX</span></span>

### <span data-ttu-id="e899c-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="e899c-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e899c-106">Większa</span><span class="sxs-lookup"><span data-stu-id="e899c-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e899c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e899c-107">DESCRIPTION</span></span>
<span data-ttu-id="e899c-108">Polecenie cmdlet **Get-AzNetworkSecurityGroup** pobiera grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="e899c-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="e899c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e899c-109">EXAMPLES</span></span>

### <span data-ttu-id="e899c-110">1: pobieranie istniejącej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="e899c-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="e899c-111">To polecenie zwraca zawartość grupy zabezpieczeń sieci Azure "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="e899c-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="e899c-112">2: Wyświetlanie listy istniejących grup zabezpieczeń sieci przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="e899c-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="e899c-113">To polecenie zwraca zawartość grup zabezpieczeń sieci Azure, które zaczynają się od "NSG".</span><span class="sxs-lookup"><span data-stu-id="e899c-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="e899c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e899c-114">PARAMETERS</span></span>

### <span data-ttu-id="e899c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e899c-115">-DefaultProfile</span></span>
<span data-ttu-id="e899c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e899c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e899c-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e899c-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e899c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e899c-118">-Name</span></span>
<span data-ttu-id="e899c-119">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="e899c-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e899c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e899c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e899c-121">Określa nazwę grupy zasobów, do której należy Grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="e899c-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e899c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e899c-122">CommonParameters</span></span>
<span data-ttu-id="e899c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e899c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e899c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e899c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e899c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e899c-125">INPUTS</span></span>

### <span data-ttu-id="e899c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e899c-126">System.String</span></span>

## <span data-ttu-id="e899c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e899c-127">OUTPUTS</span></span>

### <span data-ttu-id="e899c-128">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e899c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e899c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e899c-129">NOTES</span></span>

## <span data-ttu-id="e899c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e899c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e899c-131">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e899c-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e899c-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e899c-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e899c-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e899c-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


