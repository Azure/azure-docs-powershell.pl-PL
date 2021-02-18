---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181562"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Tworzy obiekt konfiguracji na celu automatyczne poprawianie poprawek na komputerze wirtualnym.

## SKŁADNIA

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji do automatycznego poprawiania na komputerze wirtualnym.

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznego poprawiania poprawek
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

To polecenie tworzy obiekt konfiguracji na celu tworzenie poprawek.
To polecenie określa dzień tygodnia i definiuje okno konserwacji.
Ta konfiguracja umożliwia tworzenie poprawek, w których są używane te wartości.
Polecenie przechowuje wynik w $AutoBackupConfig zmienną.
Ten element konfiguracji można określić dla innych pozycji cmdlet, takich jak polecenie cmdlet Set-AzVMSqlServerExtension cmdlet.

## PARAMETERS

### -DayOfWeek
Określa dzień tygodnia, w którym mają być instalowane aktualizacje.
Dopuszczalne wartości dla tego parametru to:
- Niedziela
- Poniedziałek
- Wtorek
- Środa
- Czwartek
- Piątek
- Sobota
- Codzienne czynności

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Włącz
Oznacza, że włączono automatyczne poprawianie poprawek dla maszyny wirtualnej.
Włączenie automatycznego poprawiania za pomocą polecenia cmdlet włącza usługę Windows Update w tryb interakcyjny.
Wyłączenie automatycznego poprawiania nie powoduje zmiany ustawień usługi Windows Update.

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

### -MaintenanceWindowDuration
Określa czas trwania (w minutach) okna konserwacji.
Automatyczne poprawianie pozwala uniknąć wykonywania akcji, która może mieć wpływ na dostępność maszyny wirtualnej poza tym oknem.
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

### -MaintenanceWindowStartingHour
Określa godzinę dnia, w którym rozpoczyna się okno konserwacji.
Ten czas określa, kiedy rozpocznie się instalowanie aktualizacji.

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

### - PatchCategory
Określa, czy należy uwzględniać ważne aktualizacje.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## NOTATKI

## LINKI POKREWNE

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


