---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055513"
---
# Get-AzureVM

## STRESZCZENIe
Pobiera informacje z jednej lub większej liczby maszyn wirtualnych platformy Azure.

## POLECENIA

### ListAllVMs (domyślny)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureVM** pobiera informacje o maszynach wirtualnych uruchomionych na platformie Azure.
Zwraca obiekt z informacjami na określonej maszynie wirtualnej lub jeśli nie jest określona żadna maszyna wirtualna, dla wszystkich maszyn wirtualnych w określonej usłudze bieżącej subskrypcji.

## Przykłady

### Przykład 1: pobieranie informacji na określonej maszynie wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

To polecenie zwraca obiekt z informacjami na maszynie wirtualnej VirtualMachine02 działającej w chmurze usługi ContosoService01.

### Przykład 2: pobieranie informacji na wszystkich maszynach wirtualnych
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

To polecenie pobiera obiekt listy z informacjami na wszystkich maszynach wirtualnych uruchomionych w usłudze Cloud ContosoService01.

### Przykład 3: wyświetlanie tabeli stanu maszyny wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

To polecenie wyświetla tabelę zawierającą maszyny wirtualne uruchomione w usłudze ContosoService01, ich domenę uaktualnienia i bieżący stan każdej maszyny wirtualnej.

## PARAMETRÓW

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

### -Name (nazwa)
Określa nazwę maszyny wirtualnej, dla której mają zostać pobrane informacje.
Jeśli ten parametr nie zostanie podany, polecenie cmdlet zwraca obiekt listy z informacją o wszystkich maszynach wirtualnych w określonej usłudze.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
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

### -ServiceName
Określa nazwę usługi w chmurze, dla której mają zostać zwrócone informacje o maszynie wirtualnej.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
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

[Nowe — AzureVM](./New-AzureVM.md)

[Nowe — AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start — AzureVM](./Start-AzureVM.md)

[Zatrzymaj — AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


