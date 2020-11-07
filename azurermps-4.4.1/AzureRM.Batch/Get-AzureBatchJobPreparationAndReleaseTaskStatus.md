---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 6c44688bcd11b624738c299dc04c1a0cb0da9494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719371"
---
# Get-AzureBatchJobPreparationAndReleaseTaskStatus

## STRESZCZENIe
Pobiera zadanie wsadowe i zwalnia stan zadania.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Identyfikator (domyślnie)
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Inputobject
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureBatchJobPreparationAndReleaseTaskStatus** pobiera zadanie usługi Azure Batch dotyczące przygotowania i zwolnienia zadania wsadowego.
Do tego polecenia cmdlet należy podać parametr *identyfikatora* lub wystąpienie **PSCloudJob** .

## Przykłady

### Przykład 1: uzyskiwanie statusu przygotowywania i udostępniania zadania
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

To polecenie pobiera zadanie przygotowywania zadań i zwalnianie stanu zadań dla zadania "test".
Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.

### Przykład 2: Uzyskaj stan przygotowania i udostępniania zadania, korzystając z filtru i wybierz pozycję określony.
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

To polecenie pobiera zadania przygotowywania zadań i zwalniania stanu zadań dla zadania "test" w węźle "TVM-2316545714_1-20170613t201733z" i używa klauzuli SELECT w celu określenia, aby zwracała tylko informacje JobPreparationTaskExecutionInformation

## PARAMETRÓW

### -BatchContext
Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.
Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.

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

### -Expand
Określa klauzulę expanda Open Data Protocol (OData).
Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Określa klauzulę filtru OData.
Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania przygotowywania i zwalniania o stanie zadań dla tego zadania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Określa identyfikator zadania, dla którego mają zostać pobrane zadania przygotowania i wydania.
Nie można określać symboli wieloznacznych.

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

### -Inputobject
Określa obiekt **PSCloudJob** reprezentujący zadanie w celu uzyskania statusu zadania przygotowania i wydania.
Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzureBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Określa maksymalną liczbę zadań przygotowywania i zwalniania statusu zadania, które mają zostać zwrócone.
Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.
Wartość domyślna to 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wybierz pozycję
Określa klauzulę SELECT OData.
Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### System. String
Microsoft.Azure.Commands.Batch. Modele. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext

## WYSYŁA

### Microsoft.Azure.Commands.Batch. Modele. PSJobPreparationAndReleaseTaskExecutionInformation

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Polecenia cmdlet usługi Azure Batch](./AzureRM.Batch.md)
