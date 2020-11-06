---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8804fd7fd9e2ea1d784d2b1607f72e7e0aa1bb6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524358"
---
# Set-AzureRmNetworkInterfaceIpConfig

## STRESZCZENIe
Ustawia stan celu konfiguracji adresu IP interfejsu sieciowego platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SetByResource (domyślny)
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmNetworkInterfaceIpConfig** ustawia stan celu konfiguracji protokołu IP interfejsu sieciowego platformy Azure.

## Przykłady

### 1: Zmienianie adresu IP konfiguracji adresu IP
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, a następnie przechowują ją w $vnet zmiennych i $subnet. Trzecia komenda uzyskuje interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana. Trzecie polecenie ustawia prywatny adres IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11. Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.
    

### 2: Kojarzenie konfiguracji IP z grupą zabezpieczeń aplikacji
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

W tym przykładzie zmienna $asg zawiera odwołanie do grupy zabezpieczeń aplikacji.
W czwartym poleceniu jest pobierany interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana. Set-AzureRmNetworkInterfaceIpConfig służy do ustawiania prywatnego adresu IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11 i tworzenia skojarzenia z pobraną grupą zabezpieczeń aplikacji.
Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.

## PARAMETRÓW

### -ApplicationGatewayBackendAddressPool
Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPool
Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
Określa kolekcję odwołań do zasad ruchu przychodzącego NAT modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konfiguracji sieci IP, dla której ustawiono to polecenie cmdlet.

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

### -NetworkInterface
Określa obiekt **NetworkInterface** .
To polecenie cmdlet umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do obiektu, który ten parametr określa.

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

### -Primary
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
Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.

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
Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.
Dopuszczalne wartości tego parametru to:
- Protokol
- Obsługi

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
Określa obiekt **PublicIPAddress** .
To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.

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
To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.

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

### -Podsieć
Określa obiekt **podsieci** .
To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.

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
To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSNetworkInterface
Parametry: NetworkInterface (ByValue)

### System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSBackendAddressPool; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSInboundNatRule; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayBackendAddressPool; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationSecurityGroup; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSNetworkInterface

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking

## LINKI POKREWNE

[Dodaj-AzureRmNetworkInterfaceIpConfig](./Add-AzureRmNetworkInterfaceIpConfig.md)

[Get-AzureRmNetworkInterfaceIpConfig](./Get-AzureRmNetworkInterfaceIpConfig.md)

[Nowe — AzureRmNetworkInterfaceIpConfig](./New-AzureRmNetworkInterfaceIpConfig.md)

[Remove-AzureRmNetworkInterfaceIpConfig](./Remove-AzureRmNetworkInterfaceIpConfig.md)


