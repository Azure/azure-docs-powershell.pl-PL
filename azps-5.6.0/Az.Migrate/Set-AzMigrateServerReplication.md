---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009585"
---
# <span data-ttu-id="e242c-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="e242c-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="e242c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e242c-102">SYNOPSIS</span></span>
<span data-ttu-id="e242c-103">Aktualizuje właściwości docelowe serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="e242c-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="e242c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e242c-104">SYNTAX</span></span>

### <span data-ttu-id="e242c-105">ByIDVBlockCbt (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e242c-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e242c-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="e242c-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e242c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e242c-107">DESCRIPTION</span></span>
<span data-ttu-id="e242c-108">Polecenie Set-AzMigrateServerReplication aktualizuje właściwości docelowe serwera replikowania.</span><span class="sxs-lookup"><span data-stu-id="e242c-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="e242c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e242c-109">EXAMPLES</span></span>

### <span data-ttu-id="e242c-110">Przykład 1. Aktualizacja według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e242c-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="e242c-111">Według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e242c-111">By id.</span></span>

## <span data-ttu-id="e242c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e242c-112">PARAMETERS</span></span>

### <span data-ttu-id="e242c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e242c-113">-DefaultProfile</span></span>
<span data-ttu-id="e242c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e242c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e242c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e242c-115">-InputObject</span></span>
<span data-ttu-id="e242c-116">Określa serwer replikowania, dla którego trzeba zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="e242c-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="e242c-117">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e242c-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="e242c-118">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="e242c-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e242c-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="e242c-119">-NicToUpdate</span></span>
<span data-ttu-id="e242c-120">Aktualizuje kartę NIC dla maszyny wirtualnej platformy Azure, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="e242c-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="e242c-121">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach NICTOUPDATE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="e242c-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e242c-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e242c-122">-SubscriptionId</span></span>
<span data-ttu-id="e242c-123">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e242c-123">The subscription Id.</span></span>

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

### <span data-ttu-id="e242c-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e242c-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="e242c-125">Określa zestaw dostępności używany do tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e242c-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="e242c-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="e242c-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="e242c-127">Określa strefę dostępności, która ma być używana do tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e242c-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="e242c-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e242c-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="e242c-129">Określa konto magazynu, które ma być używane do diagnostyki rozruchu.</span><span class="sxs-lookup"><span data-stu-id="e242c-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="e242c-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="e242c-130">-TargetNetworkId</span></span>
<span data-ttu-id="e242c-131">Aktualizuje identyfikator wirtualnej sieci w docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="e242c-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="e242c-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="e242c-132">-TargetObjectID</span></span>
<span data-ttu-id="e242c-133">Określa serwer, dla którego trzeba zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="e242c-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="e242c-134">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e242c-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="e242c-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="e242c-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="e242c-136">Aktualizuje identyfikator grupy zasobów w docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="e242c-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="e242c-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="e242c-137">-TargetVMName</span></span>
<span data-ttu-id="e242c-138">Określa serwer, dla którego trzeba zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="e242c-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="e242c-139">Identyfikator powinien zostać pobrany przy użyciu Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e242c-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="e242c-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="e242c-140">-TargetVMSize</span></span>
<span data-ttu-id="e242c-141">Aktualizuje sku maszyny wirtualnej platformy Azure, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="e242c-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="e242c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e242c-142">CommonParameters</span></span>
<span data-ttu-id="e242c-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e242c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e242c-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e242c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e242c-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e242c-145">INPUTS</span></span>

## <span data-ttu-id="e242c-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e242c-146">OUTPUTS</span></span>

### <span data-ttu-id="e242c-147">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="e242c-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="e242c-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e242c-148">NOTES</span></span>

<span data-ttu-id="e242c-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e242c-149">ALIASES</span></span>

<span data-ttu-id="e242c-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e242c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e242c-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e242c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e242c-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e242c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e242c-153">INPUTOBJECT: <IMigrationItem> Określa serwer replikowania, dla którego należy zaktualizować właściwości.</span><span class="sxs-lookup"><span data-stu-id="e242c-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="e242c-154">Obiekt serwera można pobrać za pomocą Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e242c-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="e242c-155">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="e242c-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="e242c-156">`[CurrentJobId <String>]`: ARM identyfikatora zadania do wykonania.</span><span class="sxs-lookup"><span data-stu-id="e242c-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="e242c-157">`[CurrentJobName <String>]`: nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="e242c-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="e242c-158">`[CurrentJobStartTime <DateTime?>]`: godzina rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="e242c-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="e242c-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Ustawienia niestandardowe dostawcy migracji.</span><span class="sxs-lookup"><span data-stu-id="e242c-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="e242c-160">NICTOUPDATE <IVCbtNicInput[]>: Aktualizuje kartę NIC dla maszyny wirtualnej platformy Azure, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="e242c-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="e242c-161">`IsPrimaryNic <String>`: wartość wskazująca, czy jest to podstawowa wartość NIC.</span><span class="sxs-lookup"><span data-stu-id="e242c-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="e242c-162">`NicId <String>`: Identyfikator NIC.</span><span class="sxs-lookup"><span data-stu-id="e242c-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="e242c-163">`[IsSelectedForMigration <String>]`: wartość wskazująca, czy ta karta NIC jest wybrana do migracji.</span><span class="sxs-lookup"><span data-stu-id="e242c-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="e242c-164">`[TargetStaticIPAddress <String>]`: statyczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="e242c-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="e242c-165">`[TargetSubnetName <String>]`: docelowa nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="e242c-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="e242c-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e242c-166">RELATED LINKS</span></span>

