---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054707"
---
# Stop-AzureVM

## STRESZCZENIe
Zamykanie maszyny wirtualnej platformy Azure.

## POLECENIA

### ByName (domyślny)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Wprowadzone
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureVM** zamyka maszynę wirtualną.

## Przykłady

### Przykład 1: zamykanie maszyny wirtualnej
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

To polecenie zamyka maszynę wirtualną, którą zawiera określona usługa.

### Przykład 2: zamykanie maszyny wirtualnej za pomocą obiektu maszyny wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera, przy użyciu obiektu maszyna wirtualna, który zwraca **-AzureVM** .

### Przykład 3: zamykanie maszyny wirtualnej i zachowywanie zainicjowanej obsługi maszyny wirtualnej
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera, i utrzymuje jej obsługę administracyjną.

### Przykład 4: zamykanie maszyny wirtualnej i Zezwalanie na przydział ostatniej maszyny wirtualnej we wdrożeniu
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera i zezwala na oddzielenie ostatniej maszyny wirtualnej we wdrożeniu.

### Przykład 5: zamykanie wielu maszyn wirtualnych
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

To polecenie zamyka wiele maszyn wirtualnych, które zawiera określona usługa.

## PARAMETRÓW

### -Force
Określa, czy należy zezwolić na oddzielenie ostatniej maszyny wirtualnej we wdrożeniu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -Name (nazwa)
Określa nazwę maszyny wirtualnej do zamknięcia.

Używanie znaku wieloznacznego do asynchronicznego zatrzymywania wielu maszyn wirtualnych.
W przypadku symboli wieloznacznych to polecenie cmdlet wywołuje operację role zamknięcia https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) zamiast operacji roli Shutdown https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
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
Określa nazwę usługi platformy Azure zawierającej maszynę wirtualną do zamknięcia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Określa, że w tym poleceniu cmdlet jest zachowywana obsługa administracyjna maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej wskazujący, że maszyna wirtualna zostanie zamknięta.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
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

[Get-AzureVM](./Get-AzureVM.md)

[Nowe — AzureVM](./New-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start — AzureVM](./Start-AzureVM.md)


