---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 007fb7a309b9dd305f58d2f947d3d2dfc55078e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707368"
---
# New-AzTrafficManagerEndpoint

## STRESZCZENIe
Tworzy punkt końcowy w profilu w usłudze Traffic Manager.

## POLECENIA

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.

To polecenie cmdlet umożliwia przekazanie każdego nowego punktu końcowego do usługi Traffic Manager.
Aby dodać wiele punktów końcowych do obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Add-AzTrafficManagerEndpointConfig.

## Przykłady

### Przykład 1. Tworzenie zewnętrznego punktu końcowego dla profilu
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

To polecenie powoduje utworzenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.

### Przykład 2: Tworzenie punktu końcowego Azure dla profilu
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

To polecenie tworzy punkt końcowy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.
Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Menedżera zasobów Azure jest określony przez ścieżkę URI w *TargetResourceId*.
Polecenie nie określa parametru *EndpointLocation* , ponieważ zasób aplikacji sieci Web udostępnia lokalizację.

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
Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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
Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny". Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją w usłudze Traffic Manager.

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
Określ nazwę regionu platformy Azure.
Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -Name (nazwa)
Określa nazwę punktu końcowego usługi Traffic Managera, który jest tworzony przez to polecenie cmdlet.

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

### -Refilename
Określa nazwę profilu usługi Traffic Manager, do którego to polecenie cmdlet dodaje punkt końcowy.
Aby uzyskać profil, Użyj poleceń cmdlet New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile.

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

### -ResourceGroupName
Określa nazwę grupy zasobów.
To polecenie cmdlet powoduje utworzenie punktu końcowego zarządzania ruchem w grupie, którą ten parametr określa.

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

### -SubnetMapping
Lista zakresów adresów lub podsieci zamapowanych do tego punktu końcowego w przypadku korzystania z metody routingu ruchu sieciowego â € ̃Subnetâ €™.

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

### -Type
Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Nowe — AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


