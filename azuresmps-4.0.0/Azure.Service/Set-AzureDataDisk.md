---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055032"
---
# Set-AzureDataDisk

## STRESZCZENIe
Modyfikuje buforowanie hosta istniejącego dysku danych na maszynie wirtualnej platformy Azure.

## POLECENIA

### Noresize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Resize
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureDataDisk** modyfikuje atrybuty pamięci podręcznej istniejącego dysku danych na maszynie wirtualnej platformy Azure.
Określ, który dysk danych ma zostać zaktualizowany za pomocą numeru jednostki logicznej (LUN).

## Przykłady

### Przykład 1. Modyfikowanie buforowania hosta dla dysku z danymi
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

To polecenie pobiera maszyny wirtualne uruchomione w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie cmdlet ustawia dysk danych w jednostkach LUN 2 maszyny wirtualnej o nazwie VirtualMachine07, aby używać buforowania hosta ReadOnly.
Polecenie powoduje zaktualizowanie maszyny wirtualnej w celu odzwierciedlenia wprowadzonych zmian przy użyciu polecenia cmdlet **Update-AzureVM** .

### Przykład 2: modyfikowanie buforowania hosta dla wszystkich dysków z danymi na maszynie wirtualnej
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

To polecenie pobiera obiekt maszyny wirtualnej o nazwie VirtualMachine07 w chmurze usługi ContosoService.
Polecenie przekazuje je do polecenia cmdlet **Get-AzureDataDisk** , które pobiera dyski danych dla tej maszyny wirtualnej.
Bieżące polecenie cmdlet ustawia tryb buforowania hosta każdego z dysków z danymi na ReadWrite.
Polecenie aktualizuje maszynę wirtualną, aby odzwierciedlić wprowadzone zmiany.

## PARAMETRÓW

### -Diskname
Określa nazwę konfiguracji dysku danych, którą to polecenie cmdlet modyfikuje.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> Buforowanie dysków nie jest obsługiwane w przypadku dysków 4 TiB i większych. Jeśli do maszyny wirtualnej jest podłączonych wiele dysków, każdy dysk o rozmiarze mniejszym niż 4 TiB będzie obsługiwać buforowanie.
>
> Zmiana ustawienia pamięci podręcznej dysku Azure powoduje odłączenie i ponowne załączenie dysku docelowego. Jeśli jest to dysk systemu operacyjnego, maszyna wirtualna zostanie ponownie uruchomiona. Przed zmianą ustawienia pamięci podręcznej dysku Zatrzymaj wszystkie aplikacje/usługi, które mogą być dotknięte tym zakłóceniem. Obserwowanie tych rekomendacji może spowodować uszkodzenie danych.

Określa ustawienia buforowania na poziomie hosta dla dysku.
Prawidłowe wartości:

- Znaleziono
- Odczytu
- ReadWrite

```yaml
Type: String
Parameter Sets: NoResize
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
Określa jednostkę LUN dla dysku danych na maszynie wirtualnej.
Prawidłowe wartości to: od 0 do 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
Określa nowy rozmiar (w gigabajtach) dysku danych.
Nowy rozmiar musi być większy niż bieżący rozmiar.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej dołączony do dysku z danymi.
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

[Dodaj-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


