---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063587"
---
# <span data-ttu-id="7f14d-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7f14d-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="7f14d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f14d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f14d-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="7f14d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f14d-104">SYNTAX</span></span>

### <span data-ttu-id="7f14d-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f14d-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f14d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f14d-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f14d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7f14d-107">DESCRIPTION</span></span>
<span data-ttu-id="7f14d-108">Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7f14d-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="7f14d-109">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f14d-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="7f14d-110">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="7f14d-110">These cmdlets are:</span></span>
- <span data-ttu-id="7f14d-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="7f14d-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="7f14d-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f14d-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="7f14d-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7f14d-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="7f14d-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f14d-115">EXAMPLES</span></span>

### <span data-ttu-id="7f14d-116">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="7f14d-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="7f14d-117">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="7f14d-118">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="7f14d-119">W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="7f14d-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7f14d-120">Example 2</span></span>

<span data-ttu-id="7f14d-121">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="7f14d-122">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="7f14d-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="7f14d-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f14d-123">PARAMETERS</span></span>

### <span data-ttu-id="7f14d-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="7f14d-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="7f14d-125">Ilość czasu, w której automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="7f14d-126">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="7f14d-127">Pomaga to uniknąć przedwczesnych lub przypadkowych napraw.</span><span class="sxs-lookup"><span data-stu-id="7f14d-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="7f14d-128">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="7f14d-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="7f14d-129">Minimalny dozwolony okres prolongaty to 30 minut (PT30M), który jest również wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="7f14d-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="7f14d-130">Maksymalny dozwolony okres prolongaty to 90 minut (PT90M).</span><span class="sxs-lookup"><span data-stu-id="7f14d-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="7f14d-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7f14d-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="7f14d-132">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="7f14d-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7f14d-133">-BootDiagnostic</span></span>
<span data-ttu-id="7f14d-134">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="7f14d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-135">-DefaultProfile</span></span>
<span data-ttu-id="7f14d-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f14d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f14d-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="7f14d-137">-DisableAutoRollback</span></span>
<span data-ttu-id="7f14d-138">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="7f14d-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="7f14d-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="7f14d-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="7f14d-140">Włączenie automatycznej naprawy w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7f14d-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7f14d-141">-EnableUltraSSD</span></span>
<span data-ttu-id="7f14d-142">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="7f14d-143">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="7f14d-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="7f14d-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="7f14d-144">-EncryptionAtHost</span></span>
<span data-ttu-id="7f14d-145">Ten parametr umożliwia szyfrowanie wszystkich dysków, w tym dysku Resource/temp, na hoście.</span><span class="sxs-lookup"><span data-stu-id="7f14d-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="7f14d-146">Wartość domyślna: szyfrowanie na hoście zostanie wyłączone, chyba że dla tego zasobu zostanie ustawiona wartość true dla tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="7f14d-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="7f14d-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7f14d-147">-EvictionPolicy</span></span>
<span data-ttu-id="7f14d-148">Określa zasady wykluczania dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="7f14d-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="7f14d-149">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="7f14d-149">-Extension</span></span>
<span data-ttu-id="7f14d-150">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="7f14d-151">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="7f14d-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="7f14d-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="7f14d-152">-HealthProbeId</span></span>
<span data-ttu-id="7f14d-153">Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="7f14d-154">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="7f14d-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="7f14d-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7f14d-155">-IdentityId</span></span>
<span data-ttu-id="7f14d-156">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7f14d-157">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="7f14d-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7f14d-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7f14d-158">-IdentityType</span></span>
<span data-ttu-id="7f14d-159">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="7f14d-160">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7f14d-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="7f14d-161">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="7f14d-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f14d-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f14d-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7f14d-163">SystemAssigned</span></span>
- <span data-ttu-id="7f14d-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="7f14d-164">UserAssigned</span></span>
- <span data-ttu-id="7f14d-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="7f14d-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="7f14d-166">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f14d-166">None</span></span>

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

