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
# <span data-ttu-id="8585e-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="8585e-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="8585e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8585e-102">SYNOPSIS</span></span>
<span data-ttu-id="8585e-103">Pobiera stan zadania migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8585e-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="8585e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8585e-104">SYNTAX</span></span>

### <span data-ttu-id="8585e-105">ListByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8585e-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8585e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="8585e-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8585e-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8585e-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8585e-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="8585e-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8585e-109">ListById</span><span class="sxs-lookup"><span data-stu-id="8585e-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8585e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="8585e-110">DESCRIPTION</span></span>
<span data-ttu-id="8585e-111">Polecenie cmdlet Get-AzMigrateJob retrives stan zadania migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8585e-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="8585e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8585e-112">EXAMPLES</span></span>

### <span data-ttu-id="8585e-113">Przykład 1. Poproś o identyfikator zadania</span><span class="sxs-lookup"><span data-stu-id="8585e-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="8585e-114">Spowoduje to pobranie zadania o jego identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="8585e-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="8585e-115">Przykład 2: Wyświetlanie listy według grupy zasobów i projektu</span><span class="sxs-lookup"><span data-stu-id="8585e-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="8585e-116">Spowoduje to odpobieranie wszystkich zadań w projekcie.</span><span class="sxs-lookup"><span data-stu-id="8585e-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="8585e-117">Przykład 3: Pobierz według grupy zasobów, projektu i nazwy zadania</span><span class="sxs-lookup"><span data-stu-id="8585e-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="8585e-118">Spowoduje to wyświetlenie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-118">This gets a specific job.</span></span>

## <span data-ttu-id="8585e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8585e-119">PARAMETERS</span></span>

### <span data-ttu-id="8585e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8585e-120">-DefaultProfile</span></span>
<span data-ttu-id="8585e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8585e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8585e-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="8585e-122">-Filter</span></span>
<span data-ttu-id="8585e-123">Opcje filtru OData.</span><span class="sxs-lookup"><span data-stu-id="8585e-123">OData filter options.</span></span>

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

### <span data-ttu-id="8585e-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8585e-124">-InputObject</span></span>
<span data-ttu-id="8585e-125">Określa obiekt zadania serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="8585e-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="8585e-126">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8585e-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8585e-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="8585e-127">-JobID</span></span>
<span data-ttu-id="8585e-128">Określa identyfikator zadania, dla którego należy pobrać dane.</span><span class="sxs-lookup"><span data-stu-id="8585e-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="8585e-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="8585e-129">-JobName</span></span>
<span data-ttu-id="8585e-130">Identyfikator zadania</span><span class="sxs-lookup"><span data-stu-id="8585e-130">Job identifier</span></span>

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

### <span data-ttu-id="8585e-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="8585e-131">-ProjectID</span></span>
<span data-ttu-id="8585e-132">Określa projekt migracji platformy Azure, w którym są replikowane serwery.</span><span class="sxs-lookup"><span data-stu-id="8585e-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="8585e-133">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="8585e-133">-ProjectName</span></span>
<span data-ttu-id="8585e-134">Nazwa projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="8585e-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="8585e-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="8585e-135">-ResourceGroupID</span></span>
<span data-ttu-id="8585e-136">Określa grupę zasobów projektu migracji platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8585e-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="8585e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8585e-137">-ResourceGroupName</span></span>
<span data-ttu-id="8585e-138">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8585e-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="8585e-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8585e-139">-SubscriptionId</span></span>
<span data-ttu-id="8585e-140">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8585e-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8585e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8585e-141">CommonParameters</span></span>
<span data-ttu-id="8585e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8585e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8585e-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8585e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8585e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8585e-144">INPUTS</span></span>

## <span data-ttu-id="8585e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8585e-145">OUTPUTS</span></span>

### <span data-ttu-id="8585e-146">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="8585e-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8585e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8585e-147">NOTES</span></span>

<span data-ttu-id="8585e-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8585e-148">ALIASES</span></span>

