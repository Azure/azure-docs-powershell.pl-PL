---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194003"
---
# Add-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Dodaje konfigurację frontoronu IP do bramy aplikacji.

## SKŁADNIA

### SetByResourceId
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzApplicationGatewayFrontendIPConfig** dodaje konfigurację frontoronu IP do bramy aplikacji.
Brama aplikacji obsługuje dwa typy konfiguracji frontoronu IP: 
- Publiczne adresy IP
- Prywatne adresy IP używające wewnętrznego równoważenia obciążenia (ILB) Brama aplikacji może mieć co najwyżej jeden publiczny adres IP i jeden prywatny adres IP.
Dodaj publiczny adres IP i prywatny adres IP jako osobne adresy IP frontoronu.

## PRZYKŁADY

### Przykład 1. Dodawanie publicznego adresu IP jako adresu IP frontoronu
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Pierwsze polecenie tworzy publiczny obiekt adresu IP i przechowuje go w $PublicIp adresie.
Drugie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.
Trzecie polecenie dodaje konfigurację frontoronu IP o nazwie FrontEndIp01, dla bramy w programie $AppGw, używając adresu przechowywanego w $PublicIp.

### Przykład 2. Dodawanie statycznego prywatnego adresu IP jako adresu IP frontoronu
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.
Drugie polecenie pobiera konfigurację podsieci o nazwie Podsieci01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.
Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.
Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia i prywatnego adresu IP 10.0.1.1.

### Przykład 3. Dodawanie dynamicznego prywatnego adresu IP jako adresu IP frontoronu
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.
Drugie polecenie pobiera konfigurację podsieci o nazwie Podsieci01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.
Trzecie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w $AppGw zmienną.
Czwarte polecenie dodaje konfigurację frontoronu IP o nazwie FrontendIP02, używając $Subnet drugiego polecenia.

## PARAMETERS

### - ApplicationGateway
Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację frontoronu IP.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Określa nazwę konfiguracji frontoronu IP do dodania.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddress
Określa prywatny adres IP do dodania jako fronto endowy adres IP dla bramy aplikacji.
Jeśli jest określony, ten adres IP jest przydzielany statycznie z podsieci.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Określa publiczny adres IP, który to polecenie cmdlet dodaje jako frontowy adres IP bramy aplikacji.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Określa identyfikator publicznego adresu IP, który to polecenie cmdlet dodaje jako adres FRONT-END IP bramy aplikacji.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Określa podsieci, którą to polecenie cmdlet dodaje jako konfigurację frontoronu IP.
Określenie tego parametru oznacza, że brama aplikacji obsługuje prywatną konfigurację opartą na adresie IP.
Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.
Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Określa identyfikator podsieci, którą to polecenie cmdlet dodaje jako konfigurację frontoronu ip.
Przechodząca podsieci oznacza prywatny adres IP.
Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do tej podsieci.
W przeciwnym razie jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTATKI

## LINKI POKREWNE

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


