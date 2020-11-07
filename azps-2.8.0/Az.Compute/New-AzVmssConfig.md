---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: e65bfa607f9689a85f7734b1913bbabadd4dd115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706313"
---
# <span data-ttu-id="74311-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="74311-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="74311-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74311-102">SYNOPSIS</span></span>
<span data-ttu-id="74311-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="74311-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74311-104">SYNTAX</span></span>

### <span data-ttu-id="74311-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74311-105">DefaultParameterSet (Default)</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74311-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="74311-106">ExplicitIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74311-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="74311-107">AssignIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74311-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74311-108">DESCRIPTION</span></span>
<span data-ttu-id="74311-109">Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="74311-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="74311-110">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74311-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="74311-111">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="74311-111">These cmdlets are:</span></span>
- <span data-ttu-id="74311-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="74311-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="74311-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="74311-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="74311-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="74311-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="74311-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="74311-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="74311-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74311-116">EXAMPLES</span></span>

### <span data-ttu-id="74311-117">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="74311-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="74311-118">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="74311-119">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="74311-120">W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="74311-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="74311-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74311-121">PARAMETERS</span></span>

### <span data-ttu-id="74311-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="74311-122">-AssignIdentity</span></span>
<span data-ttu-id="74311-123">Określ tożsamość przypisanego systemu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="74311-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="74311-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="74311-125">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="74311-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="74311-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="74311-126">-BootDiagnostic</span></span>
<span data-ttu-id="74311-127">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="74311-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="74311-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74311-128">-DefaultProfile</span></span>
<span data-ttu-id="74311-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74311-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74311-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="74311-130">-DisableAutoRollback</span></span>
<span data-ttu-id="74311-131">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="74311-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="74311-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="74311-132">-EnableUltraSSD</span></span>
<span data-ttu-id="74311-133">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="74311-134">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="74311-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="74311-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="74311-135">-EvictionPolicy</span></span>
<span data-ttu-id="74311-136">Określa zasady wykluczania dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="74311-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="74311-137">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="74311-137">-Extension</span></span>
<span data-ttu-id="74311-138">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="74311-139">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="74311-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="74311-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="74311-140">-HealthProbeId</span></span>
<span data-ttu-id="74311-141">Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="74311-142">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="74311-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="74311-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="74311-143">-IdentityId</span></span>
<span data-ttu-id="74311-144">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="74311-145">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="74311-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="74311-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="74311-146">-IdentityType</span></span>
<span data-ttu-id="74311-147">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="74311-148">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74311-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="74311-149">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="74311-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74311-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74311-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="74311-151">SystemAssigned</span></span>
- <span data-ttu-id="74311-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="74311-152">UserAssigned</span></span>
- <span data-ttu-id="74311-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="74311-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="74311-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="74311-154">None</span></span>

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

### <span data-ttu-id="74311-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="74311-155">-LicenseType</span></span>
<span data-ttu-id="74311-156">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="74311-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="74311-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74311-157">-Location</span></span>
<span data-ttu-id="74311-158">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="74311-159">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="74311-159">-MaxPrice</span></span>
<span data-ttu-id="74311-160">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-160">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="74311-161">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="74311-161">This price is in US Dollars.</span></span> <span data-ttu-id="74311-162">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-162">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="74311-163">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="74311-163">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="74311-164">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-164">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="74311-165">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="74311-165">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="74311-166">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="74311-166">Example: 0.01538.</span></span>  <span data-ttu-id="74311-167">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="74311-167">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="74311-168">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="74311-168">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="74311-169">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="74311-169">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="74311-170">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-170">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="74311-171">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="74311-171">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="74311-172">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="74311-172">-OsProfile</span></span>
<span data-ttu-id="74311-173">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-173">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="74311-174">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="74311-174">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="74311-175">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="74311-175">-Overprovision</span></span>
<span data-ttu-id="74311-176">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-176">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="74311-177">-PlanName</span><span class="sxs-lookup"><span data-stu-id="74311-177">-PlanName</span></span>
<span data-ttu-id="74311-178">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="74311-178">Specifies the plan name.</span></span>

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

### <span data-ttu-id="74311-179">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="74311-179">-PlanProduct</span></span>
<span data-ttu-id="74311-180">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="74311-180">Specifies the plan product.</span></span>

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

