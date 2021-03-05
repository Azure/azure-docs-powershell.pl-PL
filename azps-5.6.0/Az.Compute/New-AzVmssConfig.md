---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: ba44e397aa09834b1371fa9188527a056153017c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988408"
---
# <span data-ttu-id="937d4-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="937d4-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="937d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937d4-102">SYNOPSIS</span></span>
<span data-ttu-id="937d4-103">Tworzy obiekt konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="937d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="937d4-104">SYNTAX</span></span>

### <span data-ttu-id="937d4-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="937d4-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="937d4-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="937d4-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="937d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="937d4-107">DESCRIPTION</span></span>
<span data-ttu-id="937d4-108">Polecenie **cmdlet New-AzVmssConfig** tworzy konfigurowalny lokalny obiekt VIRTUAL Manager Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="937d4-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="937d4-109">Inne polecenia cmdlet są potrzebne do skonfigurowania obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="937d4-110">Oto następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="937d4-110">These cmdlets are:</span></span>
- <span data-ttu-id="937d4-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="937d4-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="937d4-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="937d4-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="937d4-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="937d4-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="937d4-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="937d4-115">EXAMPLES</span></span>

### <span data-ttu-id="937d4-116">Przykład 1. Tworzenie obiektu konfiguracyjne maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="937d4-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="937d4-117">W tym przykładzie jest tworzenie obiektu konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="937d4-118">Pierwsze polecenie używa polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji maszyny WIRTUALNEJ i przechowuje wynik w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="937d4-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="937d4-119">Drugie polecenie używa polecenia cmdlet **New-AzVmss w** celu utworzenia maszyny wirtualnej, która korzysta z obiektu konfiguracji maszyny wirtualnej utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="937d4-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="937d4-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="937d4-120">Example 2</span></span>

<span data-ttu-id="937d4-121">Tworzy obiekt konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="937d4-122">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="937d4-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="937d4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="937d4-123">PARAMETERS</span></span>

### <span data-ttu-id="937d4-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="937d4-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="937d4-125">Czas, na jaki automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="937d4-126">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="937d4-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="937d4-127">Pomaga to uniknąć przypadkowej lub przypadkowej naprawy.</span><span class="sxs-lookup"><span data-stu-id="937d4-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="937d4-128">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="937d4-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="937d4-129">Minimalny dozwolony okres prolongaty to 30 minut (PT30M), co jest również wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="937d4-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="937d4-130">Maksymalny dozwolony okres prolongaty to 90 minut (PT90M).</span><span class="sxs-lookup"><span data-stu-id="937d4-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="937d4-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="937d4-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="937d4-132">Określa, czy uaktualnienia systemu operacyjnego powinny być automatycznie stosowane do skalowania wystąpień zestawu w sposób toczący się, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="937d4-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="937d4-133">— BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="937d4-133">-BootDiagnostic</span></span>
<span data-ttu-id="937d4-134">Określa profil diagnostyki rozruchu zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="937d4-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="937d4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-135">-DefaultProfile</span></span>
<span data-ttu-id="937d4-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="937d4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="937d4-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="937d4-137">-DisableAutoRollback</span></span>
<span data-ttu-id="937d4-138">Wyłączanie automatycznego wycofywania dla zasad uaktualniania systemu Auto OS</span><span class="sxs-lookup"><span data-stu-id="937d4-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="937d4-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="937d4-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="937d4-140">Włącza automatyczne naprawy na zestawie skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="937d4-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="937d4-141">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="937d4-141">-EnableUltraSSD</span></span>
<span data-ttu-id="937d4-142">Umożliwia możliwość, że jedna lub więcej zarządzanych dysków danych UltraSSD_LRS typ konta magazynu na podstawie ustawionej skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="937d4-143">Dysk zarządzany z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="937d4-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="937d4-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="937d4-144">-EncryptionAtHost</span></span>
<span data-ttu-id="937d4-145">Ten parametr umożliwia szyfrowanie dla wszystkich dysków dysków, w tym dysku zasobu/tempa na samym hoście.</span><span class="sxs-lookup"><span data-stu-id="937d4-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="937d4-146">Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="937d4-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="937d4-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="937d4-147">-EvictionPolicy</span></span>
<span data-ttu-id="937d4-148">Określa zasady wywłasowania dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="937d4-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="937d4-149">- Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="937d4-149">-Extension</span></span>
<span data-ttu-id="937d4-150">Określa obiekt informacji o rozszerzeniu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="937d4-151">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension.**</span><span class="sxs-lookup"><span data-stu-id="937d4-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="937d4-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="937d4-152">-HealthProbeId</span></span>
<span data-ttu-id="937d4-153">Określa identyfikator urządzenia do równoważenia obciążenia używany do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="937d4-154">Identyfikator HealthProbeId ma postać "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/rzys/{nazwa_pliku_pliku}".</span><span class="sxs-lookup"><span data-stu-id="937d4-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="937d4-155">- IdentityId</span><span class="sxs-lookup"><span data-stu-id="937d4-155">-IdentityId</span></span>
<span data-ttu-id="937d4-156">Określa listę tożsamości użytkowników skojarzonych z zestawem skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="937d4-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="937d4-157">Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="937d4-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="937d4-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="937d4-158">-IdentityType</span></span>
<span data-ttu-id="937d4-159">Określa typ tożsamości używany dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="937d4-160">Typ "SystemAssignedUserAssigned" zawiera zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="937d4-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="937d4-161">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="937d4-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="937d4-162">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="937d4-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="937d4-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="937d4-163">SystemAssigned</span></span>
- <span data-ttu-id="937d4-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="937d4-164">UserAssigned</span></span>
- <span data-ttu-id="937d4-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="937d4-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="937d4-166">Brak</span><span class="sxs-lookup"><span data-stu-id="937d4-166">None</span></span>

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

