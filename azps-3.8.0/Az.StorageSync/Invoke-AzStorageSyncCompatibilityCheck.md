---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052097"
---
# Invoke-AzStorageSyncCompatibilityCheck

## STRESZCZENIe
Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.

## POLECENIA

### PathBased (domyślny)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Invoke-AzStorageSyncCompatibilityCheck** sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure. W przypadku ścieżki lokalnej lub zdalnej jest ona zbiorem funkcji sprawdzania poprawności w systemie i obszarze nazw plików, a następnie zwraca wszystkie znalezione problemy ze zgodnością.
Testy systemowe:
- Obszar nazw plików zgodności systemu operacyjnego:
- Nieobsługiwane znaki
- Maksymalny rozmiar pliku
- Maksymalna długość ścieżki
- Maksymalna długość pliku
- Maksymalny rozmiar zestawu danych
- Maksymalna głębokość katalogów

## Przykłady

### Przykład 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA.

### Przykład 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

To polecenie sprawdza zgodność plików i folderów w programie C:\DATA, ale nie sprawdza zgodności systemu.

### Przykład 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA, a następnie eksportuje wyniki w postaci pliku CSV do C:\results.

## PARAMETRÓW

### -ComputerName
Komputer, na którym wykonywana jest ta kontrola.

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

### — Poświadczenie
Twoje poświadczenia dla udziału, którego dotyczy Walidacja.

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

### -Path
Ścieżka UNC udziału, którego dotyczy Walidacja.

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
Ustaw tę flagę, aby pominąć sprawdzanie nazw plików i wykonywać tylko sprawdzanie poprawności systemu.

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
Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności nazw plików.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. StorageSync. Evaluation. MODELES. PSValidationResult

## INFORMACYJN
* Słowa kluczowe: Azure, AZ, ARM, Resource, Management, storagesync, FileSync

## LINKI POKREWNE
