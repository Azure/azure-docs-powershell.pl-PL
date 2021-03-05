---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015393"
---
# <span data-ttu-id="0b097-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-101">Update-AzVmss</span></span>

## <span data-ttu-id="0b097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b097-102">SYNOPSIS</span></span>
<span data-ttu-id="0b097-103">Aktualizuje stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="0b097-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b097-104">SYNTAX</span></span>

### <span data-ttu-id="0b097-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b097-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b097-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b097-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b097-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b097-107">DESCRIPTION</span></span>
<span data-ttu-id="0b097-108">Polecenie **cmdlet Update-AzVmss** aktualizuje stan zestawu skal maszyny wirtualnej do stanu lokalnego obiektu MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="0b097-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="0b097-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b097-109">EXAMPLES</span></span>

### <span data-ttu-id="0b097-110">Przykład 1. Aktualizowanie stanu maszyn wirtualnych do stanu lokalnego obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="0b097-111">To polecenie aktualizuje stan maszyny wirtualnej o nazwie VMSS001, która należy do grupy zasobów o nazwie Group001, do stanu lokalnego obiektu MASZYNY.WIRTUALNE, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="0b097-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="0b097-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b097-112">PARAMETERS</span></span>

### <span data-ttu-id="0b097-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0b097-113">-AsJob</span></span>
<span data-ttu-id="0b097-114">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0b097-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0b097-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0b097-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="0b097-116">Określa, czy uaktualnienia systemu operacyjnego powinny być automatycznie stosowane do skalowania wystąpień zestawu w sposób toczący się, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="0b097-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="0b097-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="0b097-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="0b097-118">Czas, na jaki automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="0b097-119">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="0b097-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="0b097-120">Pomaga to uniknąć przypadkowej lub przypadkowej naprawy.</span><span class="sxs-lookup"><span data-stu-id="0b097-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="0b097-121">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="0b097-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="0b097-122">Minimalny dozwolony okres prolongaty to 30 minut (PT30M), co jest również wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="0b097-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="0b097-123">Maksymalny dozwolony okres prolongaty to 90 minut (PT90M).</span><span class="sxs-lookup"><span data-stu-id="0b097-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="0b097-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="0b097-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="0b097-125">Czy diagnostyka rozruchu powinna być włączona na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0b097-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="0b097-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="0b097-127">URI konta magazynu, które ma być służące do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="0b097-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="0b097-128">- CustomData</span><span class="sxs-lookup"><span data-stu-id="0b097-128">-CustomData</span></span>
<span data-ttu-id="0b097-129">Określa zakodowany ciąg danych niestandardowych o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="0b097-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="0b097-130">Jest on dekodowany do tablicy binarnej zapisanej jako plik na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="0b097-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="0b097-131">Maksymalna długość tablicy binarnej to 65 535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="0b097-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="0b097-132">Aby uzyskać informacje na temat korzystania z init w chmurze dla maszyny wirtualnej, zobacz Dostosowywanie maszyny wirtualnej systemu Linux podczas tworzenia za pomocą [init w chmurze.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="0b097-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="0b097-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b097-133">-DefaultProfile</span></span>
<span data-ttu-id="0b097-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b097-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b097-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="0b097-135">-DisableAutoRollback</span></span>
<span data-ttu-id="0b097-136">Wyłączanie automatycznego wycofywania dla zasad uaktualniania systemu Auto OS</span><span class="sxs-lookup"><span data-stu-id="0b097-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="0b097-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="0b097-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="0b097-138">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasłem systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="0b097-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="0b097-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="0b097-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="0b097-140">Włączanie lub wyłączanie napraw automatycznych w zestawie skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0b097-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0b097-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="0b097-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="0b097-142">Wskazuje, czy maszyny wirtualne systemu Windows w usługach VIRTUALSS są włączone dla aktualizacji automatycznych.</span><span class="sxs-lookup"><span data-stu-id="0b097-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="0b097-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="0b097-143">-EncryptionAtHost</span></span>
<span data-ttu-id="0b097-144">Ten parametr może być używany przez użytkownika w żądaniu w celu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="0b097-145">- IdentityId</span><span class="sxs-lookup"><span data-stu-id="0b097-145">-IdentityId</span></span>
<span data-ttu-id="0b097-146">Określa listę tożsamości użytkowników skojarzonych z zestawem skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0b097-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="0b097-147">Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="0b097-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0b097-148">-IdentityType</span></span>
<span data-ttu-id="0b097-149">Określa typ tożsamości używany dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="0b097-150">Typ "SystemAssignedUserAssigned" zawiera zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0b097-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="0b097-151">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0b097-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="0b097-152">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b097-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b097-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0b097-153">SystemAssigned</span></span>
- <span data-ttu-id="0b097-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="0b097-154">UserAssigned</span></span>
- <span data-ttu-id="0b097-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="0b097-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="0b097-156">Brak</span><span class="sxs-lookup"><span data-stu-id="0b097-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="0b097-157">-ImageReferenceId</span></span>
<span data-ttu-id="0b097-158">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="0b097-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="0b097-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="0b097-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="0b097-160">Określa typ oferty obrazu maszyny wirtualnej (VIRTUALImage).</span><span class="sxs-lookup"><span data-stu-id="0b097-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="0b097-161">Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="0b097-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="0b097-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="0b097-163">Określa nazwę wydawcy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0b097-164">Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0b097-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="0b097-165">-ImageReferenceSku</span></span>
<span data-ttu-id="0b097-166">Określa wartość SKU MASZYNY.WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="0b097-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="0b097-167">Aby uzyskać jednostki SKU, użyj Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="0b097-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="0b097-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="0b097-169">Określa wersję programu VMImage.</span><span class="sxs-lookup"><span data-stu-id="0b097-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="0b097-170">Aby użyć najnowszej wersji, określ wartość najnowszej zamiast określonej wersji.</span><span class="sxs-lookup"><span data-stu-id="0b097-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="0b097-171">- ImageUri</span><span class="sxs-lookup"><span data-stu-id="0b097-171">-ImageUri</span></span>
<span data-ttu-id="0b097-172">Określa identyfikator URI obiektu blob dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0b097-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="0b097-173">Narzędzie VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0b097-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="0b097-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0b097-174">-LicenseType</span></span>
<span data-ttu-id="0b097-175">Określ typ licencji, który umożliwia sprowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="0b097-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="0b097-176">-Managed JakAstorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0b097-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="0b097-177">Określa typ konta magazynu dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0b097-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="0b097-178">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b097-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b097-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="0b097-179">StandardLRS</span></span>
- <span data-ttu-id="0b097-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="0b097-180">PremiumLRS</span></span>

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