### <span data-ttu-id="7f14d-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7f14d-167">-LicenseType</span></span>
<span data-ttu-id="7f14d-168">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="7f14d-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="7f14d-169">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f14d-169">-Location</span></span>
<span data-ttu-id="7f14d-170">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="7f14d-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7f14d-171">-MaxPrice</span></span>
<span data-ttu-id="7f14d-172">Określa cenę maksymalną, jaką należy zapłacić za dodatkowe maszyny wirtualne lub VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="7f14d-173">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="7f14d-173">This price is in US Dollars.</span></span> <span data-ttu-id="7f14d-174">Ta cena będzie porównywana z bieżącą ceną na miejscu w danym rozmiarze maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="7f14d-175">Ceny są również porównywane w czasie tworzenia/aktualizowania dodatkowych maszyn wirtualnych/VMSS, a operacja będzie działać tylko wtedy, gdy maxPrice jest większa niż bieżąca cena.</span><span class="sxs-lookup"><span data-stu-id="7f14d-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="7f14d-176">MaxPrice będzie również stosowany do wykluczania dodatkowych maszyn wirtualnych/VMSS, jeśli bieżąca cena na miejscu przekracza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7f14d-177">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="7f14d-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7f14d-178">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="7f14d-178">Example: 0.01538.</span></span>  <span data-ttu-id="7f14d-179">-1 wskazuje, że docelowa maszyna wirtualna/VMSS nie powinna być wykluczona ze względu na cenę.</span><span class="sxs-lookup"><span data-stu-id="7f14d-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7f14d-180">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="7f14d-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="7f14d-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f14d-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="7f14d-182">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="7f14d-183">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7f14d-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="7f14d-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-184">-OsProfile</span></span>
<span data-ttu-id="7f14d-185">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="7f14d-186">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="7f14d-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="7f14d-187">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="7f14d-187">-Overprovision</span></span>
<span data-ttu-id="7f14d-188">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="7f14d-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7f14d-189">-PlanName</span></span>
<span data-ttu-id="7f14d-190">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="7f14d-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="7f14d-191">-PlanProduct</span></span>
<span data-ttu-id="7f14d-192">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="7f14d-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="7f14d-193">-PlanPromotionCode</span></span>
<span data-ttu-id="7f14d-194">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="7f14d-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7f14d-195">-PlanPublisher</span></span>
<span data-ttu-id="7f14d-196">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="7f14d-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="7f14d-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="7f14d-198">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="7f14d-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="7f14d-199">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="7f14d-199">-Priority</span></span>
<span data-ttu-id="7f14d-200">Priorytet machien wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="7f14d-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="7f14d-201">Obsługiwane są tylko wartości "Regular", "spot" i "Low".</span><span class="sxs-lookup"><span data-stu-id="7f14d-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="7f14d-202">"Zwykła" dotyczy zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="7f14d-203">"Miejsce na maszynie wirtualnej" jest na miejscu.</span><span class="sxs-lookup"><span data-stu-id="7f14d-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="7f14d-204">"Niski" jest również na odniesieniu do maszyny wirtualnej, ale został zastąpiony przez "punkt".</span><span class="sxs-lookup"><span data-stu-id="7f14d-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="7f14d-205">Użyj "spot" zamiast "niski".</span><span class="sxs-lookup"><span data-stu-id="7f14d-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="7f14d-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7f14d-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7f14d-207">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="7f14d-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="7f14d-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7f14d-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="7f14d-209">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="7f14d-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="7f14d-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="7f14d-210">-ScaleInPolicy</span></span>
<span data-ttu-id="7f14d-211">Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="7f14d-212">Możliwe wartości: "default", "OldestVM" i "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="7f14d-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="7f14d-213">"Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.</span><span class="sxs-lookup"><span data-stu-id="7f14d-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="7f14d-214">Następnie będzie on w miarę możliwości równoważony między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="7f14d-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="7f14d-215">W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.</span><span class="sxs-lookup"><span data-stu-id="7f14d-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="7f14d-216">OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="7f14d-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7f14d-217">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="7f14d-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7f14d-218">W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="7f14d-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="7f14d-219">NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="7f14d-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7f14d-220">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="7f14d-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7f14d-221">W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="7f14d-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="7f14d-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7f14d-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="7f14d-223">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="7f14d-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="7f14d-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="7f14d-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="7f14d-225">Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7f14d-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="7f14d-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7f14d-226">-SkuCapacity</span></span>
<span data-ttu-id="7f14d-227">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="7f14d-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7f14d-228">-SkuName</span></span>
<span data-ttu-id="7f14d-229">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="7f14d-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7f14d-230">-SkuTier</span></span>
<span data-ttu-id="7f14d-231">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="7f14d-232">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f14d-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f14d-233">Standard</span><span class="sxs-lookup"><span data-stu-id="7f14d-233">Standard</span></span>
- <span data-ttu-id="7f14d-234">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="7f14d-234">Basic</span></span>

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

