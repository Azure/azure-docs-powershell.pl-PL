---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054701"
---
# Add-AzureDataDisk

## STRESZCZENIe
Dodaje dysk danych do maszyny wirtualnej.

## POLECENIA

### CreateNew (domyślnie)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Przywoz
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureDataDisk** umożliwia dodanie nowego lub istniejącego dysku danych do obiektu maszyny wirtualnej platformy Azure.
Użyj parametru *CreateNew* , aby utworzyć nowy dysk danych o określonym rozmiarze i etykiecie.
Użyj parametru *Import* , aby dołączyć istniejący dysk z repozytorium obrazów.
Użyj parametru *ImportFrom* , aby dołączyć istniejący dysk z obiektu BLOB na koncie magazynu.
Możesz określić tryb pamięci podręcznej hosta dołączonego dysku danych.

## Przykłady

### Przykład 1: Importowanie dysku danych z repozytorium
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie VirtualMachine07 w usłudze Cloud ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
To polecenie dołącza do maszyny wirtualnej istniejący dysk danych z repozytorium.
Dysk danych ma jednostkę LUN równą 0.
Polecenie powoduje zaktualizowanie maszyny wirtualnej w celu odzwierciedlenia wprowadzonych zmian przy użyciu polecenia cmdlet **Update-AzureVM** .

### Przykład 2: Dodawanie nowego dysku danych
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie VirtualMachine08.
Polecenie przekazuje je do bieżącego polecenia cmdlet.
To polecenie dołącza nowy dysk danych o nazwie MyNewDisk. VHD.
Polecenie cmdlet powoduje utworzenie dysku w kontenerze VHD na domyślnym koncie magazynu bieżącej subskrypcji.
Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.

### Przykład 3: Dodawanie dysku z danymi z określonej lokalizacji
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej o nazwie Database.
Polecenie przekazuje je do bieżącego polecenia cmdlet.
To polecenie dołącza istniejący dysk danych o nazwie Disk14. VHD z określonej lokalizacji.
Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.

## PARAMETRÓW

### -CreateNew
Wskazuje, że to polecenie cmdlet tworzy dysk danych.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Określa etykietę dysku dla nowego dysku danych.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diskname
Określa nazwę dysku z danymi w repozytorium dysków.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Określa rozmiar dysku logicznego (w gigabajtach) dla nowego dysku danych.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Określa ustawienia buforowania na poziomie hosta dla dysku.
Prawidłowe wartości: 

- Znaleziono 
- Odczytu 
- ReadWrite

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

### — Importowanie
Wskazuje, że to polecenie cmdlet importuje istniejący dysk danych z repozytorium obrazów.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Wskazuje, że to polecenie cmdlet importuje istniejący dysk danych z obiektu BLOB na koncie magazynu.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LUN
Określa logiczny numer jednostki (LUN) dla dysku z danymi na maszynie wirtualnej.
Prawidłowe wartości to: od 0 do 15.
Każdy dysk z danymi musi mieć unikatową jednostkę LUN.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Określa lokalizację obiektu BLOB na koncie usługi Azure Storage, w którym to polecenie cmdlet przechowuje dysk danych.
Jeśli nie podano lokalizacji, polecenie cmdlet zapisuje dysk danych w kontenerze VHD na domyślnym koncie magazynu dla bieżącej subskrypcji.
Jeśli kontener wirtualnych dysków twardych nie istnieje, polecenie cmdlet tworzy kontener dysków VHD.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
Określa obiekt maszyny wirtualnej, do którego to polecenie cmdlet dołącza dysk danych.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureVM** .

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


