---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 281e8a883474b3cb0f42b22de1bb00ef2f6e7249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524602"
---
# Disable-AzureBatchComputeNodeScheduling

## STRESZCZENIe
Wyłącza planowanie zadań w określonym węźle obliczeniowym.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Identyfikator (domyślnie)
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Inputobject
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **disable-AzureBatchComputeNodeScheduling** wyłącza planowanie zadań w określonym węźle COMPUTE.
Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.
Po wyłączeniu planowania zadań w węźle obliczeniowym dostępna jest również opcja określająca, co należy zrobić w kolejce zadań węzła.
**Disable-AzureBatchComputeNodeScheduling** umożliwia wykonywanie następujących czynności: 
- Zakończ zadania i umieść je z powrotem w kolejce zadań.
Dzięki temu zadania mogą być ponownie planowane w innym węźle obliczeniowym. 
- Kończenie zadań i usuwanie ich z kolejki zadań.
Zadania zatrzymane w ten sposób nie będą ponownie planowane. 
- Poczekaj na ukończenie wszystkich zadań, które są obecnie wykonywane, a następnie wyłącz planowanie zadań w węźle obliczeniowym. 
- Poczekaj na ukończenie wszystkich uruchomionych zadań, a wszystkie okresy przechowywania danych wygasną, a następnie wyłącz planowanie zadań w węźle obliczeniowym.

## Przykłady

### Przykład 1. wyłączenie planowania zadań w węźle obliczeniowym
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Te polecenia wyłączają harmonogram zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.
W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **disable-AzureBatchComputeNodeScheduling** , aby połączyć się z pulą moja Pula i wyłączyć planowanie zadań w węźle TVM-1783593343_34-20151117t222514z.
Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węźle obliczeniowym zostaną ponownie przekolejkowane.

### Przykład 2: wyłączenie planowania zadań we wszystkich węzłach obliczeniowych w puli
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

Te polecenia wyłączają planowanie zadań na wszystkich węzłach komputerów w Pool06 puli partii.
Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.
Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzureBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.
Ta kolekcja jest następnie **przełączana do polecenia cmdlet Disable-AzureBatchComputeNodeScheduling** , aby wyłączyć planowanie zadań w każdym węźle obliczeniowym w kolekcji.
Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węzłach obliczeniowych zostaną ponownie przekolejkowane.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

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
Określa odwołanie obiektu do węzła obliczeniowego, w którym jest wyłączone planowanie zadań.
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

### -DisableSchedulingOption
Określa, jak to polecenie cmdlet dotyczy wszystkich zadań uruchomionych obecnie w węźle komputera, na którym jest wyłączone planowanie.
Dopuszczalne wartości tego parametru to:
- Przekolejkowanie.
Zadania zostaną natychmiast zatrzymane i zwrócone do kolejki zadań.
Umożliwia to ponowne planowanie zadań w innym węźle obliczeniowym.
Jest to wartość domyślna. 
- Zakończyć.
Zadania są natychmiast przetrzymywane i usuwane z kolejki zadań.
Te zadania nie zostaną zaplanowane ponownie. 
- TaskCompletion.
Obecnie uruchomione zadania będą mogły zostać ukończone przed wyłączeniem planowania zadań w węźle obliczeniowym.
Żadne nowe zadania nie będą planowane w tym węźle. 
- RetainedData.
Obecnie uruchomione zadania będą mogły zostać ukończone, a okres przechowywania danych będzie mógł wygasnąć, zanim planowanie zadań zostanie wyłączone w węźle obliczeniowym.
Żadne nowe zadania nie będą planowane w tym węźle.

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

### -ID
Określa identyfikator węzła obliczeniowego, w którym jest wyłączone planowanie zadań.

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
Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest wyłączone planowanie zadań.
Jeśli używasz parametru *PoolId* , nie używaj parametru *ComputeNode* w tym samym poleceniu.

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
Parametry: ComputeNode (ByValue)

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Parametry: BatchContext (ByValue)

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Enable-AzureBatchComputeNodeScheduling](./Enable-AzureBatchComputeNodeScheduling.md)


