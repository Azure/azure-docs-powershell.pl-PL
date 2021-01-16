---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368935"
---
# Get-AzBatchJob

## STRESZCZENIe
Pobiera zadania wsadowe dla konta partii lub harmonogramu zadań.

## POLECENIA

### ODataFilter (domyślny)
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Identyfikacji
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Obiekt nadrzędnyobject
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzBatchJob** pobiera zadania wsadowe platformy Azure dla konta wsadowego określonego przez parametr *BatchAccountContext* .
Za pomocą parametru *ID* można uzyskać jedno zadanie.
Za pomocą parametru *Filter* można uzyskać zadania zgodne z filtrem Open Data Protocol (OData).
Jeśli zostanie podany identyfikator harmonogramu zadań lub wystąpienie **PSCloudJobSchedule** , to polecenie cmdlet zwróci tylko zadania dla tego harmonogramu zadań.

## Przykłady

### Przykład 1: uzyskiwanie zadania wsadowego według identyfikatora
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 :
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

To polecenie uzyskuje zadanie o IDENTYFIKATORze Job01.
Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.

### Przykład 2: pobieranie wszystkich aktywnych zadań dla harmonogramu zadań
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

To polecenie pobiera aktywne zadania harmonogramu zadań o IDENTYFIKATORze JobSchedule27.

### Przykład 3: Pobiera wszystkie zadania w harmonogramie zadań przy użyciu potoku.
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule27 przy użyciu polecenia cmdlet Get-AzBatchJobSchedule.
Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie pobiera wszystkie zadania dla tego harmonogramu zadań.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

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
Określa klauzulę filtru OData dla zadań.
Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania dla konta partii lub harmonogramu zadań.

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.
Nie można określać symboli wieloznacznych.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobSchedule
Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadań zawierający zadania.
Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzBatchJobSchedule.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobScheduleId
Określa identyfikator harmonogramu zadań zawierającego zadania.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Określa maksymalną liczbę zadań do zwrócenia.
Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.
Wartość domyślna to 1000.

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## WYSYŁA

### Microsoft.Azure.Commands.Batch. Modele. PSCloudJob

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzBatchJob](./Disable-AzBatchJob.md)

[Enable-AzBatchJob](./Enable-AzBatchJob.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJobSchedule](./Get-AzBatchJobSchedule.md)

[Nowe — AzBatchJob](./New-AzBatchJob.md)

[Remove-AzBatchJob](./Remove-AzBatchJob.md)

[Zatrzymaj — AzBatchJob](./Stop-AzBatchJob.md)

[Polecenia cmdlet usługi Azure Batch](/powershell/module/Az.Batch/)
