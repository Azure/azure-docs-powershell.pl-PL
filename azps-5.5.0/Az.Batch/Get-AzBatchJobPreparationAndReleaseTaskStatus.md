---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239394"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Pobiera stan zadań wsadowych i zwalniania zadań.

## SKŁADNIA

### Identyfikator (domyślne)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzBatchJobPreparationAndReleaseTaskStatus** pobiera zadanie wsadowe platformy Azure i stan zadania wsadowego dla zadania wsadowego.
Do tego  polecenia cmdlet należy podać parametr Id lub wystąpienie usługi **PSCloudJob.**

## PRZYKŁADY

### Przykład 1. Uzyskiwanie przygotowania do pracy i stanu zwolnienia stanowiska
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

To polecenie pobiera informacje o przygotowaniu zadania i zwolnieniu stanu zadania dla zadania "Test".
Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.

### Przykład 2. Uzyskiwanie informacji o przygotowaniu stanowiska i zwolnieniu go za pomocą opcji Filtruj i Wybierz
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

To polecenie pobiera informacje o przygotowaniu zadania i zwolnieniu stanu zadania "Test" w węźle "tvm-2316545714_1-20170613t201733z" i używa klauzuli Select w celu zwrócenia tylko informacji JobPreparationTaskExecutionInformation

## PARAMETERS

### - BatchContext
Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą batch.
Użyj Get-AzBatchAccountKey cmdlet, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.

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

### — Rozwiń
Określa klauzulę rozwijania protokołu Open Data (OData).
Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej o otrzymuję.

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

### — Filtr
Określa klauzulę filtru OData.
Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie informacje o przygotowaniu zadania i zwolnieniu stanu zadania.

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

### — Id
Określa identyfikator zadania, którego zadania związane z przygotowaniem i wydaniem powinny zostać pobrane.
Nie można określić symboli wieloznacznych.

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

### -InputObject
Określa obiekt **PSCloudJob** reprezentujący zadanie w celu uzyskania przygotowania i zwolnienia stanu zadania.
Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.

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
Określa maksymalną liczbę zadań do zwrócenia podczas przygotowywania i zwalniania stanu zadania.
Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.
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

### — Wybierz
Określa klauzulę wybierania danych OData.
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
