---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524129"
---
# Set-AzureStorageServiceLoggingProperty

## STRESZCZENIe
Modyfikuje rejestrowanie w usłudze Azure Storage Services.

## POLECENIA

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageServiceLoggingProperty** modyfikuje rejestrowanie usług Azure Storage Services.

## Przykłady

### Przykład 1: modyfikowanie właściwości rejestrowania usługi BLOB
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

To polecenie modyfikuje w wersji 1,0 rejestrowanie w magazynie obiektów blob, aby uwzględnić operacje odczytu i zapisu.
Rejestrowanie usługi Azure Storage Service zachowuje wpisy przez 10 dni.
Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla zmodyfikowane właściwości rejestrowania.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.

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

### -LoggingOperations
Określa tablicę operacji usługi Azure Storage.
Usługa Azure Storage Services rejestruje operacje, które ten parametr określa.
Dopuszczalne wartości tego parametru to:

- Znaleziono
- Czytał
- Wpisywan
- Usuwać
- Cały

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Wskazuje, że to polecenie cmdlet zwraca zaktualizowane właściwości rejestrowania.
Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.

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

### -RetentionDays
Określa liczbę dni przechowywania zarejestrowanych informacji w usłudze Azure Storage.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Określa typ usługi magazynu.
To polecenie cmdlet modyfikuje właściwości rejestrowania dla typu usługi, który ten parametr określa.
Dopuszczalne wartości tego parametru to:

- Obiektów BLOB 
- Tworząc
- Wykonany
- Plik

Wartość pliku nie jest obecnie obsługiwana.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Określa wersję rejestrowania usługi Azure Storage.
Wartość domyślna to 1,0.

```yaml
Type: Double
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

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[Nowe — AzureStorageContext](./New-AzureStorageContext.md)