### <span data-ttu-id="937d4-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="937d4-167">-LicenseType</span></span>
<span data-ttu-id="937d4-168">Określ typ licencji, który umożliwia sprowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="937d4-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="937d4-169">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="937d4-169">-Location</span></span>
<span data-ttu-id="937d4-170">Określa lokalizację platformy Azure, w której jest tworzona usługa MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="937d4-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="937d4-171">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="937d4-171">-MaxPrice</span></span>
<span data-ttu-id="937d4-172">Określa maksymalną cenę, jaką zamierzasz zapłacić za maszynę wirtualnej lub maszyny wirtualnej na miejscu.</span><span class="sxs-lookup"><span data-stu-id="937d4-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="937d4-173">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="937d4-173">This price is in US Dollars.</span></span> <span data-ttu-id="937d4-174">Ta cena będzie porównywana z bieżącą ceną spotową rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="937d4-175">Ponadto ceny są porównywane w czasie tworzenia/aktualizowania maszyny wirtualnej na miejscu/maszyny wirtualnej, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż bieżąca cena bieżąca.</span><span class="sxs-lookup"><span data-stu-id="937d4-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="937d4-176">Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej na miejscu, jeśli bieżąca cena spot wykracza poza wartość maxPrice po utworzeniu maszyny wirtualnej/maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="937d4-177">Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="937d4-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="937d4-178">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="937d4-178">Example: 0.01538.</span></span>  <span data-ttu-id="937d4-179">-1 wskazuje, że maszyny wirtualnej/maszyny wirtualnej na miejscu nie należy owijać ze względu na cenę.</span><span class="sxs-lookup"><span data-stu-id="937d4-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="937d4-180">Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.</span><span class="sxs-lookup"><span data-stu-id="937d4-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="937d4-181">- NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="937d4-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="937d4-182">Określa obiekt profilu sieciowego zawierający właściwości sieci dla konfiguracji usług VMSS.</span><span class="sxs-lookup"><span data-stu-id="937d4-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="937d4-183">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="937d4-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="937d4-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-184">-OsProfile</span></span>
<span data-ttu-id="937d4-185">Określa obiekt profilu systemu operacyjnego zawierający właściwości systemu operacyjnego dla konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="937d4-186">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile.**</span><span class="sxs-lookup"><span data-stu-id="937d4-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="937d4-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="937d4-187">-Overprovision</span></span>
<span data-ttu-id="937d4-188">Wskazuje, czy polecenie cmdlet overprovisions the VMSS.</span><span class="sxs-lookup"><span data-stu-id="937d4-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="937d4-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="937d4-189">-PlanName</span></span>
<span data-ttu-id="937d4-190">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="937d4-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="937d4-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="937d4-191">-PlanProduct</span></span>
<span data-ttu-id="937d4-192">Określa produkt planu.</span><span class="sxs-lookup"><span data-stu-id="937d4-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="937d4-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="937d4-193">-PlanPromotionCode</span></span>
<span data-ttu-id="937d4-194">Określa kod promocyjny planu.</span><span class="sxs-lookup"><span data-stu-id="937d4-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="937d4-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="937d4-195">-PlanPublisher</span></span>
<span data-ttu-id="937d4-196">Określa wydawcę planu.</span><span class="sxs-lookup"><span data-stu-id="937d4-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="937d4-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="937d4-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="937d4-198">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="937d4-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="937d4-199">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="937d4-199">-Priority</span></span>
<span data-ttu-id="937d4-200">Priorytet wirtualnego machien w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="937d4-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="937d4-201">Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".</span><span class="sxs-lookup"><span data-stu-id="937d4-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="937d4-202">"Zwykła" jest dla zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="937d4-203">"Spot" jest dla maszyny wirtualnej spot.</span><span class="sxs-lookup"><span data-stu-id="937d4-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="937d4-204">"Low" jest również dla spot virtual machine, ale jest zastępowany przez "Spot".</span><span class="sxs-lookup"><span data-stu-id="937d4-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="937d4-205">Użyj pozycji Spot (Spot) zamiast "Low" (Najniszej).</span><span class="sxs-lookup"><span data-stu-id="937d4-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="937d4-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="937d4-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="937d4-207">Identyfikator zasobu grupy Położenie odległości, który ma być ustawiony dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="937d4-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="937d4-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="937d4-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="937d4-209">Określa zasady uaktualniania przy wycofywaniu.</span><span class="sxs-lookup"><span data-stu-id="937d4-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="937d4-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="937d4-210">-ScaleInPolicy</span></span>
<span data-ttu-id="937d4-211">Reguły, które mają być stosowane podczas skalowania w zestawie skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="937d4-212">Dopuszczalne wartości to: "Domyślne", "NajstarszeVM" i "NajnowszeVM".</span><span class="sxs-lookup"><span data-stu-id="937d4-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="937d4-213">Ustawienie "Domyślne", gdy skala zestawu maszyn wirtualnych jest skalowana w, zestaw skali zostanie najpierw wyrównany w różnych strefach, jeśli jest to zestaw skali zonal.</span><span class="sxs-lookup"><span data-stu-id="937d4-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="937d4-214">Następnie zostanie on w możliwie najdalej sytą równowagi między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="937d4-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="937d4-215">W obrębie każdej domeny błędu maszyny wirtualne wybrane do usunięcia będą najnowszymi, które nie są chronione przez skalowanie.</span><span class="sxs-lookup"><span data-stu-id="937d4-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="937d4-216">Podczas skalowania zestawu skalowania dla maszyny wirtualnej najstarsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="937d4-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="937d4-217">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="937d4-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="937d4-218">W każdej strefie najstarsze komputery wirtualne, które nie są chronione, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="937d4-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="937d4-219">W przypadku skalowania zestawu skalowania do najnowszej maszyny wirtualnej, która nie jest chroniona skalą, do usunięcia zostanie wybrana najnowsza wersja maszyn wirtualnych, które nie są chronione przez skalowanie.</span><span class="sxs-lookup"><span data-stu-id="937d4-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="937d4-220">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="937d4-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="937d4-221">W każdej strefie do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="937d4-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="937d4-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="937d4-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="937d4-223">Określa pojedynczą grupę położenia.</span><span class="sxs-lookup"><span data-stu-id="937d4-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="937d4-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="937d4-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="937d4-225">Określa, że rozszerzenia nie są uruchamiane na dodatkowych nadprowizowanych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="937d4-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="937d4-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="937d4-226">-SkuCapacity</span></span>
<span data-ttu-id="937d4-227">Określa liczbę wystąpień w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="937d4-228">-SKUName</span><span class="sxs-lookup"><span data-stu-id="937d4-228">-SkuName</span></span>
<span data-ttu-id="937d4-229">Określa rozmiar wszystkich wystąpień maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="937d4-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="937d4-230">-SkuTier</span></span>
<span data-ttu-id="937d4-231">Określa warstwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="937d4-232">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="937d4-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="937d4-233">Standardowe</span><span class="sxs-lookup"><span data-stu-id="937d4-233">Standard</span></span>
- <span data-ttu-id="937d4-234">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="937d4-234">Basic</span></span>

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

