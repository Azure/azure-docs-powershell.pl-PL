---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: 1f49c2de253b41db97719933111a5ec2f9b861d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193834"
---
# <span data-ttu-id="b5b26-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5b26-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="b5b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b26-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b26-103">Otrzymuje interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="b5b26-103">Gets a network interface.</span></span>

## <span data-ttu-id="b5b26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5b26-104">SYNTAX</span></span>

### <span data-ttu-id="b5b26-105">NoExpandStandAloneNic (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b5b26-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b26-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="b5b26-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b26-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="b5b26-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b26-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="b5b26-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b26-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b26-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b26-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b26-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b26-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5b26-111">DESCRIPTION</span></span>
<span data-ttu-id="b5b26-112">Polecenie **cmdlet Get-AzNetworkInterface** otrzymuje interfejs sieciowy platformy Azure lub listę interfejsów sieciowych platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5b26-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="b5b26-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5b26-113">EXAMPLES</span></span>

### <span data-ttu-id="b5b26-114">Przykład 1. Uzyskiwanie wszystkich interfejsów sieciowych</span><span class="sxs-lookup"><span data-stu-id="b5b26-114">Example 1: Get all network interfaces</span></span>
```
PS C:\> Get-AzNetworkInterface

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="b5b26-115">To polecenie pobiera wszystkie interfejsy sieciowe dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b5b26-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="b5b26-116">Przykład 2. Uzyskiwanie wszystkich interfejsów sieciowych z określonym stanem inicjowania obsługi</span><span class="sxs-lookup"><span data-stu-id="b5b26-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="b5b26-117">To polecenie pobiera wszystkie interfejsy sieciowe w grupie zasobów o nazwie ResourceGroup1, w przypadku których stan inicjowania obsługi administracyjnej zakończył się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="b5b26-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="b5b26-118">Przykład 3. Uzyskiwanie interfejsów sieciowych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="b5b26-118">Example 3: Get network interfaces using filtering</span></span>
```
PS C:\> Get-AzNetworkInterface -Name test*

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="b5b26-119">To polecenie pobiera wszystkie interfejsy sieciowe dla bieżącej subskrypcji, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="b5b26-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="b5b26-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b26-120">PARAMETERS</span></span>

### <span data-ttu-id="b5b26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b26-121">-DefaultProfile</span></span>
<span data-ttu-id="b5b26-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b26-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b26-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b5b26-123">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b26-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b5b26-124">-Name</span></span>
<span data-ttu-id="b5b26-125">Określa nazwę interfejsu sieciowego, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b26-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b5b26-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b26-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5b26-127">Określa nazwę grupy zasobów, z której to polecenie cmdlet uzyskuje interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="b5b26-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b5b26-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5b26-128">-ResourceId</span></span>
<span data-ttu-id="b5b26-129">Identyfikator menedżera zasobów platformy Azure interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5b26-129">The Azure resource manager id of the network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b26-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="b5b26-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="b5b26-131">Określa indeks maszyny wirtualnej zestawu skali maszyny wirtualnej, z którego to polecenie cmdlet uzyskuje interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="b5b26-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b26-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b5b26-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="b5b26-133">Określa nazwę zestawu skali maszyny wirtualnej, z którego to polecenie cmdlet uzyskuje interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="b5b26-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b26-134">CommonParameters</span></span>
<span data-ttu-id="b5b26-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b26-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5b26-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b26-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b26-137">INPUTS</span></span>

### <span data-ttu-id="b5b26-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b5b26-138">System.String</span></span>

## <span data-ttu-id="b5b26-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5b26-139">OUTPUTS</span></span>

### <span data-ttu-id="b5b26-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5b26-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b5b26-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5b26-141">NOTES</span></span>

## <span data-ttu-id="b5b26-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b26-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5b26-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5b26-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="b5b26-144">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5b26-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="b5b26-145">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5b26-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


