---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055356"
---
# Add-AzurePHPWebRole

## STRESZCZENIe
Tworzy wymagane pliki i konfigurację dla aplikacji PHP.

## POLECENIA

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Add-AzurePHPWebRole** tworzy pliki i konfigurację, czasami nazywane rusztowaniem, dla aplikacji PHP, która będzie hostowana na platformie Azure za pośrednictwem internetowych usług informacyjnych.

## Przykłady

### Przykład 1: Dodawanie roli w sieci Web przy użyciu wartości domyślnych
```
PS C:\> Add-AzurePHPWebRole
```

W tym przykładzie dodano wymagane pliki i konfigurację dla nowej roli w sieci Web przy użyciu wartości domyślnych usługi o nazwie "WebRole1" z jedną instancją.

### Przykład 2: Dodawanie roli sieci Web z wieloma wystąpieniami
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

W tym przykładzie zostaną dodane wymagane pliki i konfiguracja nowej roli sieci Web w bieżącej aplikacji przy użyciu nazwy "MyWebRole" i liczby wystąpień roli 2.

## PARAMETRÓW

### -Wystąpienia
Określa liczbę wystąpień roli dla tej roli sieci Web.
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
Określa nazwę roli sieci Web.
Nazwa Określa nazwę katalogu zawierającego wymagane pliki i konfigurację dla aplikacji PHP.
Wartość domyślna to webrola #, gdzie # to liczba ról sieci Web w usłudze.

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

[Dodaj-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)


