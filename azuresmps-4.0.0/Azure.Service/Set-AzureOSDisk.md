---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054794"
---
# Set-AzureOSDisk

## STRESZCZENIe
Modyfikuje tryb pamięci podręcznej hosta maszyny wirtualnej platformy Azure.

## POLECENIA

### Noresize
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Resize
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureOSDisk** modyfikuje tryb pamięci podręcznej hosta na dysku systemu operacyjnego maszyny wirtualnej platformy Azure.
Obsługiwane tryby pamięci podręcznej hosta są tylko do odczytu i ReadWrite.
Uruchomienie tego polecenia cmdlet na maszynie wirtualnej, która jest uruchomiona, powoduje ponowne uruchomienie maszyny wirtualnej.

## Przykłady

### Przykład 1: Ustawianie trybu pamięci podręcznej hosta na wartość ReadOnly za pomocą potoku
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine02 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet ustawia tryb pamięci podręcznej hosta na dysku systemu operacyjnego tej maszyny wirtualnej jako tylko do odczytu.

### Przykład 2: Ustawianie trybu pamięci podręcznej hosta na ReadWrite
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine02 w usłudze o nazwie ContosoService, a następnie zapisuje ją w zmiennej.

Drugie polecenie ustawia tryb pamięci podręcznej hosta na dysku z systemem operacyjnym tej maszyny wirtualnej na ReadWrite.

## PARAMETRÓW

### -HostCaching
Określa atrybut pamięć podręczna hosta dla dysku systemu operacyjnego.
Prawidłowe wartości: 

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
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
Określa nowy rozmiar dysku systemu operacyjnego (w gigabajtach).
Rozmiar musi być większy niż bieżący rozmiar.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Określa maszynę wirtualną, dla której to polecenie cmdlet modyfikuje dysk systemu operacyjnego.
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

[Dodaj-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


