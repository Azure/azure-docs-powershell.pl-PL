---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987386"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Dodaje punkt końcowy do obiektu profilu lokalnego menedżera ruchu.

## SKŁADNIA

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzTrafficManagerEndpointConfig** dodaje punkt końcowy do lokalnego obiektu profilu usługi Azure Traffic Manager.
Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.

To polecenie cmdlet działa na lokalnym obiekcie profilu.
Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.
Aby utworzyć punkt końcowy i zatwierdzić zmianę w ramach jednej operacji, użyj New-AzTrafficManagerEndpoint cmdlet.

## PRZYKŁADY

### Przykład 1. Dodawanie punktu końcowego do profilu
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**
Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.

Drugie polecenie powoduje dodanie punktu końcowego o nazwie contoso do profilu przechowywanego w $TrafficManagerProfile.
To polecenie zawiera dane konfiguracji dla punktu końcowego.
To polecenie zmienia tylko obiekt lokalny.

Ostatnie polecenie aktualizuje profil usługi Traffic Manager na platformie Azure w celu dopasowania wartości lokalnej do $TrafficManagerProfile.

## PARAMETERS

### - CustomHeader
Lista niestandardowych par nazw nagłówków i wartości dla żądań zakupu.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -EndpointLocation
Określa lokalizację punktu końcowego do użycia w metodzie routingu ruchu wydajności.
Ten parametr ma zastosowanie tylko do punktów końcowych typu ExternalEndpoints lub NestedEndpoints.
Ten parametr należy określić podczas korzystania z metody routingu ruchu wydajności.

Określ nazwę regionu platformy Azure.
Aby uzyskać pełną listę regionów platformy Azure, zobacz Regiony platformy Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.

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

### -EndpointName
Określa nazwę punktu końcowego Menedżera ruchu, który dodaje to polecenie cmdlet.

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

### -EndpointStatus
Określa stan punktu końcowego.
Prawidłowe wartości to: 

- Włączone 
- Wyłączone 

Jeśli stan jest włączony, punkt końcowy jest prawdopodobny dla kondycji punktu końcowego i jest uwzględniany w metodzie routingu ruchu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — GeoMapping
Lista regionów zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu geograficznego. Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z [dokumentacją menedżera ruchu.](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)

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

### -MinChildEndpoints
Minimalna liczba punktów końcowych, które muszą być dostępne w profilu podrzędnym, aby zagnieżdżony punkt końcowy w profilu nadrzędnym był uznawany za dostępny.
Dotyczy tylko punktu końcowego typu "NestedEndpoints".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Priority (Priorytet)
Określa priorytet przypisywany przez Menedżera ruchu do punktu końcowego.
Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu o priorytecie.
Prawidłowe wartości to liczby całkowite z od 1 do 1000.
Niższe wartości mają wyższy priorytet.

Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.
Jeśli nie określisz priorytetów, menedżer ruchu przypisze domyślne wartości priorytetów do punktów końcowych, zaczynając od jednego (1) w kolejności, w których profil zawiera listę punktów końcowych.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
Lista zakresów adresów lub podsieci zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu "Podsieci".

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — element docelowy
Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.
Menedżer ruchu zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.
Określ ten parametr tylko dla typu punktu końcowego ExternalEndpoints.
W przypadku innych typów punktów końcowych określ zamiast *tego parametr TargetResourceId.*

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

### -TargetResourceId
Określa identyfikator zasobu docelowego.
Określ ten parametr tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.
W przypadku typu punktu końcowego ExternalEndpoints określ zamiast tego *parametr Target.*

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

### -TrafficManagerProfile
Określa lokalny obiekt **TrafficManagerProfile.**
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Wpisz
Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu usługi Azure Traffic Manager.
Prawidłowe wartości to: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Waga
Określa wagę, która zostanie przypisana przez Menedżera ruchu do punktu końcowego.
Prawidłowe wartości to liczby całkowite z od 1 do 1000.
Wartość domyślna to jeden (1).
Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu ważonego.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## NOTATKI

## LINKI POKREWNE

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


