---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061877"
---
# Remove-WAPackVMSubnet

## STRESZCZENIe
Usuwa obiekty podsieci maszyny wirtualnej.

## POLECENIA

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Te tematy są przestarzałe i zostaną usunięte w przyszłości.
W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.
Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Remove-WAPackVMSubnet** usuwa obiekty podsieci maszyny wirtualnej.

## Przykłady

### Przykład 1: usuwanie podsieci maszyny wirtualnej
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

Pierwsze polecenie pobiera podsieć maszyny wirtualnej o nazwie ContosoVMSubnet01 przy użyciu polecenia cmdlet **Get-WAPackVMSubnet** , a następnie zapisuje ten obiekt w zmiennej $VMSubnet.

Drugie polecenie usuwa podsieć maszyny wirtualnej przechowywaną w $VMSubnet.
Polecenie wyświetli monit o potwierdzenie.

### Przykład 2: usunięcie maszyny wirtualnej bez potwierdzenia
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoVMSubnet02 przy użyciu polecenia cmdlet **Get-WAPackVMSubnet** , a następnie zapisuje ten obiekt w zmiennej $VMSubnet.

Drugie polecenie usuwa podsieć maszyny wirtualnej przechowywaną w $VMSubnet.
To polecenie zawiera parametr *Force* .
Polecenie nie wyświetla monitu o potwierdzenie.

## PARAMETRÓW

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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

### -VMSubnet
Określa podsieć maszyny wirtualnej.
Aby uzyskać podsieć maszyny wirtualnej, użyj polecenia cmdlet **Get-WAPackVMSubnet** .

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[Nowe — WAPackVMSubnet](./New-WAPackVMSubnet.md)


