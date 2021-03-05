---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994512"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Wyłącza planowanie zadań w określonym węźle obliczeniowym.

## SKŁADNIA

### Identyfikator (domyślne)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Disable-AzBatchComputeNodeScheduling** wyłącza planowanie zadań w określonym węźle obliczeniowym.
Węzeł obliczeniowy jest maszyną wirtualną platformy Azure dedykowaną konkretnym obciążeniem aplikacji.
Wyłączenie planowania zadań w węźle obliczeniowym umożliwia również określenie, co należy zrobić w przypadku zadań obecnie w kolejce zadań węzła.
**Disable-AzBatchComputeNodeScheduling** umożliwia: 
- Zakończ zadania i umieść je z powrotem w kolejce zadań.
Dzięki temu te zadania będą ponownieplanowane w innym węźle obliczeniowym. 
- Zakończ zadania i usuń je z kolejki zadań.
Zadania zatrzymane w ten sposób nie będą ponownieplanowane. 
- Poczekaj na ukończenie wszystkich obecnie wykonywanych zadań, a następnie wyłącz planowanie zadań w węźle obliczeniowym. 
- Zaczekaj na ukończenie wszystkich uruchomionych zadań i wygaśnie wszystkie okresy przechowywania danych, a następnie wyłącz planowanie zadań w węźle obliczeniowym.

## PRZYKŁADY

### Przykład 1. Wyłączanie planowania zadań w węźle obliczeniowym
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Te polecenia wyłączyły harmonogram zadań w węźle obliczeniowym tvm-1783593343_34-20151117t222514z.
W tym celu pierwsze polecenie w tym przykładzie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego contosobatchaccount.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie używa następnie tego odwołania do obiektu i polecenia cmdlet **Disable-AzBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą mojej buforu i wyłączenia planowania zadań w węźle tvm-1783593343_34-20151117t222514z.
Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węźle obliczeniowym będą przekierowywane w kolejkę.

### Przykład 2. Wyłączanie planowania zadań we wszystkich węzłach obliczeniowych w puli
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Te polecenia wyłączą planowanie zadań we wszystkich węzłach komputerów w puli partii (Pool06).
Aby wykonać to zadanie, pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu do kluczy konta dla konta wsadowego contosobatchaccount.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie w tym przykładzie używa następnie tego odwołania do obiektu i polecenia **Get-AzBatchComputeNode** w celu zwrócenia kolekcji wszystkich węzłów obliczeniowych znalezionych w pool06.
Ta kolekcja jest następnie przekierowyowana potokowo do polecenia cmdlet **Disable-AzBatchComputeNodeScheduling,** aby wyłączyć planowanie zadań na każdym węźle obliczeniowym w kolekcji.
Parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, ponieważ żadne zadania obecnie uruchomione w węzłach obliczeniowych nie będą kolejkowane.

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
Określa odwołanie do obiektu do węzła obliczeniowego, w którym planowanie zadań jest wyłączone.
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

### -DisableSchedulingOption
Określa sposób, w jaki to polecenie cmdlet obsługuje wszystkie zadania obecnie uruchomione w węźle komputera, w którym planowanie jest wyłączone.
Dopuszczalne wartości dla tego parametru to:
- Kolejkowanie ponownie.
Zadania są natychmiast zatrzymywane i zwracane do kolejki zadań.
Dzięki temu zadania będą ponownieplanowane w innym węźle obliczeniowym.
Jest to wartość domyślna. 
- Zakończ.
Zadania są natychmiast zatrzymywane i usuwane z kolejki zadań.
Te zadania nie zostaną ponownieplanowane. 
- TaskCompletion.
Obecnie uruchomione zadania będą mogły zostać ukończone przed wyłączeniem planowania zadań w węźle obliczeniowym.
W tym węźle nie będą planowane żadne nowe zadania. 
- RetainedData.
Obecnie uruchomione zadania będą mogły wykonywać, a okresy przechowywania danych będą mogły wygasać przed wyłączeniem planowania zadań w węźle obliczeniowym.
W tym węźle nie będą planowane żadne nowe zadania.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Identyfikator
Określa identyfikator węzła obliczeniowego, w którym planowanie zadań jest wyłączone.

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
Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym planowanie zadań jest wyłączone.
W przypadku użycia *parametru PoolId* nie należy używać *parametru ComputeNode* w tym samym poleceniu.

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

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