### <span data-ttu-id="74311-181">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="74311-181">-PlanPromotionCode</span></span>
<span data-ttu-id="74311-182">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="74311-182">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="74311-183">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="74311-183">-PlanPublisher</span></span>
<span data-ttu-id="74311-184">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="74311-184">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="74311-185">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="74311-185">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="74311-186">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="74311-186">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="74311-187">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="74311-187">-Priority</span></span>
<span data-ttu-id="74311-188">Określa priorytet maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="74311-188">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="74311-189">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="74311-189">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="74311-190">Identyfikator ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="74311-190">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="74311-191">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="74311-191">-RollingUpgradePolicy</span></span>
<span data-ttu-id="74311-192">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="74311-192">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="74311-193">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="74311-193">-SinglePlacementGroup</span></span>
<span data-ttu-id="74311-194">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="74311-194">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="74311-195">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="74311-195">-SkuCapacity</span></span>
<span data-ttu-id="74311-196">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-196">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="74311-197">-SkuName</span><span class="sxs-lookup"><span data-stu-id="74311-197">-SkuName</span></span>
<span data-ttu-id="74311-198">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-198">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="74311-199">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="74311-199">-SkuTier</span></span>
<span data-ttu-id="74311-200">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-200">Specifies the tier of VMSS.</span></span> <span data-ttu-id="74311-201">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74311-201">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74311-202">Standard</span><span class="sxs-lookup"><span data-stu-id="74311-202">Standard</span></span>
- <span data-ttu-id="74311-203">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="74311-203">Basic</span></span>

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

### <span data-ttu-id="74311-204">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="74311-204">-StorageProfile</span></span>
<span data-ttu-id="74311-205">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="74311-205">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="74311-206">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="74311-206">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="74311-207">-Tag</span><span class="sxs-lookup"><span data-stu-id="74311-207">-Tag</span></span>
<span data-ttu-id="74311-208">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="74311-208">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74311-209">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="74311-209">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="74311-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="74311-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="74311-211">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="74311-211">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="74311-212">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="74311-212">-TerminateScheduledEvents</span></span>
<span data-ttu-id="74311-213">Włączanie kończenia zaplanowanych zdarzeń</span><span class="sxs-lookup"><span data-stu-id="74311-213">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="74311-214">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="74311-214">-UpgradePolicyMode</span></span>
<span data-ttu-id="74311-215">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="74311-215">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="74311-216">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74311-216">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74311-217">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="74311-217">Automatic</span></span>
- <span data-ttu-id="74311-218">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="74311-218">Manual</span></span>

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

### <span data-ttu-id="74311-219">-Zone</span><span class="sxs-lookup"><span data-stu-id="74311-219">-Zone</span></span>
<span data-ttu-id="74311-220">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74311-220">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="74311-221">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="74311-221">-ZoneBalance</span></span>
<span data-ttu-id="74311-222">Czy należy wymusić ścisłe, nawet strefy krzyżowe funkcji dystrybucji maszyn wirtualnych na wypadek awarii strefy.</span><span class="sxs-lookup"><span data-stu-id="74311-222">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="74311-223">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74311-223">-Confirm</span></span>
<span data-ttu-id="74311-224">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74311-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74311-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74311-225">-WhatIf</span></span>
<span data-ttu-id="74311-226">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74311-226">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74311-227">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74311-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74311-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74311-228">CommonParameters</span></span>
<span data-ttu-id="74311-229">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74311-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74311-230">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74311-230">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74311-231">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74311-231">INPUTS</span></span>

### <span data-ttu-id="74311-232">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74311-232">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74311-233">System. String</span><span class="sxs-lookup"><span data-stu-id="74311-233">System.String</span></span>

### <span data-ttu-id="74311-234">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="74311-234">System.Collections.Hashtable</span></span>

### <span data-ttu-id="74311-235">System. Int32</span><span class="sxs-lookup"><span data-stu-id="74311-235">System.Int32</span></span>

### <span data-ttu-id="74311-236">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. MODELES. Upgrademode; Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="74311-236">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="74311-237">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="74311-237">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="74311-238">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="74311-238">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="74311-239">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="74311-239">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="74311-240">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="74311-240">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="74311-241">System. String []</span><span class="sxs-lookup"><span data-stu-id="74311-241">System.String[]</span></span>

### <span data-ttu-id="74311-242">Microsoft. Azure. Management. COMPUTE. MODELES. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="74311-242">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="74311-243">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74311-243">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="74311-244">Microsoft. Azure. Management. COMPUTE. MODELES. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="74311-244">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="74311-245">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ResourceIdentityType, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="74311-245">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="74311-246">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74311-246">OUTPUTS</span></span>

### <span data-ttu-id="74311-247">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="74311-247">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="74311-248">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74311-248">NOTES</span></span>

## <span data-ttu-id="74311-249">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74311-249">RELATED LINKS</span></span>

[<span data-ttu-id="74311-250">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="74311-250">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="74311-251">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="74311-251">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="74311-252">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="74311-252">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="74311-253">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="74311-253">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="74311-254">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="74311-254">New-AzVmss</span></span>](./New-AzVmss.md)