### <span data-ttu-id="0b097-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0b097-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="0b097-182">Maksymalny procent całkowitej liczby wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnianie w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="0b097-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="0b097-183">Ponieważ jest to maksymalna liczba wystąpień w poprzednich lub przyszłych partiach o złej kondycji, może spowodować zmniejszenie procentu wystąpień w partii w celu zapewnienia większej niezawodności.</span><span class="sxs-lookup"><span data-stu-id="0b097-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="0b097-184">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="0b097-184">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-185">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="0b097-185">-MaxPrice</span></span>
<span data-ttu-id="0b097-186">Określa maksymalną cenę za niską płatność za maszyny wirtualne/maszyny wirtualne o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="0b097-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="0b097-187">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="0b097-187">This price is in US Dollars.</span></span> <span data-ttu-id="0b097-188">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="0b097-189">Ponadto ceny są porównywane w czasie tworzenia/aktualizacji maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż obecna cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="0b097-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="0b097-190">Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, jeśli bieżąca cena o niskim priorytecie przekracza wartość maxCena po utworzeniu maszyny wirtualnej/maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="0b097-191">Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="0b097-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="0b097-192">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="0b097-192">Example: 0.01538.</span></span>  <span data-ttu-id="0b097-193">-1 oznacza, że maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie nie należy ich ujednać ze względu na cenę.</span><span class="sxs-lookup"><span data-stu-id="0b097-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="0b097-194">Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.</span><span class="sxs-lookup"><span data-stu-id="0b097-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0b097-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="0b097-196">Maksymalna wartość procentowa całkowitej liczby wystąpień maszyn wirtualnych w zestawie skali, które mogą być jednocześnie w złej kondycji w wyniku uaktualnienia lub w wyniku wystąpienia w stanie złej kondycji przez testy kondycji maszyn wirtualnych przed kropkami uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="0b097-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="0b097-197">To ograniczenie będzie sprawdzane przed uruchomieniem dowolnej partii.</span><span class="sxs-lookup"><span data-stu-id="0b097-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="0b097-198">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="0b097-198">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="0b097-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="0b097-200">Maksymalna wartość procentowa uaktualnionych wystąpień maszyn wirtualnych, które mogą być w stanie o złej kondycji.</span><span class="sxs-lookup"><span data-stu-id="0b097-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="0b097-201">Ten sprawdzanie będzie się odbywać po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="0b097-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="0b097-202">Jeśli wartość procentowa będzie kiedykolwiek przekroczona, czas aktualizacji jest przerywany.</span><span class="sxs-lookup"><span data-stu-id="0b097-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="0b097-203">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="0b097-203">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-204">-OsDriveCaching</span><span class="sxs-lookup"><span data-stu-id="0b097-204">-OsDiskCaching</span></span>
<span data-ttu-id="0b097-205">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b097-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="0b097-206">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b097-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b097-207">Brak</span><span class="sxs-lookup"><span data-stu-id="0b097-207">None</span></span>
- <span data-ttu-id="0b097-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0b097-208">ReadOnly</span></span>
- <span data-ttu-id="0b097-209">ReadWrite Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0b097-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0b097-210">Jeśli zmienisz wartość buforowania, polecenie cmdlet uruchomi ponownie maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="0b097-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="0b097-211">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="0b097-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-212">-Os JednakowyAccelerator</span><span class="sxs-lookup"><span data-stu-id="0b097-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="0b097-213">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0b097-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="0b097-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="0b097-214">-Overprovision</span></span>
<span data-ttu-id="0b097-215">Wskazuje, czy polecenie cmdlet overprovisions the VMSS.</span><span class="sxs-lookup"><span data-stu-id="0b097-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="0b097-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="0b097-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="0b097-217">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii a rozpoczęciem następnej partii.</span><span class="sxs-lookup"><span data-stu-id="0b097-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="0b097-218">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="0b097-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="0b097-219">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="0b097-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="0b097-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0b097-220">-PlanName</span></span>
<span data-ttu-id="0b097-221">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="0b097-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="0b097-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="0b097-222">-PlanProduct</span></span>
<span data-ttu-id="0b097-223">Określa produkt planu.</span><span class="sxs-lookup"><span data-stu-id="0b097-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="0b097-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="0b097-224">-PlanPromotionCode</span></span>
<span data-ttu-id="0b097-225">Określa kod promocyjny planu.</span><span class="sxs-lookup"><span data-stu-id="0b097-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="0b097-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="0b097-226">-PlanPublisher</span></span>
<span data-ttu-id="0b097-227">Określa wydawcę planu.</span><span class="sxs-lookup"><span data-stu-id="0b097-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="0b097-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="0b097-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="0b097-229">Wskazuje, czy agent maszyny wirtualnej powinien mieć inicjowanie obsługi administracyjnej na komputerach wirtualnych systemu Windows w systemie VIRTUALSS.</span><span class="sxs-lookup"><span data-stu-id="0b097-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="0b097-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="0b097-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="0b097-231">Identyfikator zasobu grupy Położenie odległości, który ma być ustawiony dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="0b097-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="0b097-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b097-232">-ResourceGroupName</span></span>
<span data-ttu-id="0b097-233">Określa nazwę grupy zasobów, do której należy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="0b097-234">-ScaleInPolicy</span></span>
<span data-ttu-id="0b097-235">Reguły, które mają być stosowane podczas skalowania w zestawie skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="0b097-236">Dopuszczalne wartości to: "Domyślne", "NajstarszeVM" i "NajnowszeVM".</span><span class="sxs-lookup"><span data-stu-id="0b097-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="0b097-237">Ustawienie "Domyślne", gdy skala zestawu maszyn wirtualnych jest skalowana w, zestaw skali zostanie najpierw wyrównany w różnych strefach, jeśli jest to zestaw skali zonal.</span><span class="sxs-lookup"><span data-stu-id="0b097-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="0b097-238">Następnie zostanie on w możliwie najdalej sytą równowagi między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="0b097-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="0b097-239">W obrębie każdej domeny błędu maszyny wirtualne wybrane do usunięcia będą najnowszymi, które nie są chronione przez skalowanie.</span><span class="sxs-lookup"><span data-stu-id="0b097-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="0b097-240">Podczas skalowania zestawu skalowania dla maszyny wirtualnej najstarsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0b097-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="0b097-241">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="0b097-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="0b097-242">W każdej strefie najstarsze komputery wirtualne, które nie są chronione, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0b097-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="0b097-243">W przypadku skalowania zestawu skalowania do najnowszej maszyny wirtualnej, która nie jest chroniona skalą, do usunięcia zostanie wybrana najnowsza wersja maszyn wirtualnych, które nie są chronione przez skalowanie.</span><span class="sxs-lookup"><span data-stu-id="0b097-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="0b097-244">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="0b097-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="0b097-245">W każdej strefie do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="0b097-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0b097-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="0b097-247">Określa pojedynczą grupę położenia.</span><span class="sxs-lookup"><span data-stu-id="0b097-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="0b097-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="0b097-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="0b097-249">Określa, że rozszerzenia nie są uruchamiane na dodatkowych nadprowizowanych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0b097-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="0b097-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0b097-250">-SkuCapacity</span></span>
<span data-ttu-id="0b097-251">Określa liczbę wystąpień w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-251">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-252">-SKUName</span><span class="sxs-lookup"><span data-stu-id="0b097-252">-SkuName</span></span>
<span data-ttu-id="0b097-253">Określa rozmiar wszystkich wystąpień maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="0b097-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0b097-254">-SkuTier</span></span>
<span data-ttu-id="0b097-255">Określa warstwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="0b097-256">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b097-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b097-257">Standardowe</span><span class="sxs-lookup"><span data-stu-id="0b097-257">Standard</span></span>
- <span data-ttu-id="0b097-258">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="0b097-258">Basic</span></span>

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

