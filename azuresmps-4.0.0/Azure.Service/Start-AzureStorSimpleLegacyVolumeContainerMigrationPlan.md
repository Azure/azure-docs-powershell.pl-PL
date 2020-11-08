---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054739"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## STRESZCZENIe
Rozpoczynanie tworzenia planu migracji.

## POLECENIA

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** rozpoczyna Tworzenie planu migracji.
Tworzenie planu migracji jest asynchroniczne.
Aby sprawdzić stan planu migracji, użyj polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .

## Przykłady

### Przykład 1. Rozpocznij plan migracji
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

To polecenie rozpoczyna Tworzenie planu migracji dla starszego kontenera o nazwie OneSDKAzureCloud.
Polecenie zwraca wiadomość o stanie planu i używa polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** w celu uzyskania aktualnych informacji.

### Przykład 2: Rozpoczynanie planu migracji dla wszystkich kontenerów woluminów
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

To polecenie rozpoczyna Tworzenie planu migracji dla wszystkich starszych kontenerów woluminów w importowanym pliku konfiguracji.

## PARAMETRÓW

### -All
Wskazuje, że to polecenie cmdlet rozpoczyna Szacowanie czasu migracji dla wszystkich kontenerów woluminów w zaimportowanym pliku konfiguracji.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Określa unikatowy identyfikator starszego urządzenia.

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

### -LegacyContainerNames
Określa tablicę nazw kontenerów woluminów, dla których ma zostać utworzony plan migracji.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
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

### Znaleziono

## WYSYŁA

### Ciąg
To polecenie cmdlet zwraca stan zadania planu migracji, jeśli zostało pomyślnie uruchomione na urządzeniu.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


