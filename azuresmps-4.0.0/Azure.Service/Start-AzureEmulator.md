---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054997"
---
# Start-AzureEmulator

## STRESZCZENIe
Uruchamia emulatory obliczeniowe i magazynowe.

## POLECENIA

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Start-AzureEmulator** uruchamia zarówno emulatory obliczeniowe, jak i magazynowe oraz hostuje bieżącą usługę w emulatorze obliczeniowym.

## Przykłady

### Przykład 1. Uruchom emulator i uruchom przeglądarkę
```
PS C:\> Start-AzureEmulator -L
```

W tym przykładzie usługa jest uruchamiana w emulatorze Azure i uruchamia nowe okno przeglądarki w emulowanej usłudze.

## PARAMETRÓW

### -Uruchom
Otwiera nowe okno przeglądarki w usłudze po jej umieszczeniu w emulatorze.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mode (tryb)
Określa tryb emulatora.
Prawidłowe wartości to: Full i Express.
Wartość domyślna to ekspresowa.

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)

[Publikowanie — AzureServiceProject](./Publish-AzureServiceProject.md)

[Zatrzymaj — AzureEmulator](./Stop-AzureEmulator.md)


