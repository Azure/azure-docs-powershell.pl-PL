---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975729"
---
# <span data-ttu-id="71b50-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="71b50-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="71b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b50-102">SYNOPSIS</span></span>
<span data-ttu-id="71b50-103">Uruchamia replikację dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="71b50-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="71b50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71b50-104">SYNTAX</span></span>

### <span data-ttu-id="71b50-105">ByIdDefaultUser (domyślne)</span><span class="sxs-lookup"><span data-stu-id="71b50-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71b50-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="71b50-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71b50-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="71b50-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71b50-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="71b50-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71b50-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="71b50-109">DESCRIPTION</span></span>
<span data-ttu-id="71b50-110">Polecenie New-AzMigrateServerReplication uruchamia replikację konkretnego serwera wykrytego w projekcie migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71b50-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="71b50-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71b50-111">EXAMPLES</span></span>

### <span data-ttu-id="71b50-112">Przykład 1. Jeśli jest tylko dysk systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="71b50-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="71b50-113">Dotyczy to sytuacji, w których jest tylko jeden dysk, który musi być chroniony.</span><span class="sxs-lookup"><span data-stu-id="71b50-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="71b50-114">Przykład 2. Gdy jest wiele dyskietek</span><span class="sxs-lookup"><span data-stu-id="71b50-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="71b50-115">Dotyczy to sytuacji, w których istnieje wiele dyskietek, które muszą być chronione.</span><span class="sxs-lookup"><span data-stu-id="71b50-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="71b50-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71b50-116">PARAMETERS</span></span>

### <span data-ttu-id="71b50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b50-117">-DefaultProfile</span></span>
<span data-ttu-id="71b50-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71b50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71b50-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="71b50-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="71b50-120">Określa zestaw encypcji dysku, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="71b50-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="71b50-121">-DiskToInclude</span></span>
<span data-ttu-id="71b50-122">Określa dysk dysk na serwerze źródłowym, który ma zostać uwzględniony w celu replikacji.</span><span class="sxs-lookup"><span data-stu-id="71b50-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="71b50-123">Aby skonstruować, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach DISKTOINCLUDE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="71b50-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="71b50-124">-DiskType</span></span>
<span data-ttu-id="71b50-125">Określa typ dysków, które mają być używane dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71b50-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71b50-126">-InputObject</span></span>
<span data-ttu-id="71b50-127">Określa serwer, który ma zostać podmigrowany.</span><span class="sxs-lookup"><span data-stu-id="71b50-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="71b50-128">Obiekt serwera można pobrać za pomocą Get-AzMigrateServer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b50-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="71b50-129">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="71b50-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="71b50-130">-LicenseType</span></span>
<span data-ttu-id="71b50-131">Określa, czy dla serwera źródłowego, który ma zostać zmigrowany, ma zastosowanie korzyść hybrydowa platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71b50-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="71b50-132">— MachineId</span><span class="sxs-lookup"><span data-stu-id="71b50-132">-MachineId</span></span>
<span data-ttu-id="71b50-133">Określa identyfikator komputera wykrytego serwera do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="71b50-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-134">-OS JednakowyID</span><span class="sxs-lookup"><span data-stu-id="71b50-134">-OSDiskID</span></span>
<span data-ttu-id="71b50-135">Określa dysk systemu operacyjnego dla serwera źródłowego, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="71b50-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b50-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="71b50-136">-PerformAutoResync</span></span>
<span data-ttu-id="71b50-137">Określa, czy replikacja zostanie naprawiona automatycznie w przypadku, gdy śledzenie zmian dla serwera źródłowego w ramach replikacji zostanie utracone.</span><span class="sxs-lookup"><span data-stu-id="71b50-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="71b50-138">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71b50-138">-SubscriptionId</span></span>
<span data-ttu-id="71b50-139">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71b50-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="71b50-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="71b50-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="71b50-141">Określa zestaw dostępności używany do tworzenia maszyn wirtualnych określa zestaw dostępności używany do tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="71b50-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="71b50-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="71b50-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="71b50-143">Określa strefę dostępności, która ma być używana do tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="71b50-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="71b50-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71b50-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="71b50-145">Określa konto magazynu, które ma być używane do diagnostyki rozruchu.</span><span class="sxs-lookup"><span data-stu-id="71b50-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="71b50-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="71b50-146">-TargetNetworkId</span></span>
<span data-ttu-id="71b50-147">Określa identyfikator sieci wirtualnej w docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="71b50-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="71b50-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="71b50-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="71b50-149">Określa identyfikator grupy zasobów w docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="71b50-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="71b50-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="71b50-150">-TargetSubnetName</span></span>
<span data-ttu-id="71b50-151">Określa nazwę podsieci w docelowym środowisku wirtualnym Netowk, do którego należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="71b50-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="71b50-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="71b50-152">-TargetVMName</span></span>
<span data-ttu-id="71b50-153">Określa nazwę maszyny wirtualnej platformy Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="71b50-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="71b50-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="71b50-154">-TargetVMSize</span></span>
<span data-ttu-id="71b50-155">Określa sku maszyny wirtualnej platformy Azure, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="71b50-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="71b50-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="71b50-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="71b50-157">Identyfikator konta.</span><span class="sxs-lookup"><span data-stu-id="71b50-157">Account id.</span></span>

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

### <span data-ttu-id="71b50-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b50-158">CommonParameters</span></span>
<span data-ttu-id="71b50-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b50-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b50-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71b50-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b50-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b50-161">INPUTS</span></span>

## <span data-ttu-id="71b50-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b50-162">OUTPUTS</span></span>

### <span data-ttu-id="71b50-163">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iJob</span><span class="sxs-lookup"><span data-stu-id="71b50-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="71b50-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71b50-164">NOTES</span></span>

<span data-ttu-id="71b50-165">ALIASY</span><span class="sxs-lookup"><span data-stu-id="71b50-165">ALIASES</span></span>

<span data-ttu-id="71b50-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71b50-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71b50-167">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="71b50-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71b50-168">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71b50-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71b50-169">DISKTOINCLUDE <IVCbt Jednak[]>: Określa dysk, który ma zostać uwzględniony na serwerze źródłowym w celu replikacji.</span><span class="sxs-lookup"><span data-stu-id="71b50-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="71b50-170">`DiskId <String>`: Identyfikator dysku.</span><span class="sxs-lookup"><span data-stu-id="71b50-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="71b50-171">`IsOSDisk <String>`: wartość wskazująca, czy dysk jest dyskiem systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="71b50-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="71b50-172">`LogStorageAccountId <String>`: Konto magazynu dziennika ARM identyfikator.</span><span class="sxs-lookup"><span data-stu-id="71b50-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="71b50-173">`LogStorageAccountSasSecretName <String>`: tajna nazwa magazynu kluczy konta magazynu dziennika.</span><span class="sxs-lookup"><span data-stu-id="71b50-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="71b50-174">`[DiskEncryptionSetId <String>]`: Identyfikator ARM DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="71b50-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="71b50-175">`[DiskType <DiskAccountType?>]`: typ dysku.</span><span class="sxs-lookup"><span data-stu-id="71b50-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="71b50-176">INPUTOBJECT: Określa serwer, który ma zostać <IVMwareMachine> podmigrowany.</span><span class="sxs-lookup"><span data-stu-id="71b50-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="71b50-177">Obiekt serwera można pobrać za pomocą Get-AzMigrateServer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b50-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="71b50-178">`[GuestOSDetailOstype <String>]`: typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="71b50-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="71b50-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71b50-179">RELATED LINKS</span></span>

