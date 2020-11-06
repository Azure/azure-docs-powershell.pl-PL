---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: b460eb4377f06cfa7348f06cdd60f2013e5b5e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527073"
---
# Start-AzureBatchPoolResize

## STRESZCZENIe
Rozpoczynanie zmieniania rozmiaru puli.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureBatchPoolResize** rozpoczyna operację zmiany rozmiaru wsadu Azure Part na puli.

## Przykłady

### Przykład 1: Zmienianie rozmiaru puli na 12 węzłów
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

To polecenie rozpoczyna operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.
Elementem docelowym tej operacji jest 12 dedykowanych węzłów obliczeniowych.
Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.

### Przykład 2: Zmienianie rozmiaru puli przy użyciu opcji dealokacji
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

To polecenie cmdlet umożliwia zmienianie rozmiaru puli na pięć dedykowanych węzłów obliczeniowych.
Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzureBatchPool.
Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie rozpoczyna operację zmiany rozmiaru w puli.
Celem jest pięć dedykowanych węzłów obliczeniowych.
To polecenie określa czas trwania jednej godziny.
Polecenie określa opcję rozdzielania, którą można zakończyć.

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

### -ComputeNodeDeallocationOption
Określa opcję dealokacji dla operacji zmiany rozmiaru, która zostanie uruchomiona przez to polecenie cmdlet.

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ID
Określa identyfikator puli, której rozmiar tego polecenia cmdlet zmienia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResizeTimeout
Określa okres limitu czasu dla operacji zmiany rozmiaru.
Jeśli pula nie dociera do rozmiaru docelowego, operacja zmiany rozmiaru zostaje zatrzymana.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDedicatedComputeNodes
Liczba dedykowanych węzłów obliczeniowych docelowych.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetLowPriorityComputeNodes
Liczba docelowych węzłów obliczeniowych o niskim priorytecie.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BatchAccountContext
Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu

### Ciąg
Parametr "ID" akceptuje wartość typu "String" z procesu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Zatrzymaj — AzureBatchPoolResize](./Stop-AzureBatchPoolResize.md)

[Polecenia cmdlet usługi Azure Batch](./AzureRM.Batch.md)


