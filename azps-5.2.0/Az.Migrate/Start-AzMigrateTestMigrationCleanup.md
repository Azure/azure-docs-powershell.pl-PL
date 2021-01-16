---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363559"
---
# <span data-ttu-id="779ec-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="779ec-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="779ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="779ec-102">SYNOPSIS</span></span>
<span data-ttu-id="779ec-103">Czyści migrację testową dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="779ec-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="779ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="779ec-104">SYNTAX</span></span>

### <span data-ttu-id="779ec-105">ByIDVMwareCbt (domyślny)</span><span class="sxs-lookup"><span data-stu-id="779ec-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="779ec-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="779ec-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="779ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="779ec-107">DESCRIPTION</span></span>
<span data-ttu-id="779ec-108">Polecenie cmdlet Start-AzMigrateTestMigrationCleanup Inicjuje oczyszczanie migracji testowej dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="779ec-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="779ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="779ec-109">EXAMPLES</span></span>

### <span data-ttu-id="779ec-110">Przykład 1: Identyfikator komputera.</span><span class="sxs-lookup"><span data-stu-id="779ec-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="779ec-111">Przez identyfikator komputera.</span><span class="sxs-lookup"><span data-stu-id="779ec-111">By machine id.</span></span>

### <span data-ttu-id="779ec-112">Przykład 2. według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="779ec-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="779ec-113">Przez obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="779ec-113">By input object.</span></span>

## <span data-ttu-id="779ec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="779ec-114">PARAMETERS</span></span>

### <span data-ttu-id="779ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779ec-115">-DefaultProfile</span></span>
<span data-ttu-id="779ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="779ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="779ec-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="779ec-117">-InputObject</span></span>
<span data-ttu-id="779ec-118">Określa serwer replikacji, dla którego należy zainicjować oczyszczanie migracji testowej.</span><span class="sxs-lookup"><span data-stu-id="779ec-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="779ec-119">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication do skonstruowania, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="779ec-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="779ec-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="779ec-120">-SubscriptionId</span></span>
<span data-ttu-id="779ec-121">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="779ec-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="779ec-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="779ec-122">-TargetObjectID</span></span>
<span data-ttu-id="779ec-123">Określa serwer replikacji, dla którego należy zainicjować oczyszczanie migracji testowej.</span><span class="sxs-lookup"><span data-stu-id="779ec-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="779ec-124">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="779ec-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="779ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779ec-125">CommonParameters</span></span>
<span data-ttu-id="779ec-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779ec-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="779ec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779ec-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="779ec-128">INPUTS</span></span>

## <span data-ttu-id="779ec-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="779ec-129">OUTPUTS</span></span>

### <span data-ttu-id="779ec-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="779ec-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="779ec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="779ec-131">NOTES</span></span>

<span data-ttu-id="779ec-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="779ec-132">ALIASES</span></span>

<span data-ttu-id="779ec-133">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="779ec-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="779ec-134">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="779ec-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="779ec-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="779ec-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="779ec-136">INPUTobject <IMigrationItem> : Określa serwer replikacji, dla którego należy zainicjować oczyszczanie migracji testów.</span><span class="sxs-lookup"><span data-stu-id="779ec-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="779ec-137">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="779ec-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="779ec-138">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="779ec-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="779ec-139">`[CurrentJobId <String>]`: Identyfikator ARM wykonywanego zadania.</span><span class="sxs-lookup"><span data-stu-id="779ec-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="779ec-140">`[CurrentJobName <String>]`: Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="779ec-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="779ec-141">`[CurrentJobStartTime <DateTime?>]`: Godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="779ec-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="779ec-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="779ec-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="779ec-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="779ec-143">RELATED LINKS</span></span>

