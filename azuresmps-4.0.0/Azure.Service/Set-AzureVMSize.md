---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054757"
---
# Set-AzureVMSize

## STRESZCZENIe
Ustawia rozmiar maszyny wirtualnej platformy Azure.

## POLECENIA

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureVMSize** umożliwia zaktualizowanie rozmiaru maszyny wirtualnej.
Ma dwa parametry: *InstanceSize* , czyli nowy rozmiar maszyny wirtualnej, a *maszyna* wirtualna, która jest obiektem maszyny wirtualnej pobrana przy użyciu polecenia cmdlet **Get-AzureVM** .
Wynik polecenia **Set-AzureVMSize można przetworzyć** do polecenia cmdlet **Update-AzureVM** lub zapisać w zmiennej do późniejszego użycia.
Rzeczywista zmiana nie jest wprowadzana do momentu wykonania instrukcji **Update-AzureVM** .

Uwaga: to polecenie cmdlet wymaga ponownego udostępnienia maszyny wirtualnej i może otrzymać nowy adres IP.

## Przykłady

### Przykład 1: Ustawianie rozmiaru maszyny wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

To polecenie umożliwia zaktualizowanie maszyny wirtualnej w celu zmiany rozmiaru "mały".

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

### -InstanceSize
Określa rozmiar maszyny wirtualnej.

Dopuszczalne wartości tego parametru to:

--ExtraSmall--mały--medium--Large--ExtraLarge--A5--A6--

```yaml
Type: String
Parameter Sets: (All)
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

### -VM
Określa trwały obiekt maszyny wirtualnej, w którym ten aplet cmdlet ustawia rozmiar.

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

[Get-AzureVM](./Get-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


