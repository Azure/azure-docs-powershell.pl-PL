---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: 65f9527005b849b9ffbcc8c343b57515b2d437c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006561"
---
# <span data-ttu-id="f4329-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="f4329-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="f4329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4329-102">SYNOPSIS</span></span>
<span data-ttu-id="f4329-103">Zatrzymuje replikację dla migrego serwera.</span><span class="sxs-lookup"><span data-stu-id="f4329-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="f4329-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4329-104">SYNTAX</span></span>

### <span data-ttu-id="f4329-105">ByIDVBlockCbt (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f4329-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4329-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="f4329-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4329-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4329-107">DESCRIPTION</span></span>
<span data-ttu-id="f4329-108">Polecenie Remove-AzMigrateServerReplication zatrzymuje replikację dla serwera poddanego migracji.</span><span class="sxs-lookup"><span data-stu-id="f4329-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="f4329-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4329-109">EXAMPLES</span></span>

### <span data-ttu-id="f4329-110">Przykład 1. Usuwanie według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="f4329-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="f4329-111">Ponowne synchronizacja według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="f4329-111">Resync by id.</span></span>

### <span data-ttu-id="f4329-112">Przykład 2. Usuwanie według obiektu Input</span><span class="sxs-lookup"><span data-stu-id="f4329-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="f4329-113">Według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f4329-113">By name.</span></span>

## <span data-ttu-id="f4329-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4329-114">PARAMETERS</span></span>

### <span data-ttu-id="f4329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4329-115">-DefaultProfile</span></span>
<span data-ttu-id="f4329-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4329-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4329-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="f4329-117">-ForceRemove</span></span>
<span data-ttu-id="f4329-118">Określa, czy replikacja musi zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="f4329-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="f4329-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4329-119">-InputObject</span></span>
<span data-ttu-id="f4329-120">Określa obiekt komputera serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="f4329-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="f4329-121">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="f4329-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4329-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4329-122">-SubscriptionId</span></span>
<span data-ttu-id="f4329-123">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4329-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f4329-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="f4329-124">-TargetObjectID</span></span>
<span data-ttu-id="f4329-125">Określa serwer replcatingu, dla którego replice muszą zostać wyłączone.</span><span class="sxs-lookup"><span data-stu-id="f4329-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="f4329-126">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4329-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="f4329-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4329-127">CommonParameters</span></span>
<span data-ttu-id="f4329-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4329-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4329-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4329-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4329-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4329-130">INPUTS</span></span>

## <span data-ttu-id="f4329-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4329-131">OUTPUTS</span></span>

### <span data-ttu-id="f4329-132">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="f4329-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="f4329-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4329-133">NOTES</span></span>

<span data-ttu-id="f4329-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f4329-134">ALIASES</span></span>

<span data-ttu-id="f4329-135">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4329-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4329-136">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f4329-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4329-137">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4329-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4329-138">INPUTOBJECT: <IMigrationItem> Określa obiekt komputera serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="f4329-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="f4329-139">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="f4329-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="f4329-140">`[CurrentJobId <String>]`: ARM identyfikatora zadania do wykonania.</span><span class="sxs-lookup"><span data-stu-id="f4329-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="f4329-141">`[CurrentJobName <String>]`: nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="f4329-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="f4329-142">`[CurrentJobStartTime <DateTime?>]`: godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="f4329-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="f4329-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="f4329-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="f4329-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4329-144">RELATED LINKS</span></span>

