---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330838"
---
# Get-AzMigrateJob

## STRESZCZENIe
Pobiera stan zadania migracji platformy Azure.

## POLECENIA

### ListByName (domyślny)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzMigrateJob retrives stan zadania migracji platformy Azure.

## Przykłady

### Przykład 1. Poproś o identyfikator zadania
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Spowoduje to pobranie zadania o jego identyfikatorze.

### Przykład 2: Wyświetlanie listy według grupy zasobów i projektu
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Spowoduje to odpobieranie wszystkich zadań w projekcie.

### Przykład 3: Pobierz według grupy zasobów, projektu i nazwy zadania
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Spowoduje to wyświetlenie określonego zadania.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Opcje filtru OData.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Określa obiekt zadania serwera replikowanego.
Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobID
Określa identyfikator zadania, dla którego należy pobrać dane.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Identyfikator zadania

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
Określa projekt migracji platformy Azure, w którym są replikowane serwery.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NazwaProjektu
Nazwa projektu migracji.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
Określa grupę zasobów projektu migracji platformy Azure w bieżącej subskrypcji.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Identyfikator subskrypcji platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IJob> : określa obiekt zadania serwera replikowanego.
  - `[Location <String>]`: Lokalizacja zasobu
  - `[ActivityId <String>]`: Identyfikator aktywności.
  - `[AllowedAction <String[]>]`: Dozwolone działanie zadania.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Uwzględnione właściwości obiektu, takie jak serwer źródłowy, Chmura źródłowa, serwer docelowy, Chmura docelowa itd., na podstawie szczegółów obiektu przepływu pracy.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[EndTime <DateTime?>]`: Godzina zakończenia.
  - `[Error <IJobErrorDetails[]>]`: Błędy.
    - `[CreationTime <DateTime?>]`: Czas utworzenia błędu zadania.
    - `[ErrorLevel <String>]`: Błąd poziomu błędu.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Kod błędu.
    - `[ProviderErrorDetailErrorId <String>]`: Identyfikator błędu dostawcy.
    - `[ProviderErrorDetailErrorMessage <String>]`: Komunikat o błędzie.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu usunięcia błędu.
    - `[ServiceErrorDetailActivityId <String>]`: Identyfikator aktywności.
    - `[ServiceErrorDetailCode <String>]`: Kod błędu.
    - `[ServiceErrorDetailMessage <String>]`: Komunikat o błędzie.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu naprawienia błędu.
    - `[TaskId <String>]`: Identyfikator zadania.
  - `[FriendlyName <String>]`: Właściwość DisplayName.
  - `[ScenarioName <String>]`: Scenariusz.
  - `[StartTime <DateTime?>]`: Godzina rozpoczęcia.
  - `[State <String>]`: Stan zadania. Jest to jedna z następujących wartości: NotStarted, InProgress, zakończony powodzeniem, niepomyślne, anulowane, zawieszone lub inne.
  - `[StateDescription <String>]`: Opis stanu zadania. Jeśli na przykład stan jest zakończony pomyślnie, opis może być ukończony, PartiallySucceeded, CompletedWithInformation lub pominięty.
  - `[TargetInstanceType <String>]`: Typ obiektu, którego dotyczy problem, który należy do klasy {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}.
  - `[TargetObjectId <String>]`: Odpowiedni identyfikator obiektu.
  - `[TargetObjectName <String>]`: Nazwa odpowiedniego obiektu.
  - `[Task <IAsrTask[]>]`: Zadania.
    - `[AllowedAction <String[]>]`: Stan/akcje mające zastosowanie do tego zadania.
    - `[CustomDetailInstanceType <String>]`: Typ szczegółów zadania.
    - `[EndTime <DateTime?>]`: Godzina zakończenia.
    - `[Error <IJobErrorDetails[]>]`: Szczegóły błędu zadania.
    - `[FriendlyName <String>]`: Imię i nazwisko.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Zadania podrzędne.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Typ szczegółów zadania.
    - `[Name <String>]`: Unikatowa nazwa zadania.
    - `[StartTime <DateTime?>]`: Godzina rozpoczęcia.
    - `[State <String>]`: Stan. Jest to jedna z następujących wartości: NotStarted, InProgress, zakończony powodzeniem, niepomyślne, anulowane, zawieszone lub inne.
    - `[StateDescription <String>]`: Opis stanu zadania. Na przykład w przypadku pomyślnego stanu opis może być ukończony, PartiallySucceeded, CompletedWithInformation lub pominięty.
    - `[TaskId <String>]`: Identyfikator.
    - `[TaskType <String>]`: Typ zadania. Szczegóły dotyczące właściwości CustomDetails są zależne od tego typu.

## LINKI POKREWNE

