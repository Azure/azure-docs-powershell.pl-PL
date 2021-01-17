---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356769"
---
# <span data-ttu-id="7da1d-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="7da1d-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="7da1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7da1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da1d-103">Rozpoczyna replikację dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="7da1d-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="7da1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7da1d-104">SYNTAX</span></span>

### <span data-ttu-id="7da1d-105">ByIdDefaultUser (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7da1d-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7da1d-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="7da1d-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7da1d-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="7da1d-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7da1d-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="7da1d-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7da1d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7da1d-109">DESCRIPTION</span></span>
<span data-ttu-id="7da1d-110">Polecenie cmdlet New-AzMigrateServerReplication uruchamia replikację dla konkretnego wykrytego serwera w projekcie migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da1d-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="7da1d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7da1d-111">EXAMPLES</span></span>

### <span data-ttu-id="7da1d-112">Przykład 1. Jeśli jest tylko dysk systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="7da1d-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="7da1d-113">Dotyczy to sytuacji, gdy istnieje tylko jeden dysk, który musi być chroniony.</span><span class="sxs-lookup"><span data-stu-id="7da1d-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="7da1d-114">Przykład 2: Jeśli istnieje wiele dysków</span><span class="sxs-lookup"><span data-stu-id="7da1d-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="7da1d-115">Dotyczy to sytuacji, gdy istnieje wiele dysków, które trzeba chronić.</span><span class="sxs-lookup"><span data-stu-id="7da1d-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="7da1d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7da1d-116">PARAMETERS</span></span>

### <span data-ttu-id="7da1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da1d-117">-DefaultProfile</span></span>
<span data-ttu-id="7da1d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7da1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da1d-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="7da1d-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="7da1d-120">Określa zestaw encyption dysków, który ma być wykorzystywany.</span><span class="sxs-lookup"><span data-stu-id="7da1d-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="7da1d-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="7da1d-121">-DiskToInclude</span></span>
<span data-ttu-id="7da1d-122">Określa dyski serwera źródłowego, które mają zostać uwzględnione w replikacji.</span><span class="sxs-lookup"><span data-stu-id="7da1d-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="7da1d-123">Aby skonstruować, zobacz sekcję notatki dla właściwości DISKTOINCLUDE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="7da1d-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7da1d-124">-Disktype</span><span class="sxs-lookup"><span data-stu-id="7da1d-124">-DiskType</span></span>
<span data-ttu-id="7da1d-125">Określa typ dysków, które mają być używane na potrzeby maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da1d-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da1d-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7da1d-126">-InputObject</span></span>
<span data-ttu-id="7da1d-127">Określa odnaleziony serwer, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="7da1d-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="7da1d-128">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="7da1d-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="7da1d-129">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="7da1d-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7da1d-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7da1d-130">-LicenseType</span></span>
<span data-ttu-id="7da1d-131">Określa, czy korzystanie z usługi Azure hybrydowe jest właściwe dla migracji serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="7da1d-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da1d-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="7da1d-132">-MachineId</span></span>
<span data-ttu-id="7da1d-133">Określa identyfikator komputera wykrytego serwera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="7da1d-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="7da1d-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="7da1d-134">-OSDiskID</span></span>
<span data-ttu-id="7da1d-135">Określa dysk systemu operacyjnego dla serwera źródłowego, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="7da1d-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="7da1d-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="7da1d-136">-PerformAutoResync</span></span>
<span data-ttu-id="7da1d-137">Określa, czy replikacja jest automatycznie naprawiana w przypadku utraty śledzenia zmian w przypadku serwera źródłowego w obszarze replikacja.</span><span class="sxs-lookup"><span data-stu-id="7da1d-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="7da1d-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7da1d-138">-SubscriptionId</span></span>
<span data-ttu-id="7da1d-139">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da1d-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7da1d-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7da1d-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="7da1d-141">Określa zestaw dostępności, który ma być stosowany dla maszyny wirtualnej creationSpecifies zestawu dostępności, który ma być wykorzystywany do tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7da1d-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="7da1d-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="7da1d-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="7da1d-143">Określa strefę dostępności, która ma być używana do tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7da1d-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="7da1d-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7da1d-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="7da1d-145">Określa konto magazynu, które ma być używane do diagnostyki rozruchu.</span><span class="sxs-lookup"><span data-stu-id="7da1d-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="7da1d-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="7da1d-146">-TargetNetworkId</span></span>
<span data-ttu-id="7da1d-147">Określa identyfikator sieci wirtualnej w ramach docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="7da1d-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="7da1d-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7da1d-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="7da1d-149">Określa identyfikator grupy zasobów w ramach docelowej subskrypcji platformy Azure, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="7da1d-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="7da1d-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="7da1d-150">-TargetSubnetName</span></span>
<span data-ttu-id="7da1d-151">Określa nazwę podsieci w docelowym wirtualnym Netowk, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="7da1d-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="7da1d-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="7da1d-152">-TargetVMName</span></span>
<span data-ttu-id="7da1d-153">Określa nazwę maszyny wirtualnej Azure, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="7da1d-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="7da1d-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="7da1d-154">-TargetVMSize</span></span>
<span data-ttu-id="7da1d-155">Określa jednostkę SKU maszyny wirtualnej Azure, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="7da1d-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="7da1d-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="7da1d-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="7da1d-157">Identyfikator konta.</span><span class="sxs-lookup"><span data-stu-id="7da1d-157">Account id.</span></span>

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

### <span data-ttu-id="7da1d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da1d-158">CommonParameters</span></span>
<span data-ttu-id="7da1d-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da1d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da1d-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7da1d-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da1d-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7da1d-161">INPUTS</span></span>

## <span data-ttu-id="7da1d-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7da1d-162">OUTPUTS</span></span>

### <span data-ttu-id="7da1d-163">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="7da1d-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7da1d-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7da1d-164">NOTES</span></span>

<span data-ttu-id="7da1d-165">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7da1d-165">ALIASES</span></span>

<span data-ttu-id="7da1d-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7da1d-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7da1d-167">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7da1d-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7da1d-168">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7da1d-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7da1d-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: określa dyski serwera źródłowego, które mają zostać uwzględnione w replikacji.</span><span class="sxs-lookup"><span data-stu-id="7da1d-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="7da1d-170">`DiskId <String>`: Identyfikator dysku.</span><span class="sxs-lookup"><span data-stu-id="7da1d-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="7da1d-171">`IsOSDisk <String>`: Wartość wskazująca, czy dysk jest dyskiem systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="7da1d-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="7da1d-172">`LogStorageAccountId <String>`: Identyfikator ARM konta dziennika.</span><span class="sxs-lookup"><span data-stu-id="7da1d-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="7da1d-173">`LogStorageAccountSasSecretName <String>`: Poufna nazwa konta dziennika w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="7da1d-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="7da1d-174">`[DiskEncryptionSetId <String>]`: Identyfikator ARM DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="7da1d-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="7da1d-175">`[DiskType <DiskAccountType?>]`: Typ dysku.</span><span class="sxs-lookup"><span data-stu-id="7da1d-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="7da1d-176">INPUTobject <IVMwareMachine> : określa odnaleziony serwer, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="7da1d-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="7da1d-177">Obiekt serwera można pobrać przy użyciu polecenia cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="7da1d-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="7da1d-178">`[GuestOSDetailOstype <String>]`: Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="7da1d-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="7da1d-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7da1d-179">RELATED LINKS</span></span>

