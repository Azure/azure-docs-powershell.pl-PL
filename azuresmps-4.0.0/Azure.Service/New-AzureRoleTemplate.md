---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054958"
---
# New-AzureRoleTemplate

## STRESZCZENIe
Tworzy szablony ról witryny sieci Web i procesu roboczego.

## POLECENIA

### Rola
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **New-AzureRoleTemplate** tworzy szablony ról sieci Web i procesu roboczego.

## Przykłady

### Przykład 1. Tworzenie szablonu roli sieci Web
```
PS C:\> New-AzureRoleTemplate -Web
```

W tym przykładzie jest tworzony nowy szablon roli sieci Web w folderze o nazwie WebRoleTemplate w bieżącym katalogu.

### Przykład 2: Tworzenie szablonu roli pracownika
```
PS C:\> New-AzureRoleTemplate -Worker
```

W tym przykładzie jest tworzony nowy szablon roli procesu roboczego w folderze o nazwie WebRoleTemplate w bieżącym katalogu.

### Przykład 3: Tworzenie szablonu roli w katalogu niestandardowym
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

W tym przykładzie jest tworzony nowy szablon roli sieci Web w katalogu o nazwie MyWebRoleTemplate, a nie w bieżącym katalogu.

## PARAMETRÓW

### — Dane wyjściowe
Określa ścieżkę wyjściową utworzonego szablonu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Web
Określa, że chcesz utworzyć szablon roli sieci Web.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pracownik
Określa, że chcesz utworzyć szablon roli pracownika.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureWebRole](./Add-AzureWebRole.md)

[Dodaj-AzureWorkerRole](./Add-AzureWorkerRole.md)


