---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054666"
---
# Confirm-AzureStorSimpleLegacyVolumeContainerStatus

## STRESZCZENIe
Inicjuje przekazywanie lub wycofywanie kontenerów woluminów, które zostały zmigrowane.

## POLECENIA

### MigrateSpecificContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** inicjuje przekazywanie lub wycofywanie kontenerów woluminów, które są migrowane w ramach migracji starszej wersji.
Przywracanie przywraca pierwotnemu właścicielowi urządzenia.
Zlecenie przypisuje własność docelowemu urządzeniu.

## Przykłady

### Przykład 1. Rozpoczynanie operacji zatwierdzania na określonym kontenerze woluminów
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

To polecenie inicjuje operację commit na określonym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.
Aby wyświetlić stan operacji, użyj polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** .

### Przykład 2: Inicjowanie operacji wycofywania na określonym kontenerze woluminów
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

To polecenie inicjuje operację wycofywania na określonym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.

### Przykład 3: Inicjowanie operacji zatwierdzania dla wszystkich kontenerów woluminów
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

To polecenie inicjuje operację commit na całym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.

### Przykład 4: zainicjowanie operacji wycofywania dla wszystkich kontenerów woluminów
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

To polecenie inicjuje operację wycofywania na wszystkich kontenerach woluminów dla określonego identyfikatora konfiguracji starszego typu.

## PARAMETRÓW

### -All
Wskazuje, że to polecenie cmdlet Inicjuje operację wycofywania lub zatwierdzania dla wszystkich kontenerów woluminów w zaimportowanym pliku konfiguracji.

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
Określa tablicę nazw kontenerów woluminów, dla których obowiązuje plan migracji.

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

### -MigrationOperation
Określa, czy to polecenie cmdlet wykonuje zatwierdzenie lub wycofanie.
Prawidłowe wartości to: Commit i Rollback.

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

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


