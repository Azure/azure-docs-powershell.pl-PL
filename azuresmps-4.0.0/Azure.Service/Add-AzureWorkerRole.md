---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054676"
---
# Add-AzureWorkerRole

## STRESZCZENIe
Tworzy wymagane pliki i konfigurację dla niestandardowej roli pracownika.

## POLECENIA

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Add-AzureWorkerRole** tworzy wymagane pliki i konfigurację, czasami nazywane rusztowaniem, dla niestandardowej roli pracownika.

## Przykłady

### Przykład 1. Tworzenie roli pracownika jednego wystąpienia
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

W tym przykładzie dodano rusztowania dla jednej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji.

### Przykład 2: tworzenie roli pracownika wielu wystąpień
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

W tym przykładzie dodano rusztowania dla nowej roli pracownika o nazwie MyWorkerRole do bieżącej aplikacji z liczbą wystąpień roli równą 2.

### Przykład 3: tworzenie roli pracownika przy użyciu szkieletu niestandardowego
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

W tym przykładzie jest tworzona rola pracownika z niestandardową rusztowaniem.

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
Ta wartość określa nazwę folderu, który zawiera rusztowania dla aplikacji niestandardowej, która będzie obsługiwana w roli pracownika.
Wartość domyślna to WorkerRolenumber, gdzie liczba jest liczbą ról procesu roboczego w usłudze.

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

### -TemplateFolder
Określa folder szablonu rusztowania, który ma być wykorzystywany do tworzenia roli pracownika.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Dodaj-AzureWebRole](./Add-AzureWebRole.md)

[Nowe — AzureRoleTemplate](./New-AzureRoleTemplate.md)


