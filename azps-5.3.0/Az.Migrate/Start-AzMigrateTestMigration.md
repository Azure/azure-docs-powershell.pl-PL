---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490109"
---
# <span data-ttu-id="9f6f9-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="9f6f9-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="9f6f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6f9-103">Rozpoczyna migrację testową dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="9f6f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f6f9-104">SYNTAX</span></span>

### <span data-ttu-id="9f6f9-105">ByIDVMwareCbt (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9f6f9-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9f6f9-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="9f6f9-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9f6f9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9f6f9-107">DESCRIPTION</span></span>
<span data-ttu-id="9f6f9-108">Polecenie cmdlet Start-AzMigrateTestMigration inicjuje migrację testową dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="9f6f9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f6f9-109">EXAMPLES</span></span>

### <span data-ttu-id="9f6f9-110">Przykład 1: Identyfikator komputera.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="9f6f9-111">Przez identyfikator komputera.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-111">By machine id.</span></span>

### <span data-ttu-id="9f6f9-112">Przykład 2. według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="9f6f9-112">Example 2: By input object</span></span>
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

<span data-ttu-id="9f6f9-113">Przez obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-113">By input object.</span></span>

## <span data-ttu-id="9f6f9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f6f9-114">PARAMETERS</span></span>

### <span data-ttu-id="9f6f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6f9-115">-DefaultProfile</span></span>
<span data-ttu-id="9f6f9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6f9-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f6f9-117">-InputObject</span></span>
<span data-ttu-id="9f6f9-118">Określa serwer replikacji, dla którego należy zainicjować migrację testową.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="9f6f9-119">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="9f6f9-120">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f6f9-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9f6f9-121">-SubscriptionId</span></span>
<span data-ttu-id="9f6f9-122">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9f6f9-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="9f6f9-123">-TargetObjectID</span></span>
<span data-ttu-id="9f6f9-124">Określa serwer replikacji, dla którego należy zainicjować migrację testową.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="9f6f9-125">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="9f6f9-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="9f6f9-126">-TestNetworkID</span></span>
<span data-ttu-id="9f6f9-127">Aktualizuje identyfikator sieci wirtualnej w ramach docelowej subskrypcji platformy Azure w celu użycia go na potrzeby migracji testów.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="9f6f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6f9-128">CommonParameters</span></span>
<span data-ttu-id="9f6f9-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6f9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f6f9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6f9-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f6f9-131">INPUTS</span></span>

## <span data-ttu-id="9f6f9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f6f9-132">OUTPUTS</span></span>

### <span data-ttu-id="9f6f9-133">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="9f6f9-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="9f6f9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f6f9-134">NOTES</span></span>

<span data-ttu-id="9f6f9-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9f6f9-135">ALIASES</span></span>

<span data-ttu-id="9f6f9-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f6f9-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f6f9-137">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f6f9-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f6f9-139">INPUTobject <IMigrationItem> : Określa serwer replikacji, dla którego należy zainicjować migrację testową.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="9f6f9-140">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="9f6f9-141">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="9f6f9-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="9f6f9-142">`[CurrentJobId <String>]`: Identyfikator ARM wykonywanego zadania.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="9f6f9-143">`[CurrentJobName <String>]`: Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="9f6f9-144">`[CurrentJobStartTime <DateTime?>]`: Godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="9f6f9-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="9f6f9-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="9f6f9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f6f9-146">RELATED LINKS</span></span>

