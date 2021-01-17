---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490113"
---
# <span data-ttu-id="6c750-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="6c750-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="6c750-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c750-102">SYNOPSIS</span></span>
<span data-ttu-id="6c750-103">Rozpoczyna migrację dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="6c750-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="6c750-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c750-104">SYNTAX</span></span>

### <span data-ttu-id="6c750-105">ByIDVMwareCbt (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c750-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c750-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="6c750-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6c750-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c750-107">DESCRIPTION</span></span>
<span data-ttu-id="6c750-108">Rozpoczyna migrację dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="6c750-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="6c750-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c750-109">EXAMPLES</span></span>

### <span data-ttu-id="6c750-110">Przykład 1. według ID</span><span class="sxs-lookup"><span data-stu-id="6c750-110">Example 1: By id</span></span>
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

<span data-ttu-id="6c750-111">Według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="6c750-111">By id</span></span>

## <span data-ttu-id="6c750-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c750-112">PARAMETERS</span></span>

### <span data-ttu-id="6c750-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c750-113">-DefaultProfile</span></span>
<span data-ttu-id="6c750-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c750-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c750-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c750-115">-InputObject</span></span>
<span data-ttu-id="6c750-116">Określa serwer replikacji, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="6c750-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="6c750-117">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="6c750-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="6c750-118">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="6c750-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c750-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6c750-119">-SubscriptionId</span></span>
<span data-ttu-id="6c750-120">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c750-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6c750-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="6c750-121">-TargetObjectID</span></span>
<span data-ttu-id="6c750-122">Określa serwer replcating, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="6c750-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="6c750-123">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="6c750-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="6c750-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="6c750-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="6c750-125">Określa, czy serwer źródłowy powinien być wyłączony.</span><span class="sxs-lookup"><span data-stu-id="6c750-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="6c750-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c750-126">CommonParameters</span></span>
<span data-ttu-id="6c750-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c750-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c750-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c750-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c750-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c750-129">INPUTS</span></span>

## <span data-ttu-id="6c750-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c750-130">OUTPUTS</span></span>

### <span data-ttu-id="6c750-131">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="6c750-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6c750-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c750-132">NOTES</span></span>

<span data-ttu-id="6c750-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6c750-133">ALIASES</span></span>

<span data-ttu-id="6c750-134">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c750-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c750-135">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6c750-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c750-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c750-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c750-137">INPUTobject <IMigrationItem> : Określa serwer replikacji, dla którego należy zainicjować migrację.</span><span class="sxs-lookup"><span data-stu-id="6c750-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="6c750-138">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="6c750-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="6c750-139">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="6c750-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="6c750-140">`[CurrentJobId <String>]`: Identyfikator ARM wykonywanego zadania.</span><span class="sxs-lookup"><span data-stu-id="6c750-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="6c750-141">`[CurrentJobName <String>]`: Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="6c750-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="6c750-142">`[CurrentJobStartTime <DateTime?>]`: Godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="6c750-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="6c750-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="6c750-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="6c750-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c750-144">RELATED LINKS</span></span>

