---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982954"
---
# <span data-ttu-id="48982-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="48982-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="48982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48982-102">SYNOPSIS</span></span>
<span data-ttu-id="48982-103">Pobiera stan zadania migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48982-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="48982-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48982-104">SYNTAX</span></span>

### <span data-ttu-id="48982-105">ListByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="48982-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48982-106">GetById</span><span class="sxs-lookup"><span data-stu-id="48982-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48982-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="48982-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="48982-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="48982-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48982-109">ListById</span><span class="sxs-lookup"><span data-stu-id="48982-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="48982-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="48982-110">DESCRIPTION</span></span>
<span data-ttu-id="48982-111">Polecenie Get-AzMigrateJob cmdlet ponownie pointrybuje stan zadania migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48982-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="48982-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48982-112">EXAMPLES</span></span>

### <span data-ttu-id="48982-113">Przykład 1. Uzyskiwanie według identyfikatora stanowiska</span><span class="sxs-lookup"><span data-stu-id="48982-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="48982-114">To pobiera zadanie według jego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="48982-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="48982-115">Przykład 2. Lista według grupy zasobów i projektu</span><span class="sxs-lookup"><span data-stu-id="48982-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="48982-116">Otrzymuje to wszystkie zadania w projekcie.</span><span class="sxs-lookup"><span data-stu-id="48982-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="48982-117">Przykład 3. Uzyskiwanie według grupy zasobów, projektu i nazwy zadania</span><span class="sxs-lookup"><span data-stu-id="48982-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="48982-118">Otrzymujesz określoną pracę.</span><span class="sxs-lookup"><span data-stu-id="48982-118">This gets a specific job.</span></span>

## <span data-ttu-id="48982-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48982-119">PARAMETERS</span></span>

### <span data-ttu-id="48982-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48982-120">-DefaultProfile</span></span>
<span data-ttu-id="48982-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48982-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48982-122">— Filtr</span><span class="sxs-lookup"><span data-stu-id="48982-122">-Filter</span></span>
<span data-ttu-id="48982-123">Opcje filtru OData.</span><span class="sxs-lookup"><span data-stu-id="48982-123">OData filter options.</span></span>

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

### <span data-ttu-id="48982-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48982-124">-InputObject</span></span>
<span data-ttu-id="48982-125">Określa obiekt zadania serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="48982-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="48982-126">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="48982-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48982-127">— JobID</span><span class="sxs-lookup"><span data-stu-id="48982-127">-JobID</span></span>
<span data-ttu-id="48982-128">Określa identyfikator zadania, dla którego należy pobrać szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="48982-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="48982-129">— JobName</span><span class="sxs-lookup"><span data-stu-id="48982-129">-JobName</span></span>
<span data-ttu-id="48982-130">Identyfikator zadania</span><span class="sxs-lookup"><span data-stu-id="48982-130">Job identifier</span></span>

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

### <span data-ttu-id="48982-131">— ProjectID</span><span class="sxs-lookup"><span data-stu-id="48982-131">-ProjectID</span></span>
<span data-ttu-id="48982-132">Określa projekt migracji platformy Azure, w którym serwery są replikowane.</span><span class="sxs-lookup"><span data-stu-id="48982-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="48982-133">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="48982-133">-ProjectName</span></span>
<span data-ttu-id="48982-134">Nazwa migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="48982-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="48982-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="48982-135">-ResourceGroupID</span></span>
<span data-ttu-id="48982-136">Określa grupę zasobów projektu migracji platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="48982-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="48982-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48982-137">-ResourceGroupName</span></span>
<span data-ttu-id="48982-138">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="48982-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="48982-139">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48982-139">-SubscriptionId</span></span>
<span data-ttu-id="48982-140">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48982-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="48982-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48982-141">CommonParameters</span></span>
<span data-ttu-id="48982-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48982-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48982-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48982-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48982-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48982-144">INPUTS</span></span>

## <span data-ttu-id="48982-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48982-145">OUTPUTS</span></span>

### <span data-ttu-id="48982-146">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="48982-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="48982-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48982-147">NOTES</span></span>

<span data-ttu-id="48982-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="48982-148">ALIASES</span></span>

