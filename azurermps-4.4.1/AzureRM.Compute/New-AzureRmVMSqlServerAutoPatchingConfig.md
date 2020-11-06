---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553975"
---
# New-AzureVMSqlServerAutoPatchingConfig

## STRESZCZENIe
Tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.

## Przykłady

### Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

To polecenie tworzy obiekt konfiguracji do tworzenia poprawek.
Polecenie określa dzień tygodnia i definiuje okno obsługi.
Ta konfiguracja umożliwia stosowanie poprawek korzystających z tych wartości.
Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.
Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.

## PARAMETRÓW

### -Enable
Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.
Jeśli włączysz automatyczne poprawianie, polecenie cmdlet przełączy system Windows do trybu interakcyjnego.
Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmieniają się.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DayOfWeek
Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.

Dopuszczalne wartości tego parametru to:

- Niedziele
- Poniedziałek
- Wtorku
- Środa
- Czwartek
- Poniedziałek
- Sobota
- Codzienne

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

### -MaintenanceWindowStartingHour
Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.
Ten czas określa, kiedy aktualizacje rozpoczną instalację.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Określa czas trwania okna konserwacji (w minutach).
Automatyczne poprawianie nie pozwala na wykonywanie akcji, które mogą wpłynąć na dostępność maszyny wirtualnej poza tym oknem.
Określ wielokrotność 30 minut.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Określa, czy należy uwzględnić ważne aktualizacje.

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

### -InformationAction
@ {Text =}

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@ {Text =}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

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

### AutoPatchingSettings
To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


