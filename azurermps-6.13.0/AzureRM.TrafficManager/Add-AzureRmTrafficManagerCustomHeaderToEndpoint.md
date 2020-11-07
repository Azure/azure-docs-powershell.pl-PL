---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719053"
---
# Add-AzureRmTrafficManagerCustomHeaderToEndpoint

## STRESZCZENIe
Dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego lokalnego zarządzania ruchem.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego usługi Azure Local Manager.
Punkt końcowy można uzyskać przy użyciu New-AzureRmTrafficManagerEndpoint lub Get-AzureRmTrafficManagerEndpoint poleceń cmdlet.

To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.
Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.

## Przykłady

### Przykład 1: Dodawanie niestandardowych informacji nagłówka do punktu końcowego
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzureRmTrafficManagerEndpoint** .
Polecenie zapisuje lokalny punkt końcowy w zmiennej $TrafficManagerEndpoint.
Drugie polecenie dodaje niestandardowe informacje nagłówka do punktu końcowego przechowywanego w $TrafficManagerEndpoint.
Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę informacji nagłówka niestandardowego, które mają zostać dodane.

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

### -TrafficManagerEndpoint
Określa lokalny obiekt **TrafficManagerEndpoint** .
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint lub New-AzureRmTrafficManagerEndpoint.

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

### -Value
Określa wartość niestandardowych informacji nagłówka, które mają zostać dodane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet.

## WYSYŁA

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerEndpoint** .

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[Nowe — AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
