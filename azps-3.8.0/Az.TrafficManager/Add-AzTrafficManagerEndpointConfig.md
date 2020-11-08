---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050618"
---
# Add-AzTrafficManagerEndpointConfig

## STRESZCZENIe
Dodaje punkt końcowy do obiektu profilu lokalnego zarządzania ruchem.

## POLECENIA

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzTrafficManagerEndpointConfig** umożliwia dodanie punktu końcowego do obiektu profilu lokalnego usługi Azure Traffic Manager.
Możesz uzyskać profil przy użyciu New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile poleceń cmdlet.

To polecenie cmdlet działa na obiekcie profilu lokalnego.
Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.
Aby utworzyć punkt końcowy i przekazać zmianę w ramach jednej operacji, użyj polecenia cmdlet New-AzTrafficManagerEndpoint.

## Przykłady

### Przykład 1. Dodawanie punktu końcowego do profilu
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .
Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.

Drugie polecenie dodaje punkt końcowy o nazwie contoso do profilu przechowywanego w $TrafficManagerProfile.
Polecenie uwzględnia dane konfiguracji punktu końcowego.
To polecenie powoduje zmianę tylko obiektu lokalnego.

Ostatnie polecenie aktualizuje profil usługi Traffic managera na platformie Azure, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.

## PARAMETRÓW

### -CustomHeader
Lista niestandardowych par nazw nagłówków i wartości dla żądań sondujące.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.
Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.
Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.

Określ nazwę regionu platformy Azure.
Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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
Określa nazwę punktu końcowego usługi Traffic Managera, który jest dodawany przez to polecenie cmdlet.

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
Prawidłowe wartości: 

- Wyłączona 
- Łącza 

Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.

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

### -Geomapowanie
Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny". Aby uzyskać [pełną listę zaakceptowanych wartości](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions), zapoznaj się z dokumentacją w usłudze Traffic Manager.

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
Minimalna liczba punktów końcowych, które muszą być dostępne w profilu podrzędnym, aby zagnieżdżony punkt końcowy w profilu nadrzędnym był uważany za dostępny.
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

### -Priority (priorytet)
Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.
Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.
Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.
Niższe wartości reprezentują wyższy priorytet.

Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.
Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.

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
Lista zakresów adresów lub podsieci zamapowanych do tego punktu końcowego podczas korzystania z metody routingu ruchu "podsieci".

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

### -Target
Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.
Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.
Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.
W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .

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
Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.
W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .

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
Określa lokalny obiekt **TrafficManagerProfile** .
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.

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

### -Type
Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Azure Traffic Manager.
Prawidłowe wartości: 

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

### -Waga
Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.
Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.
Wartość domyślna to jeden (1).
Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## WYSYŁA

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## INFORMACYJN

## LINKI POKREWNE

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Nowe — AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


