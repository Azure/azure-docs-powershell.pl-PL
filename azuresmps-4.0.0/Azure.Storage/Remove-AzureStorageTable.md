---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710678"
---
# Remove-AzureStorageTable

## STRESZCZENIe
Usuwa tabelę magazynu.

## POLECENIA

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureStorageTable** usuwa co najmniej jeden magazyn z konta magazynu na platformie Azure.

## Przykłady

### Przykład 1. Usuwanie tabeli
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

To polecenie umożliwia usunięcie tabeli.

### Przykład 2: Usuwanie kilku tabel
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

W tym przykładzie użyto symbolu wieloznacznego z parametrem *name* w celu uzyskania wszystkich tabel pasujących do tabeli wzorzec, a następnie przekazanie wyniku w potoku w celu usunięcia tabel.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Name (nazwa)
Określa nazwę tabeli, która ma zostać usunięta.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.
Domyślnie to polecenie cmdlet nie zwraca wartości.

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

[Get-AzureStorageTable](./Get-AzureStorageTable.md)
