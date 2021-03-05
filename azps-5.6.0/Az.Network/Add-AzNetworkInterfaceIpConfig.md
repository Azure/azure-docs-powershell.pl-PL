---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 47ad7c00c2db310003dcc87b20405d05ec7f1f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009482"
---
# Add-AzNetworkInterfaceIpConfig

## SYNOPSIS
Dodaje konfigurację protokołu IP interfejsu sieciowego do interfejsu sieciowego.

## SKŁADNIA

### SetByResource (Domyślne)
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzNetworkInterfaceIpConfig** dodaje konfigurację adresu IP interfejsu sieciowego do interfejsu sieciowego platformy Azure.

## PRZYKŁADY

### Przykład 1. Dodawanie nowej konfiguracji adresu IP za pomocą grupy zabezpieczeń aplikacji
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

W tym przykładzie tworzymy nowy interfejs sieciowy MyNetworkInterface, który należy do podsieci w nowej sieci wirtualnej MyVNET. Tworzymy również pustą grupę zabezpieczeń aplikacji, MyASG, aby skojarzyć z konfiguracjami adresów IP w interfejsie sieciowym. Po utworzeniu obu obiektów łączymy domyślną konfigurację adresów IP z obiektem MyASG. Na koniec tworzymy nową konfigurację adresów IP w interfejsie sieciowym połączonym również z obiektem grupy zabezpieczeń aplikacji.

## PARAMETERS

### -ApplicationGatewayBackendAddressPool
Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -LoadBalancerBackendAddressPool
Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
Określa zbiór odwołań do reguł translacji adresów sieciowych (NAT), do których należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
Określa zbiór odwołań do reguł nat ruchu przychodzącego NAT równoważenia obciążenia, do których należy ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę konfiguracji protokołu IP interfejsu sieciowego.

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

### - NetworkInterface
Określa **obiekt NetworkInterface.**
To polecenie cmdlet dodaje konfigurację protokołu IP interfejsu sieciowego do obiektu, który określa ten parametr.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — podstawowy
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

### -PrivateIpAddress
Określa statyczny adres IP konfiguracji protokołu IP interfejsu sieciowego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddressVersion
Określa wersję adresu IP konfiguracji protokołu IP interfejsu sieciowego.
Dopuszczalne wartości dla tego parametru to:
- IPv4
- IPv6

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Określa obiekt **PublicIPAddress.**
To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Określa obiekt **Podsieci.**
To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking

## LINKI POKREWNE

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[New-AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)
