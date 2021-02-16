---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185050"
---
# <span data-ttu-id="424fb-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="424fb-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="424fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424fb-102">SYNOPSIS</span></span>
<span data-ttu-id="424fb-103">Powoduje ponowne uruchomienie replikacji dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="424fb-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="424fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="424fb-104">SYNTAX</span></span>

### <span data-ttu-id="424fb-105">ByIDVBlockCbt (domyślne)</span><span class="sxs-lookup"><span data-stu-id="424fb-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="424fb-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="424fb-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="424fb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="424fb-107">DESCRIPTION</span></span>
<span data-ttu-id="424fb-108">Polecenie Restart-AzMigrateServerReplication naprawia replikację dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="424fb-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="424fb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="424fb-109">EXAMPLES</span></span>

### <span data-ttu-id="424fb-110">Przykład 1. Według identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="424fb-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="424fb-111">Według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="424fb-111">By id.</span></span>

### <span data-ttu-id="424fb-112">Przykład 2. Według obiektu Input</span><span class="sxs-lookup"><span data-stu-id="424fb-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="424fb-113">Według obiektu Input.</span><span class="sxs-lookup"><span data-stu-id="424fb-113">By Input Object.</span></span>

## <span data-ttu-id="424fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="424fb-114">PARAMETERS</span></span>

### <span data-ttu-id="424fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424fb-115">-DefaultProfile</span></span>
<span data-ttu-id="424fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="424fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424fb-117">-InputObject</span></span>
<span data-ttu-id="424fb-118">Określa obiekt komputera serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="424fb-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="424fb-119">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="424fb-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="424fb-120">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="424fb-120">-SubscriptionId</span></span>
<span data-ttu-id="424fb-121">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="424fb-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="424fb-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="424fb-122">-TargetObjectID</span></span>
<span data-ttu-id="424fb-123">Określa serwer, dla którego ma zostać zainicjowana ponowna synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="424fb-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="424fb-124">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424fb-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="424fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424fb-125">CommonParameters</span></span>
<span data-ttu-id="424fb-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424fb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="424fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424fb-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424fb-128">INPUTS</span></span>

## <span data-ttu-id="424fb-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424fb-129">OUTPUTS</span></span>

### <span data-ttu-id="424fb-130">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="424fb-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="424fb-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="424fb-131">NOTES</span></span>

<span data-ttu-id="424fb-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="424fb-132">ALIASES</span></span>

<span data-ttu-id="424fb-133">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="424fb-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="424fb-134">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="424fb-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="424fb-135">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="424fb-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="424fb-136">INPUTOBJECT: <IMigrationItem> Określa obiekt komputera serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="424fb-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="424fb-137">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="424fb-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="424fb-138">`[CurrentJobId <String>]`: ARM identyfikatora zadania do wykonania.</span><span class="sxs-lookup"><span data-stu-id="424fb-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="424fb-139">`[CurrentJobName <String>]`: nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="424fb-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="424fb-140">`[CurrentJobStartTime <DateTime?>]`: godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="424fb-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="424fb-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="424fb-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="424fb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="424fb-142">RELATED LINKS</span></span>

