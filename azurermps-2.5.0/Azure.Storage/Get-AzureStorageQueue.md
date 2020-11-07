---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899417"
---
# Get-AzureStorageQueue

## STRESZCZENIe
Zawiera listę kolejek przechowywania.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### QueueName (domyślnie)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageQueue** zawiera listę kolejek magazynowania skojarzonych z kontem usługi Azure Storage.

## Przykłady

### Przykład 1. Lista wszystkich kolejek w usłudze Azure Storage
```
PS C:\>Get-AzureStorageQueue
```

To polecenie powoduje wyświetlenie listy wszystkich kolejek magazynu dla bieżącego konta magazynu.

### Przykład 2: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu znaku wieloznacznego
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek przechowywania, których nazwy zaczynają się od kolejki.

### Przykład 3: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

W tym przykładzie użyto parametru *prefix* , aby uzyskać listę kolejek przechowywania, których nazwy zaczynają się od kolejki.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Możesz ją utworzyć przy użyciu polecenia cmdlet **New-AzureStorageContext** .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę.
Jeśli nie podano nazwy, polecenie cmdlet powoduje wyświetlenie listy wszystkich kolejek.
Jeśli jest określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Określa prefiks, którego nazwy są używane w nazwach kolejek, które chcesz pobrać.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


