---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 3a97562c775c901e8226d1dc5a0b9d090f8f70cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892802"
---
# Set-AzExpressRouteCircuitPeeringConfig

## STRESZCZENIe
Zapisuje zmodyfikowaną konfigurację komunikacji równorzędnej ExpressRoute.

## POLECENIA

### SetByResource (domyślny)
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### MicrosoftPeeringConfigRoutFilterId
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### MicrosoftPeeringConfigRoutFilter
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenia cmdlet **Set-AzExpressRouteCircuitPeeringConfig** umożliwiają powrót do platformy Azure zmodyfikowanej konfiguracji równorzędnej usługi ExpressRoute.

## Przykłady

### Przykład 1. Zmienianie istniejącej konfiguracji komunikacji równorzędnej
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -ExpressRouteCircuit
Obiekt obwodu ExpressRoute zawierający konfigurację komunikacji równorzędnej do zmodyfikowania.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Legacymode
Starszy tryb komunikacji równorzędnej

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MicrosoftConfigAdvertisedPublicPrefixes
W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP. Akceptowane są tylko publiczne prefiksy adresów IP. Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów. Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigCustomerAsn
Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigRoutingRegistryName
Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.

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

### -Name (nazwa)
Nazwa konfiguracji komunikacji równorzędnej do zmodyfikowania.

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

### -PeerAddressType
PeerAddressType

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PeerASN
Numer AS obwodu ExpressRoute. To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringType
Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryPeerAddressPrefix
Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej. To musi być podsieć CIDR/30. Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera. Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.

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

### -RouteFilter
To jest istniejący obiekt RouteFilter.

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteFilterId
Jest to identyfikator zasobu istniejącego obiektu RouteFilter.

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryPeerAddressPrefix
Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej. To musi być podsieć CIDR/30. Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera. Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.

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

### -SharedKey
Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.

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

### -VlanId
Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSExpressRouteCircuit
Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzExpressRouteCircuitPeeringConfig](Add-AzExpressRouteCircuitPeeringConfig.md)

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)

[Nowe — AzExpressRouteCircuitPeeringConfig](New-AzExpressRouteCircuitPeeringConfig.md)

[Remove-AzExpressRouteCircuitPeeringConfig](Remove-AzExpressRouteCircuitPeeringConfig.md)