### <span data-ttu-id="937d4-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-235">-StorageProfile</span></span>
<span data-ttu-id="937d4-236">Określa obiekt profilu magazynu zawierający właściwości dysku dla konfiguracji usług VMSS.</span><span class="sxs-lookup"><span data-stu-id="937d4-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="937d4-237">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile.**</span><span class="sxs-lookup"><span data-stu-id="937d4-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="937d4-238">— Tag</span><span class="sxs-lookup"><span data-stu-id="937d4-238">-Tag</span></span>
<span data-ttu-id="937d4-239">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="937d4-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="937d4-240">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="937d4-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="937d4-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="937d4-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="937d4-242">Konfigurowany czas (w minutach) usunięcie maszyny wirtualnej będzie musiało potencjalnie zatwierdzić zdarzenie Zakończ zaplanowane przed automatycznym zatwierdzeniem zdarzenia (przeocz przekreślony czas).</span><span class="sxs-lookup"><span data-stu-id="937d4-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="937d4-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="937d4-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="937d4-244">Włączanie zdarzenia Zakończ zaplanowane</span><span class="sxs-lookup"><span data-stu-id="937d4-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="937d4-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="937d4-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="937d4-246">Określono tryb uaktualniania do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="937d4-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="937d4-247">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="937d4-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="937d4-248">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="937d4-248">Automatic</span></span>
- <span data-ttu-id="937d4-249">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="937d4-249">Manual</span></span>

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