### <span data-ttu-id="7f14d-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-235">-StorageProfile</span></span>
<span data-ttu-id="7f14d-236">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f14d-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="7f14d-237">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="7f14d-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="7f14d-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f14d-238">-Tag</span></span>
<span data-ttu-id="7f14d-239">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7f14d-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f14d-240">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7f14d-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7f14d-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7f14d-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="7f14d-242">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="7f14d-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="7f14d-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="7f14d-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="7f14d-244">Włączanie kończenia zaplanowanych zdarzeń</span><span class="sxs-lookup"><span data-stu-id="7f14d-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="7f14d-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7f14d-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="7f14d-246">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7f14d-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="7f14d-247">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f14d-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f14d-248">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="7f14d-248">Automatic</span></span>
- <span data-ttu-id="7f14d-249">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="7f14d-249">Manual</span></span>

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

### <span data-ttu-id="7f14d-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="7f14d-250">-Zone</span></span>
<span data-ttu-id="7f14d-251">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7f14d-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7f14d-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="7f14d-252">-ZoneBalance</span></span>
<span data-ttu-id="7f14d-253">Czy należy wymusić ścisłe, nawet strefy krzyżowe funkcji dystrybucji maszyn wirtualnych na wypadek awarii strefy.</span><span class="sxs-lookup"><span data-stu-id="7f14d-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="7f14d-254">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f14d-254">-Confirm</span></span>
<span data-ttu-id="7f14d-255">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f14d-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f14d-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f14d-256">-WhatIf</span></span>
<span data-ttu-id="7f14d-257">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f14d-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f14d-258">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f14d-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f14d-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f14d-259">CommonParameters</span></span>
<span data-ttu-id="7f14d-260">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f14d-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f14d-261">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f14d-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f14d-262">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f14d-262">INPUTS</span></span>

### <span data-ttu-id="7f14d-263">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f14d-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7f14d-264">System. String</span><span class="sxs-lookup"><span data-stu-id="7f14d-264">System.String</span></span>

### <span data-ttu-id="7f14d-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f14d-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7f14d-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7f14d-266">System.Int32</span></span>

### <span data-ttu-id="7f14d-267">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. MODELES. Upgrademode; Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7f14d-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7f14d-268">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="7f14d-269">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="7f14d-270">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7f14d-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="7f14d-271">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="7f14d-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="7f14d-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f14d-272">System.String[]</span></span>

### <span data-ttu-id="7f14d-273">Microsoft. Azure. Management. COMPUTE. MODELES. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7f14d-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="7f14d-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f14d-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7f14d-275">Microsoft. Azure. Management. COMPUTE. MODELES. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7f14d-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="7f14d-276">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ResourceIdentityType, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="7f14d-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7f14d-277">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f14d-277">OUTPUTS</span></span>

### <span data-ttu-id="7f14d-278">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7f14d-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7f14d-279">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f14d-279">NOTES</span></span>

## <span data-ttu-id="7f14d-280">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f14d-280">RELATED LINKS</span></span>

[<span data-ttu-id="7f14d-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="7f14d-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7f14d-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="7f14d-283">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f14d-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="7f14d-284">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7f14d-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="7f14d-285">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f14d-285">New-AzVmss</span></span>](./New-AzVmss.md)
