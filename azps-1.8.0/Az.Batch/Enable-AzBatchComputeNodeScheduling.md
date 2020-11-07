---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710442"
---
# Enable-AzBatchComputeNodeScheduling

## STRESZCZENIe
Umożliwia planowanie zadań w określonym węźle obliczeniowym.

## POLECENIA

### Identyfikator (domyślnie)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Inputobject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **enable-AzBatchComputeNodeScheduling** umożliwia planowanie zadań w określonym węźle COMPUTE.
Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.

## Przykłady

### Przykład 1: Włączanie planowania zadań w węźle obliczeniowym
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.
W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **enable-AzBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą moja Pula i włączenia planowania zadań w witrynie TVM-1783593343_34-20151117t222514z.

### Przykład 2: Włączanie planowania zadań w węzłach obliczeniowych w puli
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań na wszystkich węzłach obliczeniowych znajdujących się w puli Pool06.
Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.
Ta kolekcja jest następnie **przestawna do polecenia cmdlet Enable-AzBatchComputeNodeScheduling** , które umożliwia planowanie zadań w poszczególnych węzłach obliczeniowych w kolekcji.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

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
Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzBatchComputeNode i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Modele. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


