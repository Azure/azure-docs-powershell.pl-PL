---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055353"
---
# Add-AzurePHPWorkerRole

## STRESZCZENIe
Tworzy wymagane pliki i konfigurację dla aplikacji PHP, która będzie hostowana na platformie Azure przez php.exe.

## POLECENIA

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Tworzy wymagane pliki i konfigurację, czasami nazywane rusztowami, w aplikacji PHP, która będzie hostowana na platformie Azure przez php.exe.

## Przykłady

### Przykład 1. Tworzenie roli pracownika za pomocą jednego wystąpienia
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

W tym przykładzie dodano wymagane pliki i konfigurację dla jednej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji.

### Przykład 2: tworzenie roli pracownika z wieloma wystąpieniami
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

W tym przykładzie zostaną dodane wymagane pliki i konfiguracja dla nowej roli procesu roboczego w bieżącej aplikacji przy użyciu nazwy MyWorkerRole z liczbą wystąpień roli równą 2.

## PARAMETRÓW

### -Wystąpienia
Określa liczbę wystąpień roli dla tej roli pracownika.
Wartość domyślna to 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę roli pracownika.
Nazwa Określa nazwę folderu zawierającego wymagane pliki i konfigurację dla usługi PHP obsługiwanej w roli procesu roboczego.
Wartość domyślna to WorkerRole1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)

[Dodaj-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


