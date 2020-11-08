---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055358"
---
# Add-AzureNodeWebRole

## STRESZCZENIe
Tworzy wymagane pliki i foldery dla aplikacji Node.js.

## POLECENIA

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

W **dodatku Add-AzureNodeWebRole** są tworzone wymagane pliki i foldery, czasami nazywane rusztowaniem, aby aplikacja Node.js była hostowana w chmurze za pośrednictwem usług IIS.

## Przykłady

### Przykład 1: rola sieci Web pojedynczego wystąpienia
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

W tym przykładzie dodano rusztowania dla jednej roli sieci Web o nazwie **MyWebRole** do bieżącej aplikacji.

### Przykład 2: rola sieci Web o wielu wystąpieniach
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

W tym przykładzie dodano rusztowania dla nowej roli sieci Web o nazwie **MyWebRole** do bieżącej aplikacji z liczbą wystąpień roli równą 2.

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
Określa również nazwę katalogu zawierającego rusztowania dla aplikacji node.js, która będzie hostowana w roli sieci Web.
Wartość domyślna to webrola #, gdzie # wskazuje liczbę ról sieci Web w usłudze.

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

[Dodaj-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)


