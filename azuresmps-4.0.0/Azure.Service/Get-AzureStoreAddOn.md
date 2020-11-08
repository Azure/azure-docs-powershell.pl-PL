---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054513"
---
# Get-AzureStoreAddOn

## STRESZCZENIe
Pobiera dostępne dodatki ze Sklepu Azure.

## POLECENIA

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Getdodatków
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Pobiera wszystkie dostępne dodatki na potrzeby zakupu ze Sklepu Azure Store lub pobiera istniejące wystąpienia dodatków dla bieżącej subskrypcji.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureStoreAddOn
```

W tym przykładzie są pobierane wszystkie zakupione wystąpienia dodatków dla bieżącej subskrypcji.

### Przykład 2
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

W tym przykładzie są pobierane wszystkie dostępne dodatki dotyczące zakupu w Stanach Zjednoczonych ze Sklepu Azure.

### Przykład 3
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

W tym przykładzie jest pobierany dodatek o nazwie Moje oddodatek z zakupionego wystąpienia dodatku w bieżącej subskrypcji.

## PARAMETRÓW

### -Country
Jeśli ta funkcja jest określona, zwraca tylko wystąpienia dodatków ze Sklepu Azure dostępne w określonym kraju.
Wartość domyślna to "my".

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
Jeśli ta usługa jest określona, pobieraj dostępne dodatki do zakupu w Sklepie Azure.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Zwraca dodatek zgodny z określoną nazwą.

```yaml
Type: String
Parameter Sets: GetAddOn
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

[Nowe — AzureStoreAddOn](./New-AzureStoreAddOn.md)

[Remove-AzureStoreAddOn](./Remove-AzureStoreAddOn.md)

[Set-AzureStoreAddOn](./Set-AzureStoreAddOn.md)


