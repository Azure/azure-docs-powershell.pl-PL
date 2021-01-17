---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490117"
---
# <span data-ttu-id="a66b7-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="a66b7-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="a66b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a66b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a66b7-103">Zatrzymuje replikację zmigrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="a66b7-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="a66b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a66b7-104">SYNTAX</span></span>

### <span data-ttu-id="a66b7-105">ByIDVMwareCbt (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a66b7-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a66b7-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="a66b7-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a66b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a66b7-107">DESCRIPTION</span></span>
<span data-ttu-id="a66b7-108">Polecenie cmdlet Remove-AzMigrateServerReplication zatrzymuje replikację dla zmigrowanego serwera.</span><span class="sxs-lookup"><span data-stu-id="a66b7-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="a66b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a66b7-109">EXAMPLES</span></span>

### <span data-ttu-id="a66b7-110">Przykład 1: Usuwanie według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a66b7-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="a66b7-111">Ponowna synchronizacja według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="a66b7-111">Resync by id.</span></span>

### <span data-ttu-id="a66b7-112">Przykład 2: usuwanie przez obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="a66b7-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="a66b7-113">Według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a66b7-113">By name.</span></span>

## <span data-ttu-id="a66b7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a66b7-114">PARAMETERS</span></span>

### <span data-ttu-id="a66b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66b7-115">-DefaultProfile</span></span>
<span data-ttu-id="a66b7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a66b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66b7-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="a66b7-117">-ForceRemove</span></span>
<span data-ttu-id="a66b7-118">Określa, czy należy wymusić usunięcie replikacji.</span><span class="sxs-lookup"><span data-stu-id="a66b7-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="a66b7-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a66b7-119">-InputObject</span></span>
<span data-ttu-id="a66b7-120">Określa obiekt Machine serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="a66b7-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="a66b7-121">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a66b7-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a66b7-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a66b7-122">-SubscriptionId</span></span>
<span data-ttu-id="a66b7-123">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a66b7-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a66b7-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="a66b7-124">-TargetObjectID</span></span>
<span data-ttu-id="a66b7-125">Określa serwer replcating, dla którego należy wyłączyć replicatio.</span><span class="sxs-lookup"><span data-stu-id="a66b7-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="a66b7-126">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="a66b7-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a66b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66b7-127">CommonParameters</span></span>
<span data-ttu-id="a66b7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66b7-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a66b7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66b7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a66b7-130">INPUTS</span></span>

## <span data-ttu-id="a66b7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a66b7-131">OUTPUTS</span></span>

### <span data-ttu-id="a66b7-132">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="a66b7-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a66b7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a66b7-133">NOTES</span></span>

<span data-ttu-id="a66b7-134">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a66b7-134">ALIASES</span></span>

<span data-ttu-id="a66b7-135">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a66b7-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a66b7-136">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a66b7-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a66b7-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a66b7-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a66b7-138">INPUTobject <IMigrationItem> : określa obiekt Machine serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="a66b7-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="a66b7-139">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a66b7-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a66b7-140">`[CurrentJobId <String>]`: Identyfikator ARM wykonywanego zadania.</span><span class="sxs-lookup"><span data-stu-id="a66b7-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="a66b7-141">`[CurrentJobName <String>]`: Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="a66b7-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="a66b7-142">`[CurrentJobStartTime <DateTime?>]`: Godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="a66b7-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="a66b7-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="a66b7-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="a66b7-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a66b7-144">RELATED LINKS</span></span>

