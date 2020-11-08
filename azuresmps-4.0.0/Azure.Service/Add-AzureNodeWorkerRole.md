---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055355"
---
# Add-AzureNodeWorkerRole

## STRESZCZENIe
Tworzy wymagane pliki i foldery aplikacji Node.js, która ma być hostowana w chmurze za pośrednictwem node.exe

## POLECENIA

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Add-AzureNodeWorkerRole** tworzy wymagane pliki i foldery, czasami nazywane rusztowaniem, aby aplikacja Node.js mogła być hostowana w chmurze za pośrednictwem node.exe.

## Przykłady

### Przykład 1: rola pracownika pojedynczego wystąpienia
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

W tym przykładzie dodano rusztowania dla jednej roli pracownika o nazwie **MyWorkerRole** do bieżącej aplikacji.

### Przykład 2: rola procesu roboczego wielu wystąpień
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

W tym przykładzie dodano szkielety dla jednej roli pracownika o nazwie **MyWorkerRole** do bieżącej aplikacji z liczbą wystąpień roli równą 2.

## PARAMETRÓW

### -Wystąpienia
Określa liczbę wystąpień roli dla tej roli pracownika.
Domyślnie jest to 1.

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
Wartość określa nazwę folderu, który zawiera rusztowania dla usługi node.js obsługiwanej w roli procesu roboczego.
Domyślna to WorkerRole1.

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

[Dodaj-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)


