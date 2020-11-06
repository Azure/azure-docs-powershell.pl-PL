---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 8e3633e88bc3c0972df0d667ed1002571d5ec142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527094"
---
# Get-AzureBatchSubtask

## STRESZCZENIe
Pobiera informacje podzadania określonego zadania.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ODataFilter (domyślny)
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Obiekt nadrzędnyobject
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureBatchSubtask** pobiera informacje podzadania określonego zadania.
Podzadania zapewniają równoległą obróbkę poszczególnych zadań i umożliwiają precyzyjne monitorowanie wykonywania i postępu zadań.

## Przykłady

### Przykład 1. zwraca wszystkie podzadania dla określonego zadania.
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

Te polecenia zwracają wszystkie podzadania zadania z IDENTYFIKATORem moje zadanie.
W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.

Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzureBatchSubtask** , aby zwrócić wszystkie podzadania zadania podzadania, zadanie uruchamiane w ramach zadania zlecenia-01.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Określa identyfikator zadania zawierającego zadanie, którego podzadania są dostępne.

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Określa maksymalną liczbę podzadań, które należy zwrócić.
Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.
Wartość domyślna to 1000.

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

### — Zadanie
Określa odwołanie do obiektu zadania, które zawiera podzadania zwrócone przez to polecenie cmdlet.
Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzureBatchTask i przechowywania zwróconego obiektu w zmiennej.

```yaml
Type: PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Określa identyfikator zadania, którego podzadania są zwracane przez ten aplet polecenia.

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BatchAccountContext
Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu

### PSCloudTask
Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.

## WYSYŁA

###  
To polecenie cmdlet zwraca wystąpienia obiektu **PSSubtaskInformation** .

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureBatchTask](./Get-AzureBatchTask.md)