<span data-ttu-id="8585e-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8585e-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8585e-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8585e-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8585e-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8585e-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8585e-152">INPUTobject <IJob> : określa obiekt zadania serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="8585e-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="8585e-153">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="8585e-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="8585e-154">`[ActivityId <String>]`: Identyfikator aktywności.</span><span class="sxs-lookup"><span data-stu-id="8585e-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="8585e-155">`[AllowedAction <String[]>]`: Dozwolone działanie zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="8585e-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Uwzględnione właściwości obiektu, takie jak serwer źródłowy, Chmura źródłowa, serwer docelowy, Chmura docelowa itd., na podstawie szczegółów obiektu przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="8585e-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="8585e-157">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="8585e-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8585e-158">`[EndTime <DateTime?>]`: Godzina zakończenia.</span><span class="sxs-lookup"><span data-stu-id="8585e-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="8585e-159">`[Error <IJobErrorDetails[]>]`: Błędy.</span><span class="sxs-lookup"><span data-stu-id="8585e-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="8585e-160">`[CreationTime <DateTime?>]`: Czas utworzenia błędu zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="8585e-161">`[ErrorLevel <String>]`: Błąd poziomu błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="8585e-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Kod błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="8585e-163">`[ProviderErrorDetailErrorId <String>]`: Identyfikator błędu dostawcy.</span><span class="sxs-lookup"><span data-stu-id="8585e-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="8585e-164">`[ProviderErrorDetailErrorMessage <String>]`: Komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="8585e-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="8585e-165">`[ProviderErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="8585e-166">`[ProviderErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu usunięcia błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="8585e-167">`[ServiceErrorDetailActivityId <String>]`: Identyfikator aktywności.</span><span class="sxs-lookup"><span data-stu-id="8585e-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="8585e-168">`[ServiceErrorDetailCode <String>]`: Kod błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="8585e-169">`[ServiceErrorDetailMessage <String>]`: Komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="8585e-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="8585e-170">`[ServiceErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="8585e-171">`[ServiceErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu naprawienia błędu.</span><span class="sxs-lookup"><span data-stu-id="8585e-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="8585e-172">`[TaskId <String>]`: Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="8585e-173">`[FriendlyName <String>]`: Właściwość DisplayName.</span><span class="sxs-lookup"><span data-stu-id="8585e-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="8585e-174">`[ScenarioName <String>]`: Scenariusz.</span><span class="sxs-lookup"><span data-stu-id="8585e-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="8585e-175">`[StartTime <DateTime?>]`: Godzina rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="8585e-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="8585e-176">`[State <String>]`: Stan zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="8585e-177">Jest to jedna z następujących wartości: NotStarted, InProgress, zakończony powodzeniem, niepomyślne, anulowane, zawieszone lub inne.</span><span class="sxs-lookup"><span data-stu-id="8585e-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="8585e-178">`[StateDescription <String>]`: Opis stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="8585e-179">Jeśli na przykład stan jest zakończony pomyślnie, opis może być ukończony, PartiallySucceeded, CompletedWithInformation lub pominięty.</span><span class="sxs-lookup"><span data-stu-id="8585e-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="8585e-180">`[TargetInstanceType <String>]`: Typ obiektu, którego dotyczy problem, który należy do klasy {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="8585e-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="8585e-181">`[TargetObjectId <String>]`: Odpowiedni identyfikator obiektu.</span><span class="sxs-lookup"><span data-stu-id="8585e-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="8585e-182">`[TargetObjectName <String>]`: Nazwa odpowiedniego obiektu.</span><span class="sxs-lookup"><span data-stu-id="8585e-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="8585e-183">`[Task <IAsrTask[]>]`: Zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="8585e-184">`[AllowedAction <String[]>]`: Stan/akcje mające zastosowanie do tego zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="8585e-185">`[CustomDetailInstanceType <String>]`: Typ szczegółów zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="8585e-186">`[EndTime <DateTime?>]`: Godzina zakończenia.</span><span class="sxs-lookup"><span data-stu-id="8585e-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="8585e-187">`[Error <IJobErrorDetails[]>]`: Szczegóły błędu zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="8585e-188">`[FriendlyName <String>]`: Imię i nazwisko.</span><span class="sxs-lookup"><span data-stu-id="8585e-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="8585e-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Zadania podrzędne.</span><span class="sxs-lookup"><span data-stu-id="8585e-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="8585e-190">`[GroupTaskCustomDetailInstanceType <String>]`: Typ szczegółów zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="8585e-191">`[Name <String>]`: Unikatowa nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="8585e-192">`[StartTime <DateTime?>]`: Godzina rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="8585e-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="8585e-193">`[State <String>]`: Stan.</span><span class="sxs-lookup"><span data-stu-id="8585e-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="8585e-194">Jest to jedna z następujących wartości: NotStarted, InProgress, zakończony powodzeniem, niepomyślne, anulowane, zawieszone lub inne.</span><span class="sxs-lookup"><span data-stu-id="8585e-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="8585e-195">`[StateDescription <String>]`: Opis stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="8585e-196">Na przykład w przypadku pomyślnego stanu opis może być ukończony, PartiallySucceeded, CompletedWithInformation lub pominięty.</span><span class="sxs-lookup"><span data-stu-id="8585e-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="8585e-197">`[TaskId <String>]`: Identyfikator.</span><span class="sxs-lookup"><span data-stu-id="8585e-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="8585e-198">`[TaskType <String>]`: Typ zadania.</span><span class="sxs-lookup"><span data-stu-id="8585e-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="8585e-199">Szczegóły dotyczące właściwości CustomDetails są zależne od tego typu.</span><span class="sxs-lookup"><span data-stu-id="8585e-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="8585e-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8585e-200">RELATED LINKS</span></span>

