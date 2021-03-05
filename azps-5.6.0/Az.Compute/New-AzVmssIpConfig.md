---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965041"
---
# New-AzVmssIpConfig

## SYNOPSIS
Tworzy konfigurację adresów IP dla interfejsu sieciowego maszyn wirtualnych.

## SKŁADNIA

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzVmssIpConfig** tworzy obiekt konfiguracji adresu IP dla interfejsu sieciowego zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).
Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* Add-AzVmssNetworkInterfaceConfiguration cmdlet.

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu konfiguracji protokołu IP dla interfejsu usług VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

To polecenie tworzy obiekt konfiguracji adresu IP o nazwie ContosoVmssInterface02.
W poleceniu jest używany wcześniej zdefiniowany identyfikator podsieci przechowywany w $SubnetId.
Polecenie przechowuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia z poleceniem **Add-AzVmssNetworkInterfaceConfiguration.**

### Przykład 2. Tworzenie obiektu konfiguracji protokołu IP, który zawiera ustawienia puli NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

To polecenie tworzy obiekt konfiguracji adresu IP o nazwie ContosoVmssInterface03, a następnie przechowuje go w $IPConfiguration do późniejszego użycia.
W poleceniu jest używany wcześniej zdefiniowany identyfikator podsieci przechowywany w $SubnetId.
To polecenie przechowuje ustawienia konfiguracji w $IPConfiguration do późniejszego użycia.
To polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* i *LoadBalancerBackendAddressPoolsId.*

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
Określa tablicę odwołań do pul adresów zaplecza dla równoważenia obciążenia.
Zestaw skali może odwoływać się do puli adresów wewnętrznego jednego publicznego i wewnętrznego równoważenia obciążenia.
W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### - DnsSetting
Ustawienia DNS, które mają być stosowane do adresów PUBLICIP.
Etykieta nazwy domeny ustawień DNS, które mają być stosowane do adresów PUBLICIP.
Concatenation of the domain name label and maszyny wirtualnej index will be the domain name labels of the Public IP Address resources that will be created.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Identyfikator
Określa identyfikator.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Określa tablicę obiektów tagu ip.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Określa tablicę odwołań do pul translacji adresów sieciowych (NAT, incoming network address translation) dla równoważenia obciążenia.
Zestaw skali może odwoływać się do przychodzących pul NAT jednego publicznego i wewnętrznego równoważenia obciążenia.
W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Określa tablicę odwołań do przychodzących pul NAT dla równoważenia obciążenia.
Zestaw skali może odwoływać się do przychodzących pul NAT jednego publicznego i wewnętrznego równoważenia obciążenia.
W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę konfiguracji protokołu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — podstawowy
Określa podstawową konfigurację adresów IP, jeśli interfejs sieciowy ma więcej niż jedną konfigurację adresów IP.

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

### -PrivateIPAddressVersion
Określ konfigurację adresu IP dla prywatnego adresu IP.  Protokół IPv4 jest domyślnie przyjmowany jako protokół IPv4.  Dopuszczalne wartości to: "IPv4" i "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Limit czasu bezczynności publicznego adresu IP.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Nazwa konfiguracji publicznego adresu IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Określ konfigurację adresu IP dla publicznego adresu IP.  Protokół IPv4 jest domyślnie przyjmowany jako protokół IPv4.  Dopuszczalne wartości to: "IPv4" i "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - PublicIPPrefix
Identyfikator publicznego prefiksu IP

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy usług WIRTUALNYCH.MASZYN WIRTUALNYCH.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## NOTATKI

## LINKI POKREWNE

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


