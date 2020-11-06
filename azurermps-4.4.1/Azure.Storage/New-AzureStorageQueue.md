---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554247"
---
# New-AzureStorageQueue

## STRESZCZENIe
Umożliwia utworzenie kolejki magazynu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorageQueue** tworzy kolejkę magazynowania na platformie Azure.

## Przykłady

### Przykład 1. Tworzenie kolejki magazynu platformy Azure
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.

### Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.
Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.

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

### -Name (nazwa)
Określa nazwę kolejki.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### IStorageContext

Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku

### Ciąg

Parametr "nazwa" akceptuje wartość typu "String" z procesu

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


