---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233091"
---
# <span data-ttu-id="cbab4-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="cbab4-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="cbab4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbab4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbab4-103">Umożliwia zaktualizowanie właściwości docelowych serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="cbab4-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cbab4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbab4-104">SYNTAX</span></span>

### <span data-ttu-id="cbab4-105">ByIDVMwareCbt (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cbab4-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbab4-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="cbab4-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cbab4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cbab4-107">DESCRIPTION</span></span>
<span data-ttu-id="cbab4-108">Polecenie cmdlet Set-AzMigrateServerReplication aktualizuje właściwości docelowe serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="cbab4-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cbab4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbab4-109">EXAMPLES</span></span>

### <span data-ttu-id="cbab4-110">Przykład 1: Aktualizacja według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="cbab4-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="cbab4-111">Według identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="cbab4-111">By id.</span></span>

## <span data-ttu-id="cbab4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbab4-112">PARAMETERS</span></span>

### <span data-ttu-id="cbab4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbab4-113">-DefaultProfile</span></span>
<span data-ttu-id="cbab4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbab4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbab4-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cbab4-115">-InputObject</span></span>
<span data-ttu-id="cbab4-116">Określa serwer replikacji, dla którego należy zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="cbab4-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbab4-117">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cbab4-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="cbab4-118">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="cbab4-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbab4-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="cbab4-119">-NicToUpdate</span></span>
<span data-ttu-id="cbab4-120">Umożliwia zaktualizowanie karty interfejsu maszyny wirtualnej usługi Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="cbab4-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="cbab4-121">Aby skonstruować, zobacz sekcję notatki dla właściwości NICTOUPDATE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="cbab4-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbab4-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cbab4-122">-SubscriptionId</span></span>
<span data-ttu-id="cbab4-123">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="cbab4-123">The subscription Id.</span></span>

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

### <span data-ttu-id="cbab4-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cbab4-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="cbab4-125">Określa zestaw dostępności, który ma być wykorzystywany do tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cbab4-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="cbab4-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="cbab4-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="cbab4-127">Określa strefę dostępności, która ma być używana do tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cbab4-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="cbab4-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="cbab4-128">-TargetNetworkId</span></span>
<span data-ttu-id="cbab4-129">Aktualizuje identyfikator sieci wirtualnej w ramach docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="cbab4-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cbab4-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="cbab4-130">-TargetObjectID</span></span>
<span data-ttu-id="cbab4-131">Określa serwer replcating, dla którego należy zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="cbab4-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbab4-132">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cbab4-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cbab4-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="cbab4-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="cbab4-134">Aktualizuje identyfikator grupy zasobów w ramach docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="cbab4-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cbab4-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="cbab4-135">-TargetVMName</span></span>
<span data-ttu-id="cbab4-136">Określa serwer replcating, dla którego należy zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="cbab4-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbab4-137">Identyfikator należy pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cbab4-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cbab4-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="cbab4-138">-TargetVMSize</span></span>
<span data-ttu-id="cbab4-139">Umożliwia zaktualizowanie jednostki SKU maszyny wirtualnej usługi Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="cbab4-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="cbab4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbab4-140">CommonParameters</span></span>
<span data-ttu-id="cbab4-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbab4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbab4-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbab4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbab4-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbab4-143">INPUTS</span></span>

## <span data-ttu-id="cbab4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbab4-144">OUTPUTS</span></span>

### <span data-ttu-id="cbab4-145">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="cbab4-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="cbab4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbab4-146">NOTES</span></span>

<span data-ttu-id="cbab4-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cbab4-147">ALIASES</span></span>

<span data-ttu-id="cbab4-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbab4-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbab4-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cbab4-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbab4-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbab4-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbab4-151">INPUTobject <IMigrationItem> : Określa serwer replikacji, dla którego należy zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="cbab4-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="cbab4-152">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cbab4-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="cbab4-153">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="cbab4-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="cbab4-154">`[CurrentJobId <String>]`: Identyfikator ARM wykonywanego zadania.</span><span class="sxs-lookup"><span data-stu-id="cbab4-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="cbab4-155">`[CurrentJobName <String>]`: Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="cbab4-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="cbab4-156">`[CurrentJobStartTime <DateTime?>]`: Godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="cbab4-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="cbab4-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="cbab4-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="cbab4-158">NICTOUPDATE <IVMwareCbtNicInput [] >: umożliwia zaktualizowanie karty interfejsu maszyny wirtualnej usługi Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="cbab4-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="cbab4-159">`IsPrimaryNic <String>`: Wartość wskazująca, czy jest to podstawowa karta sieciowa.</span><span class="sxs-lookup"><span data-stu-id="cbab4-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="cbab4-160">`NicId <String>`: Identyfikator karty sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cbab4-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="cbab4-161">`[IsSelectedForMigration <String>]`: Wartość wskazująca, czy ta karta sieciowa jest wybrana do migracji.</span><span class="sxs-lookup"><span data-stu-id="cbab4-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="cbab4-162">`[TargetStaticIPAddress <String>]`: Statyczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="cbab4-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="cbab4-163">`[TargetSubnetName <String>]`: Nazwa podsieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="cbab4-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="cbab4-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbab4-164">RELATED LINKS</span></span>

