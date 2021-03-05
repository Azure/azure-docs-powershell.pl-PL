---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986763"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Tworzy konfigurację fronto strony ip dla bramy aplikacji.

## SKŁADNIA

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzApplicationGatewayFrontendIPConfig** tworzy konfigurację frontoronu IP dla bramy aplikacji Azure.
Brama aplikacji obsługuje dwa typy konfiguracji frontoronu IP: 
- Publiczne adresy IP — prywatne adresy IP z użyciem wewnętrznego równoważenia obciążenia (ILB).
 Brama aplikacji może mieć co najwyżej jeden publiczny adres IP i jeden prywatny adres IP.
Publiczny adres IP i prywatny adres IP należy dodawać oddzielnie jako adresy IP frontoronu.

## PRZYKŁADY

### Przykład 1. Tworzenie konfiguracji frontoronu adresu IP przy użyciu obiektu publicznego zasobu IP
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Pierwsze polecenie tworzy publiczny obiekt zasobu IP i przechowuje go w $PublicIP zmienną.
Drugie polecenie używa $PublicIP do utworzenia nowej konfiguracji frontonu ip o nazwie FrontEndIP01 i przechowuje ją w $FrontEnd frontonu.

### Przykład 2. Tworzenie statycznego prywatnego adresu IP jako adresu IP frontoronu
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.
Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.
Trzecie polecenie tworzy konfigurację frontonu ip o nazwie FrontEndIP02 przy użyciu drugiego polecenia i prywatnego adresu IP 10.0.1.1, $Subnet następnie zapisuje go w zmiennej $FrontEnd.

### Przykład 3. Tworzenie dynamicznego prywatnego adresu IP jako adresu IP frontoronu
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Pierwsze polecenie otrzymuje sieć wirtualną o nazwie VNet01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $VNet zasobów.
Drugie polecenie pobiera konfigurację podsieci o nazwie Subnet01, używając $VNet pierwszego polecenia i zapisuje je w zmiennej $Subnet podrzędnej.
Trzecie polecenie tworzy konfigurację frontonu ip o nazwie FrontEndIP03, używając $Subnet drugiego polecenia i zapisuje ją w $FrontEnd danych.

## PARAMETERS

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
Określa nazwę konfiguracji frontoronu ip, która jest owana przez to polecenie cmdlet.

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
Określa prywatny adres IP, który to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.
Tę wartość można określić tylko wtedy, gdy jest określona podsieci.
Ten adres IP jest przydzielany statycznie z podsieci.

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
Określa publiczny obiekt adresu IP, który to polecenie cmdlet skojarzy z frontoniem adresu IP bramy aplikacji.

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
Określa identyfikator publicznego adresu IP, który to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.

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
Określa obiekt podsieci, którą to polecenie cmdlet skojarzy z frontowym adresem IP bramy aplikacji.
Określenie tego parametru oznacza, że brama korzysta z prywatnego adresu IP.
Jeśli parametr *PrivateIPAddress* jest określony, powinien należeć do podsieci określonej przez ten parametr.
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
Określa identyfikator podsieci, którą to polecenie cmdlet skojarzy z konfiguracją frontoronu IP bramy aplikacji.
Określenie parametru *Podsieci* oznacza, że brama korzysta z prywatnego adresu IP.
Jeśli parametr *PrivateIPAddress* jest określony, powinien on należeć do podsieci określonej przez *podsieć.*
Jeśli nie określono adresu *PrivateIPAddress,* jeden z adresów IP z tej podsieci jest dynamicznie wybierany jako pierwszy adres IP bramy aplikacji.

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

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## NOTATKI

## LINKI POKREWNE

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


