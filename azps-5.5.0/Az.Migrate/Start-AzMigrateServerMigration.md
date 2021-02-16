---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185051"
---
# <span data-ttu-id="a7532-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="a7532-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="a7532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7532-102">SYNOPSIS</span></span>
<span data-ttu-id="a7532-103">Rozpoczyna migrację serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="a7532-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="a7532-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7532-104">SYNTAX</span></span>

### <span data-ttu-id="a7532-105">ByIDVBlockCbt (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a7532-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7532-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="a7532-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a7532-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7532-107">DESCRIPTION</span></span>
<span data-ttu-id="a7532-108">Rozpoczyna migrację serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="a7532-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="a7532-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7532-109">EXAMPLES</span></span>

### <span data-ttu-id="a7532-110">Przykład 1. Według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="a7532-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="a7532-111">Według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="a7532-111">By id</span></span>

## <span data-ttu-id="a7532-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7532-112">PARAMETERS</span></span>

### <span data-ttu-id="a7532-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7532-113">-DefaultProfile</span></span>
<span data-ttu-id="a7532-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7532-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7532-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7532-115">-InputObject</span></span>
<span data-ttu-id="a7532-116">Określa serwer replikowania, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="a7532-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="a7532-117">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7532-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="a7532-118">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a7532-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7532-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7532-119">-SubscriptionId</span></span>
<span data-ttu-id="a7532-120">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7532-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a7532-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="a7532-121">-TargetObjectID</span></span>
<span data-ttu-id="a7532-122">Określa serwer, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="a7532-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="a7532-123">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7532-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a7532-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="a7532-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="a7532-125">Określa, czy po migracji serwer źródłowy powinien zostać wyłączony.</span><span class="sxs-lookup"><span data-stu-id="a7532-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7532-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7532-126">CommonParameters</span></span>
<span data-ttu-id="a7532-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7532-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7532-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7532-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7532-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7532-129">INPUTS</span></span>

## <span data-ttu-id="a7532-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7532-130">OUTPUTS</span></span>

### <span data-ttu-id="a7532-131">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="a7532-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a7532-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7532-132">NOTES</span></span>

<span data-ttu-id="a7532-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a7532-133">ALIASES</span></span>

<span data-ttu-id="a7532-134">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a7532-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7532-135">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a7532-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7532-136">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7532-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7532-137">INPUTOBJECT: <IMigrationItem> Określa serwer replikowania, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="a7532-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="a7532-138">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7532-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="a7532-139">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a7532-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a7532-140">`[CurrentJobId <String>]`: ARM identyfikatora zadania do wykonania.</span><span class="sxs-lookup"><span data-stu-id="a7532-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="a7532-141">`[CurrentJobName <String>]`: nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="a7532-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="a7532-142">`[CurrentJobStartTime <DateTime?>]`: godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="a7532-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="a7532-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="a7532-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="a7532-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7532-144">RELATED LINKS</span></span>

