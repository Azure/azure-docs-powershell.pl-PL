---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054992"
---
# Start-AzureVNetGatewayDiagnostics

## STRESZCZENIe
Rozpoczyna diagnostykę bramy dla bramy VPN.

## POLECENIA

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureVNetGatewayDiagnostics** rozpoczyna nową sesję diagnostyczną bramy dla bramy wirtualnej sieci prywatnej (VPN).
W danej chwili może być uruchomiona tylko jedna sesja diagnostyki bramy.
Jeśli uruchomisz to polecenie cmdlet, gdy sesja diagnostyki bramy jest uruchomiona, to polecenie cmdlet zwróci błąd.

## Przykłady

## PARAMETRÓW

### -CaptureDurationInSeconds
Określa czas trwania przechwytywania w sekundach.

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

### -ContainerName
Określa nazwę kontenera platformy Azure.
To polecenie cmdlet przechowuje wyniki w kontenerze, który określa ten parametr.

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

### -StorageContext
Określa kontekst usługi Azure Storage.
To polecenie cmdlet przechowuje wyniki, korzystając z kontekstu magazynu określanego przez ten parametr.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla którego to polecenie cmdlet wykonuje testy diagnostyczne.

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

[Get-AzureVNetGatewayDiagnostics](./Get-AzureVNetGatewayDiagnostics.md)

[Zatrzymaj — AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


