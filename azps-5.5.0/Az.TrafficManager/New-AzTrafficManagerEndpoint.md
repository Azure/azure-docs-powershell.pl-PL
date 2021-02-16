---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195514"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Tworzy punkt końcowy w profilu Menedżera ruchu.

## SKŁADNIA

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.

To polecenie cmdlet zatwierdza każdy nowy punkt końcowy w usłudze Traffic Manager.
Aby dodać wiele punktów końcowych do obiektu profilu lokalnego menedżera ruchu i zatwierdzić zmiany w ramach jednej operacji, użyj Add-AzTrafficManagerEndpointConfig cmdlet.

## PRZYKŁADY

### Przykład 1. Tworzenie zewnętrznego punktu końcowego profilu
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

To polecenie tworzy zewnętrzny punkt końcowy o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie Grupa Zasobów11.

### Przykład 2. Tworzenie punktu końcowego platformy Azure dla profilu
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

To polecenie tworzy punkt końcowy platformy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów ResourceGroup11.
Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Azure Resource Manager jest podawany przez ścieżkę URI *w identyfikatorze TargetResourceId.*
To polecenie nie określa *parametru EndpointLocation,* ponieważ zasób aplikacji Sieci Web dostarcza lokalizację.

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
Lista regionów zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu geograficznego. Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją menedżera ruchu.

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

### - MinChildEndpoints
Określ nazwę regionu platformy Azure.
Aby uzyskać pełną listę regionów platformy Azure, zobacz Regiony platformy Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.

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

### — Nazwa
Określa nazwę punktu końcowego Menedżera ruchu, który tworzy to polecenie cmdlet.

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

### -ProfileName
Określa nazwę profilu menedżera ruchu, do którego to polecenie cmdlet dodaje punkt końcowy.
Aby uzyskać profil, użyj New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.

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
To polecenie cmdlet tworzy punkt końcowy Menedżera ruchu w grupie, która określa ten parametr.

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

### — Wpisz
Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu Menedżera ruchu.
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
Określa wagę przypisywaną przez Menedżera ruchu do punktu końcowego.
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

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTATKI

## LINKI POKREWNE

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


