---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710265"
---
# <span data-ttu-id="22047-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="22047-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="22047-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22047-102">SYNOPSIS</span></span>
<span data-ttu-id="22047-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="22047-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22047-104">SYNTAX</span></span>

### <span data-ttu-id="22047-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22047-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22047-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="22047-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22047-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="22047-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22047-108">Opis</span><span class="sxs-lookup"><span data-stu-id="22047-108">DESCRIPTION</span></span>
<span data-ttu-id="22047-109">Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="22047-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="22047-110">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22047-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="22047-111">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="22047-111">These cmdlets are:</span></span>
- <span data-ttu-id="22047-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="22047-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="22047-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="22047-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="22047-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="22047-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="22047-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="22047-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="22047-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22047-116">EXAMPLES</span></span>

### <span data-ttu-id="22047-117">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="22047-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="22047-118">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="22047-119">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="22047-120">W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="22047-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="22047-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22047-121">PARAMETERS</span></span>

### <span data-ttu-id="22047-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="22047-122">-AssignIdentity</span></span>
<span data-ttu-id="22047-123">Określ tożsamość przypisanego systemu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="22047-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="22047-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="22047-125">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="22047-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="22047-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="22047-126">-BootDiagnostic</span></span>
<span data-ttu-id="22047-127">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="22047-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="22047-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22047-128">-DefaultProfile</span></span>
<span data-ttu-id="22047-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22047-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22047-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="22047-130">-DisableAutoRollback</span></span>
<span data-ttu-id="22047-131">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="22047-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="22047-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="22047-132">-EnableUltraSSD</span></span>
<span data-ttu-id="22047-133">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="22047-134">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="22047-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="22047-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="22047-135">-EvictionPolicy</span></span>
<span data-ttu-id="22047-136">Określa zasady wykluczania dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="22047-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="22047-137">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="22047-137">-Extension</span></span>
<span data-ttu-id="22047-138">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="22047-139">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="22047-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22047-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="22047-140">-HealthProbeId</span></span>
<span data-ttu-id="22047-141">Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="22047-142">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="22047-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="22047-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="22047-143">-IdentityId</span></span>
<span data-ttu-id="22047-144">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="22047-145">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="22047-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="22047-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="22047-146">-IdentityType</span></span>
<span data-ttu-id="22047-147">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="22047-148">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="22047-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="22047-149">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="22047-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="22047-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22047-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="22047-151">SystemAssigned</span></span>
- <span data-ttu-id="22047-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="22047-152">UserAssigned</span></span>
- <span data-ttu-id="22047-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="22047-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="22047-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="22047-154">None</span></span>

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

### <span data-ttu-id="22047-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="22047-155">-LicenseType</span></span>
<span data-ttu-id="22047-156">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="22047-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="22047-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22047-157">-Location</span></span>
<span data-ttu-id="22047-158">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="22047-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="22047-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="22047-160">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="22047-161">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="22047-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="22047-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="22047-162">-OsProfile</span></span>
<span data-ttu-id="22047-163">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="22047-164">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="22047-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="22047-165">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="22047-165">-Overprovision</span></span>
<span data-ttu-id="22047-166">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="22047-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="22047-167">-PlanName</span></span>
<span data-ttu-id="22047-168">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="22047-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="22047-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="22047-169">-PlanProduct</span></span>
<span data-ttu-id="22047-170">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="22047-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="22047-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="22047-171">-PlanPromotionCode</span></span>
<span data-ttu-id="22047-172">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="22047-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="22047-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="22047-173">-PlanPublisher</span></span>
<span data-ttu-id="22047-174">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="22047-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="22047-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="22047-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="22047-176">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="22047-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="22047-177">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="22047-177">-Priority</span></span>
<span data-ttu-id="22047-178">Określa priorytet maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="22047-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="22047-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="22047-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="22047-180">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="22047-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="22047-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="22047-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="22047-182">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="22047-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="22047-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="22047-183">-SkuCapacity</span></span>
<span data-ttu-id="22047-184">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="22047-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="22047-185">-SkuName</span></span>
<span data-ttu-id="22047-186">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="22047-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="22047-187">-SkuTier</span></span>
<span data-ttu-id="22047-188">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="22047-189">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="22047-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22047-190">Standard</span><span class="sxs-lookup"><span data-stu-id="22047-190">Standard</span></span>
- <span data-ttu-id="22047-191">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="22047-191">Basic</span></span>

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

### <span data-ttu-id="22047-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="22047-192">-StorageProfile</span></span>
<span data-ttu-id="22047-193">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="22047-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="22047-194">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="22047-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="22047-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="22047-195">-Tag</span></span>
<span data-ttu-id="22047-196">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="22047-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22047-197">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="22047-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22047-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="22047-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="22047-199">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="22047-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="22047-200">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="22047-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22047-201">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="22047-201">Automatic</span></span>
- <span data-ttu-id="22047-202">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="22047-202">Manual</span></span>

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

### <span data-ttu-id="22047-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="22047-203">-Zone</span></span>
<span data-ttu-id="22047-204">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22047-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="22047-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="22047-205">-ZoneBalance</span></span>
<span data-ttu-id="22047-206">Czy należy wymusić ścisłe, nawet strefy krzyżowe funkcji dystrybucji maszyn wirtualnych na wypadek awarii strefy.</span><span class="sxs-lookup"><span data-stu-id="22047-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="22047-207">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22047-207">-Confirm</span></span>
<span data-ttu-id="22047-208">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22047-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22047-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22047-209">-WhatIf</span></span>
<span data-ttu-id="22047-210">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22047-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22047-211">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22047-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22047-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22047-212">CommonParameters</span></span>
<span data-ttu-id="22047-213">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22047-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22047-214">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22047-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22047-215">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22047-215">INPUTS</span></span>

### <span data-ttu-id="22047-216">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22047-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="22047-217">System. String</span><span class="sxs-lookup"><span data-stu-id="22047-217">System.String</span></span>

### <span data-ttu-id="22047-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22047-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="22047-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="22047-219">System.Int32</span></span>

### <span data-ttu-id="22047-220">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. MODELES. Upgrademode; Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="22047-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="22047-221">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="22047-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="22047-222">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="22047-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="22047-223">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="22047-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="22047-224">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="22047-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="22047-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="22047-225">System.String[]</span></span>

### <span data-ttu-id="22047-226">Microsoft. Azure. Management. COMPUTE. MODELES. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="22047-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="22047-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22047-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="22047-228">Microsoft. Azure. Management. COMPUTE. MODELES. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="22047-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="22047-229">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ResourceIdentityType, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="22047-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="22047-230">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22047-230">OUTPUTS</span></span>

### <span data-ttu-id="22047-231">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22047-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="22047-232">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22047-232">NOTES</span></span>

## <span data-ttu-id="22047-233">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22047-233">RELATED LINKS</span></span>

[<span data-ttu-id="22047-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="22047-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="22047-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="22047-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="22047-236">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="22047-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="22047-237">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="22047-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="22047-238">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="22047-238">New-AzVmss</span></span>](./New-AzVmss.md)
