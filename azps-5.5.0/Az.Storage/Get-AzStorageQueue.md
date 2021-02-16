---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178195"
---
# Get-AzStorageQueue

## SYNOPSIS
Lista kolejek magazynu.

## SKŁADNIA

### QueueName (Domyślna)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageQueue** wyświetla kolejki magazynu skojarzone z kontem usługi Azure Storage.

## PRZYKŁADY

### Przykład 1. Lista wszystkich kolejek magazynu platformy Azure
```
PS C:\>Get-AzStorageQueue
```

To polecenie pobiera listę wszystkich kolejek magazynu dla bieżącego konta magazynu.

### Przykład 2. Lista kolejek magazynu platformy Azure przy użyciu symbolu wieloznacznego
```
PS C:\>Get-AzStorageQueue -Name queue*
```

To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek magazynu, których nazwa rozpoczyna się od kolejki.

### Przykład 3. Lista kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

W tym przykładzie użyto *parametru Prefiks* w celu uzyskania listy kolejek magazynu, których nazwa rozpoczyna się od kolejki.

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Możesz go utworzyć za pomocą polecenia cmdlet **New-AzStorageContext.**

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Określa nazwę.
Jeśli nie zostanie określona żadna nazwa, polecenie cmdlet pobiera listę wszystkich kolejek.
Jeśli zostanie określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.

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

### — Prefiks
Określa prefiks używany w nazwie kolejek, które mają zostać naniesiene.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## NOTATKI

## LINKI POKREWNE

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


