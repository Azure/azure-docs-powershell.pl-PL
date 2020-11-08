---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055243"
---
# Get-AzureVNetGatewayDiagnostics

## STRESZCZENIe
Pobiera bieżący stan diagnostyki bramy sieci wirtualnej.

## POLECENIA

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureVNetGatewayDiagnostics** Pobiera bieżący stan diagnostyki bramy sieci wirtualnej.
Jeśli obiekt BLOB (Binary Large Object) istnieje w miejscu, w którym na **początku AzureVNetGatewayDiagnostics** Zapisano poprzednią sesję diagnostyczną, to polecenie cmdlet zwróci również adres URL obiektu BLOB, w którym polecenie cmdlet jest zapisane w tej sesji diagnostycznej.

## Przykłady

## PARAMETRÓW

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla której to polecenie cmdlet pobiera diagnostykę.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Start — AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)

[Zatrzymaj — AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


