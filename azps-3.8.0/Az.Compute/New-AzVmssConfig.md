---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049260"
---
# <span data-ttu-id="fdf37-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fdf37-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="fdf37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdf37-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf37-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="fdf37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdf37-104">SYNTAX</span></span>

### <span data-ttu-id="fdf37-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fdf37-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf37-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf37-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf37-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf37-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdf37-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fdf37-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf37-109">Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fdf37-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="fdf37-110">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf37-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="fdf37-111">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="fdf37-111">These cmdlets are:</span></span>
- <span data-ttu-id="fdf37-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="fdf37-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="fdf37-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdf37-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="fdf37-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fdf37-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="fdf37-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdf37-116">EXAMPLES</span></span>

### <span data-ttu-id="fdf37-117">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="fdf37-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="fdf37-118">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="fdf37-119">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="fdf37-120">W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="fdf37-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdf37-121">PARAMETERS</span></span>

### <span data-ttu-id="fdf37-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fdf37-122">-AssignIdentity</span></span>
<span data-ttu-id="fdf37-123">Określ tożsamość przypisanego systemu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="fdf37-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="fdf37-125">Ilość czasu, w której automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="fdf37-126">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="fdf37-127">Pomaga to uniknąć przedwczesnych lub przypadkowych napraw.</span><span class="sxs-lookup"><span data-stu-id="fdf37-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="fdf37-128">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="fdf37-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="fdf37-129">Wartość domyślna to 5 minut (PT5M).</span><span class="sxs-lookup"><span data-stu-id="fdf37-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="fdf37-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="fdf37-131">Procent (pojemność scaleset) maszyn wirtualnych, które zostaną jednocześnie naprawione.</span><span class="sxs-lookup"><span data-stu-id="fdf37-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="fdf37-132">Wartość domyślna to 20%.</span><span class="sxs-lookup"><span data-stu-id="fdf37-132">The default value is 20%.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fdf37-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="fdf37-134">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="fdf37-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fdf37-135">-BootDiagnostic</span></span>
<span data-ttu-id="fdf37-136">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-137">-DefaultProfile</span></span>
<span data-ttu-id="fdf37-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf37-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="fdf37-139">-DisableAutoRollback</span></span>
<span data-ttu-id="fdf37-140">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="fdf37-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="fdf37-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="fdf37-142">Włączenie automatycznej naprawy w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fdf37-143">-EnableUltraSSD</span></span>
<span data-ttu-id="fdf37-144">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="fdf37-145">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="fdf37-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf37-146">-EvictionPolicy</span></span>
<span data-ttu-id="fdf37-147">Określa zasady wykluczania dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="fdf37-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-148">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="fdf37-148">-Extension</span></span>
<span data-ttu-id="fdf37-149">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="fdf37-150">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="fdf37-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="fdf37-151">-HealthProbeId</span></span>
<span data-ttu-id="fdf37-152">Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="fdf37-153">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="fdf37-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="fdf37-154">-IdentityId</span></span>
<span data-ttu-id="fdf37-155">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="fdf37-156">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="fdf37-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fdf37-157">-IdentityType</span></span>
<span data-ttu-id="fdf37-158">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="fdf37-159">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fdf37-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="fdf37-160">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="fdf37-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fdf37-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdf37-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="fdf37-162">SystemAssigned</span></span>
- <span data-ttu-id="fdf37-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="fdf37-163">UserAssigned</span></span>
- <span data-ttu-id="fdf37-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="fdf37-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="fdf37-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fdf37-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fdf37-166">-LicenseType</span></span>
<span data-ttu-id="fdf37-167">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="fdf37-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-168">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fdf37-168">-Location</span></span>
<span data-ttu-id="fdf37-169">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fdf37-170">-MaxPrice</span></span>
<span data-ttu-id="fdf37-171">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="fdf37-172">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="fdf37-172">This price is in US Dollars.</span></span> <span data-ttu-id="fdf37-173">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="fdf37-174">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="fdf37-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="fdf37-175">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="fdf37-176">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="fdf37-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="fdf37-177">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="fdf37-177">Example: 0.01538.</span></span>  <span data-ttu-id="fdf37-178">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="fdf37-179">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="fdf37-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdf37-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="fdf37-181">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="fdf37-182">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fdf37-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-183">-OsProfile</span></span>
<span data-ttu-id="fdf37-184">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="fdf37-185">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="fdf37-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-186">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="fdf37-186">-Overprovision</span></span>
<span data-ttu-id="fdf37-187">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="fdf37-188">-PlanName</span></span>
<span data-ttu-id="fdf37-189">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="fdf37-190">-PlanProduct</span></span>
<span data-ttu-id="fdf37-191">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="fdf37-192">-PlanPromotionCode</span></span>
<span data-ttu-id="fdf37-193">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fdf37-194">-PlanPublisher</span></span>
<span data-ttu-id="fdf37-195">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fdf37-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fdf37-197">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="fdf37-197">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-198">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="fdf37-198">-Priority</span></span>
<span data-ttu-id="fdf37-199">Priorytet machien wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="fdf37-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="fdf37-200">Obsługiwane są tylko wartości "Regular", "spot" i "Low".</span><span class="sxs-lookup"><span data-stu-id="fdf37-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="fdf37-201">"Zwykła" dotyczy zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="fdf37-202">"Miejsce na maszynie wirtualnej" jest na miejscu.</span><span class="sxs-lookup"><span data-stu-id="fdf37-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="fdf37-203">"Niski" jest również na odniesieniu do maszyny wirtualnej, ale został zastąpiony przez "punkt".</span><span class="sxs-lookup"><span data-stu-id="fdf37-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="fdf37-204">Użyj "spot" zamiast "niski".</span><span class="sxs-lookup"><span data-stu-id="fdf37-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fdf37-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fdf37-206">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="fdf37-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="fdf37-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="fdf37-208">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="fdf37-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf37-209">-ScaleInPolicy</span></span>
<span data-ttu-id="fdf37-210">Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fdf37-211">Możliwe wartości: "default", "OldestVM" i "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="fdf37-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fdf37-212">"Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.</span><span class="sxs-lookup"><span data-stu-id="fdf37-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fdf37-213">Następnie będzie on w miarę możliwości równoważony między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="fdf37-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fdf37-214">W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.</span><span class="sxs-lookup"><span data-stu-id="fdf37-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fdf37-215">OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="fdf37-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fdf37-216">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="fdf37-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fdf37-217">W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="fdf37-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fdf37-218">NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="fdf37-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fdf37-219">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="fdf37-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fdf37-220">W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="fdf37-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf37-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="fdf37-222">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="fdf37-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="fdf37-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fdf37-224">Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="fdf37-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fdf37-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fdf37-225">-SkuCapacity</span></span>
<span data-ttu-id="fdf37-226">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fdf37-227">-SkuName</span></span>
<span data-ttu-id="fdf37-228">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fdf37-229">-SkuTier</span></span>
<span data-ttu-id="fdf37-230">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="fdf37-231">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fdf37-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdf37-232">Standard</span><span class="sxs-lookup"><span data-stu-id="fdf37-232">Standard</span></span>
- <span data-ttu-id="fdf37-233">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="fdf37-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-234">-StorageProfile</span></span>
<span data-ttu-id="fdf37-235">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="fdf37-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="fdf37-236">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="fdf37-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-237">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdf37-237">-Tag</span></span>
<span data-ttu-id="fdf37-238">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fdf37-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fdf37-239">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fdf37-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fdf37-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="fdf37-241">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="fdf37-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="fdf37-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="fdf37-243">Włączanie kończenia zaplanowanych zdarzeń</span><span class="sxs-lookup"><span data-stu-id="fdf37-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fdf37-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="fdf37-245">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="fdf37-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="fdf37-246">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fdf37-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdf37-247">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="fdf37-247">Automatic</span></span>
- <span data-ttu-id="fdf37-248">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="fdf37-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-249">-Zone</span><span class="sxs-lookup"><span data-stu-id="fdf37-249">-Zone</span></span>
<span data-ttu-id="fdf37-250">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdf37-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="fdf37-251">-ZoneBalance</span></span>
<span data-ttu-id="fdf37-252">Czy należy wymusić ścisłe, nawet strefy krzyżowe funkcji dystrybucji maszyn wirtualnych na wypadek awarii strefy.</span><span class="sxs-lookup"><span data-stu-id="fdf37-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="fdf37-253">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdf37-253">-Confirm</span></span>
<span data-ttu-id="fdf37-254">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf37-254">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf37-255">-WhatIf</span></span>
<span data-ttu-id="fdf37-256">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf37-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdf37-257">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdf37-257">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf37-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf37-258">CommonParameters</span></span>
<span data-ttu-id="fdf37-259">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf37-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf37-260">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdf37-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf37-261">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdf37-261">INPUTS</span></span>