### <span data-ttu-id="0b097-259">— Tag</span><span class="sxs-lookup"><span data-stu-id="0b097-259">-Tag</span></span>
<span data-ttu-id="0b097-260">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="0b097-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b097-261">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0b097-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0b097-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="0b097-263">Konfigurowany czas (w minutach) usunięcie maszyny wirtualnej będzie musiało potencjalnie zatwierdzić zdarzenie Zakończ zaplanowane przed automatycznym zatwierdzeniem zdarzenia (przeocz przekreślony czas).</span><span class="sxs-lookup"><span data-stu-id="0b097-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="0b097-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="0b097-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="0b097-265">Określa, czy zdarzenie Terminate Scheduled jest włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="0b097-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-266">- Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="0b097-266">-TimeZone</span></span>
<span data-ttu-id="0b097-267">Określa strefę czasową systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="0b097-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="0b097-268">np. \" Pacyfik (czas \" standardowy).</span><span class="sxs-lookup"><span data-stu-id="0b097-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="0b097-269">Możliwe wartości mogą [być](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id z stref czasowych zwracanych przez [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="0b097-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="0b097-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="0b097-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="0b097-271">Flaga umożliwiająca włączenie lub wyłączenie możliwości ustawienia co najmniej jednego zarządzanego dyskusyjnie danych z typem konta magazynu UltraSSD_LRS ustawionym na skalę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="0b097-272">Dysk zarządzany z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="0b097-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="0b097-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="0b097-274">Określono tryb uaktualniania do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="0b097-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="0b097-275">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b097-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b097-276">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="0b097-276">Automatic</span></span>
- <span data-ttu-id="0b097-277">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="0b097-277">Manual</span></span>
- <span data-ttu-id="0b097-278">Rolling</span><span class="sxs-lookup"><span data-stu-id="0b097-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-279">- VhdContainer</span><span class="sxs-lookup"><span data-stu-id="0b097-279">-VhdContainer</span></span>
<span data-ttu-id="0b097-280">Określa adresy URL kontenera służące do przechowywania dysków systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b097-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0b097-282">Określa lokalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="0b097-283">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVmss cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="0b097-284">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b097-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0b097-285">-VMScaleSetName</span></span>
<span data-ttu-id="0b097-286">Określa nazwę programu VMSS, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-287">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b097-287">-Confirm</span></span>
<span data-ttu-id="0b097-288">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b097-288">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b097-289">-WhatIf</span></span>
<span data-ttu-id="0b097-290">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b097-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b097-291">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b097-291">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b097-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b097-292">CommonParameters</span></span>
<span data-ttu-id="0b097-293">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b097-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b097-294">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b097-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b097-295">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b097-295">INPUTS</span></span>

### <span data-ttu-id="0b097-296">System.String</span><span class="sxs-lookup"><span data-stu-id="0b097-296">System.String</span></span>

### <span data-ttu-id="0b097-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b097-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0b097-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b097-298">System.Boolean</span></span>

## <span data-ttu-id="0b097-299">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b097-299">OUTPUTS</span></span>

### <span data-ttu-id="0b097-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b097-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0b097-301">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b097-301">NOTES</span></span>

## <span data-ttu-id="0b097-302">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b097-302">RELATED LINKS</span></span>

[<span data-ttu-id="0b097-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="0b097-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="0b097-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="0b097-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0b097-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0b097-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0b097-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b097-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


