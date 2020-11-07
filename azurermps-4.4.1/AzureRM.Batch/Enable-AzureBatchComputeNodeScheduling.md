---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718558"
---
# Enable-AzureBatchComputeNodeScheduling

## STRESZCZENIe
Umożliwia planowanie zadań w określonym węźle obliczeniowym.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Identyfikator (domyślnie)
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Inputobject
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **enable-AzureBatchComputeNodeScheduling** umożliwia planowanie zadań w określonym węźle COMPUTE.
Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.

## Przykłady

### Przykład 1: Włączanie planowania zadań w węźle obliczeniowym
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.
W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.

Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **enable-AzureBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą moja Pula i włączenia planowania zadań w witrynie TVM-1783593343_34-20151117t222514z.

### Przykład 2: Włączanie planowania zadań w węzłach obliczeniowych w puli
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań na wszystkich węzłach obliczeniowych znajdujących się w puli Pool06.
Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.

Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzureBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.
Ta kolekcja jest następnie **przestawna do polecenia cmdlet Enable-AzureBatchComputeNodeScheduling** , które umożliwia planowanie zadań w poszczególnych węzłach obliczeniowych w kolekcji.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Określa odwołanie obiektu do węzła obliczeniowego, w którym jest włączone planowanie zadań.
Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzureBatchComputeNode i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ID
Określa identyfikator węzła obliczeniowego, w którym jest włączone planowanie zadań.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest włączone planowanie zadań.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BatchAccountContext
Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu

### PSComputeNode
Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzureBatchComputeNodeScheduling](./Disable-AzureBatchComputeNodeScheduling.md)


