---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324730"
---
# New-AzStorageQueue

## STRESZCZENIe
Umożliwia utworzenie kolejki magazynu.

## POLECENIA

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzStorageQueue** tworzy kolejkę magazynowania na platformie Azure.

## Przykłady

### Przykład 1. Tworzenie kolejki magazynu platformy Azure
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.

### Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.
Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę kolejki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## INFORMACYJN

## LINKI POKREWNE

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


