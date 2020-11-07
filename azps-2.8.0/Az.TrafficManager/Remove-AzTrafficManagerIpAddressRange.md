---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: ea69e8d07278be2c9f122d179090e63b9153128d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888461"
---
# Remove-AzTrafficManagerIpAddressRange

## STRESZCZENIe
Usuwa zakres adresów lub podsieć z obiektu punktu końcowego lokalnego zarządzania ruchem.

## POLECENIA

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzTrafficManagerIpAddressRange** usuwa zakres adresów IP z obiektu punktu końcowego lokalnego programu Azure Endpoint Manager.
Punkt końcowy można uzyskać przy użyciu New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint poleceń cmdlet.

To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.
Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzTrafficManagerEndpoint.

## Przykłady

### Przykład 1: usuwanie zakresów adresów IP z punktu końcowego
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Pierwsze polecenie uzyskuje punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.
Drugie polecenie usuwa zakres adresów IP z punktu końcowego przechowywanego w $TrafficManagerEndpoint.
Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.

## PARAMETRÓW

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

### -TrafficManagerEndpoint
Określa lokalny obiekt **TrafficManagerEndpoint** .
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

### -First
Określa pierwszy adres IP z zakresu, który ma zostać usunięty.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint

## WYSYŁA

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzTrafficManagerIpAddressRange](./Add-AzTrafficManagerIpAddressRange.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Nowe — AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