### <span data-ttu-id="937d4-250">— Strefa</span><span class="sxs-lookup"><span data-stu-id="937d4-250">-Zone</span></span>
<span data-ttu-id="937d4-251">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="937d4-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="937d4-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="937d4-252">-ZoneBalance</span></span>
<span data-ttu-id="937d4-253">Czy należy wymusić ściśle nawet dystrybucję maszyny wirtualnej między strefami x w przypadku 30-dniowej 35-dniowej siły.</span><span class="sxs-lookup"><span data-stu-id="937d4-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="937d4-254">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="937d4-254">-Confirm</span></span>
<span data-ttu-id="937d4-255">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="937d4-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937d4-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937d4-256">-WhatIf</span></span>
<span data-ttu-id="937d4-257">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="937d4-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="937d4-258">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="937d4-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937d4-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937d4-259">CommonParameters</span></span>
<span data-ttu-id="937d4-260">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937d4-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937d4-261">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="937d4-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937d4-262">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="937d4-262">INPUTS</span></span>

### <span data-ttu-id="937d4-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="937d4-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="937d4-264">System.String</span><span class="sxs-lookup"><span data-stu-id="937d4-264">System.String</span></span>

### <span data-ttu-id="937d4-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="937d4-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="937d4-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="937d4-266">System.Int32</span></span>

### <span data-ttu-id="937d4-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="937d4-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="937d4-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="937d4-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="937d4-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="937d4-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="937d4-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="937d4-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="937d4-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="937d4-272">System.String[]</span></span>

### <span data-ttu-id="937d4-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="937d4-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="937d4-274">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="937d4-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="937d4-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="937d4-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="937d4-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="937d4-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="937d4-277">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="937d4-277">OUTPUTS</span></span>

### <span data-ttu-id="937d4-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="937d4-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="937d4-279">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="937d4-279">NOTES</span></span>

## <span data-ttu-id="937d4-280">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="937d4-280">RELATED LINKS</span></span>

[<span data-ttu-id="937d4-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="937d4-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="937d4-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="937d4-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="937d4-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="937d4-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="937d4-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="937d4-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="937d4-285">New-AzVmss</span></span>](./New-AzVmss.md)
