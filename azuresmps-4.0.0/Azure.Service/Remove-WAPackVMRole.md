---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061881"
---
# Remove-WAPackVMRole

## STRESZCZENIe
Usuwa obiekty roli maszyny wirtualnej.

## POLECENIA

### FromVMRoleObject (domyślny)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Te tematy są przestarzałe i zostaną usunięte w przyszłości.
W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.
Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Remove-WAPackVMRole** usuwa obiekty roli maszyny wirtualnej.

## Przykłady

### Przykład 1: Usuwanie roli maszyny wirtualnej (utworzonej za pomocą portalu WAP)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Pierwsze polecenie uzyskuje rolę maszyny wirtualnej o nazwie ContosoVMRole01 przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.

Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.
Polecenie wyświetli monit o potwierdzenie. Zakładając, że ta rola maszyny wirtualnej została utworzona za pomocą portalu WAP, nie trzeba określać nazwy usługi w chmurze.

### Przykład 2: Usuwanie roli maszyny wirtualnej utworzonej po ręcznym utworzeniu usługi w chmurze
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Pierwsze polecenie uzyskuje rolę maszyny wirtualnej o nazwie "ContosoVMRole02" przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.

Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.
Polecenie wyświetli monit o potwierdzenie.
Zakładając, że ta rola maszyny wirtualnej nie została utworzona za pomocą portalu, użytkownik musi określić nazwę usługi w chmurze.
W tym przypadku o nazwie "ContosoCloudService02".

### Przykład 3: Usuwanie roli maszyny wirtualnej bez potwierdzenia
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoVMRole03 przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.

Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.
To polecenie zawiera parametr *Force* .
Polecenie nie wyświetla monitu o potwierdzenie.

## PARAMETRÓW

### -CloudServiceName
Określa nazwę usługi w chmurze dla roli maszyna wirtualna.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -VMRole
Określa rolę maszyny wirtualnej.
Aby uzyskać rolę maszyny wirtualnej, użyj polecenia cmdlet **Get-WAPackVMRole** .

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Nowe — WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


