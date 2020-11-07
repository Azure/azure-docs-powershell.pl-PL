---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 3cbe0a4e0276f2b62a0e0aed5b6168a5b81f8d7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719484"
---
# Set-AzureStorageServiceMetricsProperty

## STRESZCZENIe
Modyfikuje właściwości metryk dla usługi Azure Storage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.

## Przykłady

### Przykład 1: modyfikowanie właściwości metryk dla usługi BLOB
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

To polecenie modyfikuje metryki w wersji 1,0 dla magazynu obiektów BLOB na poziom usług.
Metryki usługi Azure Storage są zachowywanie wpisów przez 10 dni.
Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla właściwości zmodyfikowano metryki.

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

### -MetricsLevel
Określa poziom metryk używany dla usługi Azure Storage.
Dopuszczalne wartości tego parametru to:

- Znaleziono
- Służby
- ServiceAndApi

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metryki
Określa typ metryk.
Ten cmldet ustawia wartość typu metryki usługi Azure Storage na wartość określaną przez ten parametr.
Dopuszczalne wartości tego parametru to: godzina i minuta.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Wskazuje, że te polecenia cmdlet zwracają zaktualizowane właściwości metryk.
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
Określa liczbę dni przechowywania informacji o metrykach w usłudze Azure Storage.

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
To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, którego ten parametr określa.
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
Określa wersję metryk magazynu platformy Azure.
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

### IStorageContext

Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku

## WYSYŁA

### Microsoft. platformy windowsazure. Storage. Shared. Protocol. MetricsProperties

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[Nowe — AzureStorageContext](./New-AzureStorageContext.md)