### <span data-ttu-id="fdf37-262">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fdf37-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fdf37-263">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf37-263">System.String</span></span>

### <span data-ttu-id="fdf37-264">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fdf37-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fdf37-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fdf37-265">System.Int32</span></span>

### <span data-ttu-id="fdf37-266">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. MODELES. Upgrademode; Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fdf37-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fdf37-267">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="fdf37-268">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="fdf37-269">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="fdf37-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="fdf37-270">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="fdf37-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="fdf37-271">System. String []</span><span class="sxs-lookup"><span data-stu-id="fdf37-271">System.String[]</span></span>

### <span data-ttu-id="fdf37-272">Microsoft. Azure. Management. COMPUTE. MODELES. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="fdf37-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="fdf37-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fdf37-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fdf37-274">Microsoft. Azure. Management. COMPUTE. MODELES. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fdf37-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="fdf37-275">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ResourceIdentityType, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="fdf37-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="fdf37-276">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdf37-276">OUTPUTS</span></span>

### <span data-ttu-id="fdf37-277">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fdf37-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fdf37-278">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdf37-278">NOTES</span></span>

## <span data-ttu-id="fdf37-279">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdf37-279">RELATED LINKS</span></span>

[<span data-ttu-id="fdf37-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="fdf37-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fdf37-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="fdf37-282">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdf37-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="fdf37-283">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fdf37-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="fdf37-284">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="fdf37-284">New-AzVmss</span></span>](./New-AzVmss.md)
