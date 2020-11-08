---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061822"
---
# Get-WAPackVMOSDisk

## STRESZCZENIe
Pobiera obiekty dyskowe systemu operacyjnego dla maszyn wirtualnych.

## POLECENIA

### Empty (domyślnie)
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Odname
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Te tematy są przestarzałe i zostaną usunięte w przyszłości.
W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.
Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Get-WAPackVMOSDisk** Pobiera obiekty dysku systemu operacyjnego dla maszyn wirtualnych.

## Przykłady

### Przykład 1: uzyskiwanie dysku z systemem operacyjnym przy użyciu nazwy
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

To polecenie uzyskuje dysk z systemem operacyjnym o nazwie ContosoOSDisk.

### Przykład 2: uzyskiwanie dysku z systemem operacyjnym przy użyciu identyfikatora
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

To polecenie pobiera dysk z systemem operacyjnym o określonym IDENTYFIKATORze.

### Przykład 3: uzyskiwanie wszystkich dysków z systemem operacyjnym
```
PS C:\> Get-WAPackVMOSDisk
```

To polecenie pobiera wszystkie dyski z systemem operacyjnym.

## PARAMETRÓW

### -ID
Określa unikatowy identyfikator dysku systemu operacyjnego.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę dysku systemu operacyjnego.

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-WAPackVM](./Get-WAPackVM.md)


