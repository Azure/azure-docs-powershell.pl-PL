---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995723"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Umożliwia planowanie zadań w określonym węźle obliczeniowym.

## SKŁADNIA

### Identyfikator (domyślne)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Enable-AzBatchComputeNodeScheduling** umożliwia planowanie zadań w określonym węźle obliczeniowym.
Węzeł obliczeniowy jest maszyną wirtualną platformy Azure dedykowaną konkretnym obciążeniem aplikacji.

## PRZYKŁADY

### Przykład 1. Włączanie planowania zadań w węźle obliczeniowym
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań w węźle obliczeniowym tvm-1783593343_34-20151117t222514z.
W tym celu pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu zawierające klucze konta dla konta wsadowego contosobatchaccount.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie używa następnie tego odwołania do obiektu i polecenia cmdlet **Enable-AzBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą myPool i włączenia planowania zadań w programie tvm-1783593343_34-20151117t222514z.

### Przykład 2. Włączanie planowania zadań w węzłach obliczeniowych w puli
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Te polecenia umożliwiają planowanie zadań we wszystkich węzłach obliczeniowych w puli Pula06.
Aby wykonać to zadanie, pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu zawierające klucze konta dla konta wsadowego contosobatchaccount.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie w tym przykładzie używa następnie tego odwołania do obiektu i polecenia **Get-AzBatchComputeNode** w celu zwrócenia kolekcji wszystkich węzłów obliczeniowych znalezionych w pool06.
Ta kolekcja jest następnie przekierowyowana potokowo do polecenia cmdlet **Enable-AzBatchComputeNodeScheduling,** które umożliwia planowanie zadań w każdym węźle obliczeniowym w kolekcji.

## PARAMETERS

### - BatchContext
Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.
Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory. Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu. Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany. Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.

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
Określa odwołanie do obiektu do węzła obliczeniowego, w którym jest włączone planowanie zadań.
To odwołanie do obiektu jest tworzone przy użyciu Get-AzBatchComputeNode cmdlet i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Identyfikator
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

### - PoolId
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


