---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185035"
---
# <span data-ttu-id="f1184-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="f1184-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="f1184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1184-102">SYNOPSIS</span></span>
<span data-ttu-id="f1184-103">Rozpoczyna migrację testów dla serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="f1184-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="f1184-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1184-104">SYNTAX</span></span>

### <span data-ttu-id="f1184-105">ByIDVBlockCbt (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f1184-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1184-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="f1184-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f1184-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1184-107">DESCRIPTION</span></span>
<span data-ttu-id="f1184-108">Polecenie Start-AzMigrateTestMigration inicjuje migrację testową dla serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="f1184-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="f1184-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1184-109">EXAMPLES</span></span>

### <span data-ttu-id="f1184-110">Przykład 1. Według identyfikatora komputera.</span><span class="sxs-lookup"><span data-stu-id="f1184-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="f1184-111">Według identyfikatora komputera.</span><span class="sxs-lookup"><span data-stu-id="f1184-111">By machine id.</span></span>

### <span data-ttu-id="f1184-112">Przykład 2. Według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="f1184-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="f1184-113">Według obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="f1184-113">By input object.</span></span>

## <span data-ttu-id="f1184-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1184-114">PARAMETERS</span></span>

### <span data-ttu-id="f1184-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1184-115">-DefaultProfile</span></span>
<span data-ttu-id="f1184-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1184-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1184-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1184-117">-InputObject</span></span>
<span data-ttu-id="f1184-118">Określa serwer replikowania, dla którego ma zostać zainicjowana migracja testowa.</span><span class="sxs-lookup"><span data-stu-id="f1184-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="f1184-119">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1184-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="f1184-120">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f1184-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1184-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1184-121">-SubscriptionId</span></span>
<span data-ttu-id="f1184-122">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f1184-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f1184-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="f1184-123">-TargetObjectID</span></span>
<span data-ttu-id="f1184-124">Określa serwer replikowania, dla którego ma zostać zainicjowana migracja testowa.</span><span class="sxs-lookup"><span data-stu-id="f1184-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="f1184-125">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1184-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="f1184-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="f1184-126">-TestNetworkID</span></span>
<span data-ttu-id="f1184-127">Aktualizuje identyfikator wirtualnej sieci w docelowej subskrypcji platformy Azure, aby był używany do migracji testowej.</span><span class="sxs-lookup"><span data-stu-id="f1184-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1184-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1184-128">CommonParameters</span></span>
<span data-ttu-id="f1184-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1184-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1184-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1184-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1184-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1184-131">INPUTS</span></span>

## <span data-ttu-id="f1184-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1184-132">OUTPUTS</span></span>

### <span data-ttu-id="f1184-133">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="f1184-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="f1184-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1184-134">NOTES</span></span>

<span data-ttu-id="f1184-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f1184-135">ALIASES</span></span>

<span data-ttu-id="f1184-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1184-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1184-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f1184-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1184-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1184-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1184-139">INPUTOBJECT: Określa serwer replikowania, dla którego ma zostać zainicjowana <IMigrationItem> migracja testowa.</span><span class="sxs-lookup"><span data-stu-id="f1184-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="f1184-140">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1184-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="f1184-141">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="f1184-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="f1184-142">`[CurrentJobId <String>]`: ARM identyfikatora zadania do wykonania.</span><span class="sxs-lookup"><span data-stu-id="f1184-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="f1184-143">`[CurrentJobName <String>]`: nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="f1184-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="f1184-144">`[CurrentJobStartTime <DateTime?>]`: godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="f1184-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="f1184-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="f1184-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="f1184-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1184-146">RELATED LINKS</span></span>

