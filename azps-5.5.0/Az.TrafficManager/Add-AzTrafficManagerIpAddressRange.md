---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198315"
---
# Add-AzTrafficManagerIpAddressRange

## SYNOPSIS
Dodaje zakres adresu lub podsieci do lokalnego obiektu końcowego menedżera ruchu.

## SKŁADNIA

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzTrafficManagerIpAddressRange** dodaje zakres adresów IP do lokalnego obiektu końcowego usługi Azure Traffic Manager.
Punkt końcowy można uzyskać za pomocą New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint cmdlet.

To polecenie cmdlet działa na lokalnym obiekcie punktu końcowego.
Zatwierdzanie zmian w punkcie końcowym usługi Traffic Manager za pomocą Set-AzTrafficManagerEndpoint cmdlet.

## PRZYKŁADY

### Przykład 1. Dodawanie zakresów adresów IP do punktu końcowego
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzTrafficManagerEndpoint.**
Polecenie przechowuje lokalny punkt końcowy w $TrafficManagerEndpoint zmienną.
Drugie polecenie dodaje zakres adresów IP od 1.2.3.4 do 5.6.7.8 do punktu końcowego przechowywanego w $TrafficManagerEndpoint.
Trzecie polecenie dodaje zakres adresów IP od 9.10.11.0 do 9.10.11.255 do punktu końcowego przechowywanego w $TrafficManagerEndpoint.
Czwarte polecenie sprawdza, czy zakres jest taki, jak rozmiar zakresu, a następnie dodaje zakres adresów IP od 12.13.14.0 do 12.13.14.31 do punktu końcowego przechowywanego w programie $TrafficManagerEndpoint.
Piąte polecenie dodaje zakres adresu IP od 15.16.17.18 do punktu końcowego 15.16.17.18 do punktu końcowego przechowywanego w $TrafficManagerEndpoint.
Ostatnie polecenie aktualizuje punkt końcowy w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerEndpoint.

## PARAMETERS

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

### — Ostatnie
Określa ostatni adres IP w zakresie, który ma zostać dodany.

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

### — Zakres
Określa zakres zakresu adresów IP do dodania.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Określa lokalny **obiekt TrafficManagerEndpoint.**
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### — Najpierw
Określa pierwszy adres IP w zakresie, który ma zostać dodany.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTATKI

## LINKI POKREWNE

[Remove-AzTrafficManagerIpAddressRange](./Remove-AzTrafficManagerIpAddressRange.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