<span data-ttu-id="48982-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48982-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48982-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="48982-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48982-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48982-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48982-152">INPUTOBJECT: <IJob> Określa obiekt zadania serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="48982-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="48982-153">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="48982-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="48982-154">`[ActivityId <String>]`: Identyfikator działania.</span><span class="sxs-lookup"><span data-stu-id="48982-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="48982-155">`[AllowedAction <String[]>]`: Dozwolona akcja zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="48982-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Właściwości obiektu, których dotyczy problem, takie jak serwer źródłowy, chmura źródłowa, serwer docelowy, chmura docelowa itp. na podstawie szczegółów obiektu przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="48982-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="48982-157">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="48982-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="48982-158">`[EndTime <DateTime?>]`: godzina zakończenia.</span><span class="sxs-lookup"><span data-stu-id="48982-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="48982-159">`[Error <IJobErrorDetails[]>]`: Błędy.</span><span class="sxs-lookup"><span data-stu-id="48982-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="48982-160">`[CreationTime <DateTime?>]`: Czas tworzenia błędu zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="48982-161">`[ErrorLevel <String>]`: Poziom błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="48982-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Kod błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="48982-163">`[ProviderErrorDetailErrorId <String>]`: Identyfikator błędu dostawcy.</span><span class="sxs-lookup"><span data-stu-id="48982-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="48982-164">`[ProviderErrorDetailErrorMessage <String>]`: Komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="48982-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="48982-165">`[ProviderErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="48982-166">`[ProviderErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu usunięcia błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="48982-167">`[ServiceErrorDetailActivityId <String>]`: Identyfikator działania.</span><span class="sxs-lookup"><span data-stu-id="48982-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="48982-168">`[ServiceErrorDetailCode <String>]`: Kod błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="48982-169">`[ServiceErrorDetailMessage <String>]`: Komunikat o błędzie.</span><span class="sxs-lookup"><span data-stu-id="48982-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="48982-170">`[ServiceErrorDetailPossibleCaus <String>]`: Możliwe przyczyny błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="48982-171">`[ServiceErrorDetailRecommendedAction <String>]`: Zalecana akcja w celu usunięcia błędu.</span><span class="sxs-lookup"><span data-stu-id="48982-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="48982-172">`[TaskId <String>]`: Identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="48982-173">`[FriendlyName <String>]`: Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="48982-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="48982-174">`[ScenarioName <String>]`: Nazwa_scenariusza.</span><span class="sxs-lookup"><span data-stu-id="48982-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="48982-175">`[StartTime <DateTime?>]`: godzina rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="48982-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="48982-176">`[State <String>]`: stan zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="48982-177">Jest to jedna z tych wartości: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended lub Other.</span><span class="sxs-lookup"><span data-stu-id="48982-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="48982-178">`[StateDescription <String>]`: opis stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="48982-179">Na przykład — w przypadku stanu zakończonego pomyślnie można dodać opis: Ukończono, Częściowoskucceed, CompletedWithInformation lub Pominięto.</span><span class="sxs-lookup"><span data-stu-id="48982-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="48982-180">`[TargetInstanceType <String>]`: typ obiektu, którego dotyczy problem, który jest klasą {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="48982-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="48982-181">`[TargetObjectId <String>]`: Identyfikator obiektu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="48982-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="48982-182">`[TargetObjectName <String>]`: nazwa obiektu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="48982-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="48982-183">`[Task <IAsrTask[]>]`: Zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="48982-184">`[AllowedAction <String[]>]`: Stan/akcje mające zastosowanie do tego zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="48982-185">`[CustomDetailInstanceType <String>]`: typ szczegółów zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="48982-186">`[EndTime <DateTime?>]`: godzina zakończenia.</span><span class="sxs-lookup"><span data-stu-id="48982-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="48982-187">`[Error <IJobErrorDetails[]>]`: Szczegóły błędu zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="48982-188">`[FriendlyName <String>]`: Nazwa.</span><span class="sxs-lookup"><span data-stu-id="48982-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="48982-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Zadania podrzędne.</span><span class="sxs-lookup"><span data-stu-id="48982-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="48982-190">`[GroupTaskCustomDetailInstanceType <String>]`: typ szczegółów zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="48982-191">`[Name <String>]`: unikatowa nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="48982-192">`[StartTime <DateTime?>]`: godzina rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="48982-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="48982-193">`[State <String>]`: Województwo.</span><span class="sxs-lookup"><span data-stu-id="48982-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="48982-194">Jest to jedna z tych wartości: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended lub Other.</span><span class="sxs-lookup"><span data-stu-id="48982-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="48982-195">`[StateDescription <String>]`: opis stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="48982-196">Na przykład — w przypadku stanu zakończonego pomyślnie opis może zostać zakończony, częściowoskucceed, CompletedWithInformation lub pominięty.</span><span class="sxs-lookup"><span data-stu-id="48982-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="48982-197">`[TaskId <String>]`: Identyfikator.</span><span class="sxs-lookup"><span data-stu-id="48982-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="48982-198">`[TaskType <String>]`: typ zadania.</span><span class="sxs-lookup"><span data-stu-id="48982-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="48982-199">Szczegóły właściwości CustomDetails zależą od tego typu.</span><span class="sxs-lookup"><span data-stu-id="48982-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="48982-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48982-200">RELATED LINKS</span></span>

