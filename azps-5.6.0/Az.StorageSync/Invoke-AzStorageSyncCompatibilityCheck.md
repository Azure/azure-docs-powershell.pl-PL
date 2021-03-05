---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002209"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Sprawdza potencjalne problemy ze zgodnością między systemem a usługą Azure File Sync.

## SKŁADNIA

### PathBased (Default)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Invoke-AzStorageSyncCompatibilityCheck** sprawdza, czy nie ma potencjalnych problemów ze zgodnością między systemem a usługą Azure File Sync. Gdy jest to ścieżka lokalna lub zdalna, wykonuje ona zestaw sprawdzania poprawności w przestrzeni nazw systemu i pliku, a następnie zwraca znalezione problemy ze zgodnością.
Testy systemu:
- Sprawdza przestrzeń nazw plików zgodności systemu operacyjnego:
- Nieobsługiwane znaki
- Maksymalny rozmiar pliku
- Maksymalna długość ścieżki
- Maksymalna długość pliku
- Maksymalny rozmiar zestawu danych
- Maksymalna głębokość katalogu

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA.

### Przykład 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

To polecenie sprawdza zgodność plików i folderów w folderze C:\DATA, ale nie sprawdza zgodności systemu.

### Przykład 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA, a następnie eksportuje wyniki jako plik CSV do folderu C:\results.

## PARAMETERS

### — Nazwa_komputera
Komputer, na który jest sprawdzana ta kontrola.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Credential
Poświadczenia dla ważnego udziału.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Ścieżka
Ścieżka UNC dla ważnego udziału.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
Ustaw tę flagę, aby pominąć sprawdzanie poprawności przestrzeni nazw plików i wykonać tylko sprawdzanie poprawności systemu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności przestrzeni nazw plików.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## NOTATKI
* Słowa kluczowe: azure, Az, arm, resource, management, storagesync, filesync

## LINKI POKREWNE
