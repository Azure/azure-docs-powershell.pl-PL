---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304152"
---
# <span data-ttu-id="616a8-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-101">Update-AzVmss</span></span>

## <span data-ttu-id="616a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="616a8-102">SYNOPSIS</span></span>
<span data-ttu-id="616a8-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="616a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="616a8-104">SYNTAX</span></span>

### <span data-ttu-id="616a8-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="616a8-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="616a8-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="616a8-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="616a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="616a8-107">DESCRIPTION</span></span>
<span data-ttu-id="616a8-108">Polecenie cmdlet **Update-AzVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="616a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="616a8-109">EXAMPLES</span></span>

### <span data-ttu-id="616a8-110">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="616a8-111">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="616a8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="616a8-112">PARAMETERS</span></span>

### <span data-ttu-id="616a8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="616a8-113">-AsJob</span></span>
<span data-ttu-id="616a8-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="616a8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="616a8-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="616a8-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="616a8-116">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="616a8-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="616a8-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="616a8-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="616a8-118">Ilość czasu, w której automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="616a8-119">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="616a8-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="616a8-120">Pomaga to uniknąć przedwczesnych lub przypadkowych napraw.</span><span class="sxs-lookup"><span data-stu-id="616a8-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="616a8-121">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="616a8-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="616a8-122">Minimalny dozwolony okres prolongaty to 30 minut (PT30M), który jest również wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="616a8-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="616a8-123">Maksymalny dozwolony okres prolongaty to 90 minut (PT90M).</span><span class="sxs-lookup"><span data-stu-id="616a8-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="616a8-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="616a8-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="616a8-125">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="616a8-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="616a8-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="616a8-127">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="616a8-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="616a8-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="616a8-128">-CustomData</span></span>
<span data-ttu-id="616a8-129">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="616a8-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="616a8-130">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="616a8-131">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="616a8-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="616a8-132">Aby uzyskać informacje na temat używania chmury-init dla maszyny wirtualnej, zobacz [Używanie chmury-init w celu dostosowania maszyny wirtualnej Linux podczas jej tworzenia](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="616a8-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="616a8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616a8-133">-DefaultProfile</span></span>
<span data-ttu-id="616a8-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="616a8-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="616a8-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="616a8-135">-DisableAutoRollback</span></span>
<span data-ttu-id="616a8-136">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="616a8-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="616a8-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="616a8-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="616a8-138">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła dla systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="616a8-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="616a8-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="616a8-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="616a8-140">Włączanie lub wyłączanie automatycznego naprawiania w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="616a8-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="616a8-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="616a8-142">Wskazuje, czy na komputerach wirtualnych systemu Windows w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="616a8-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="616a8-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="616a8-143">-EncryptionAtHost</span></span>
<span data-ttu-id="616a8-144">Ten parametr może być wykorzystywany przez użytkownika w żądaniu do włączania lub wyłączania szyfrowania hosta dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="616a8-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="616a8-145">-IdentityId</span></span>
<span data-ttu-id="616a8-146">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="616a8-147">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="616a8-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="616a8-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="616a8-148">-IdentityType</span></span>
<span data-ttu-id="616a8-149">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="616a8-150">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="616a8-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="616a8-151">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="616a8-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="616a8-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="616a8-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="616a8-153">SystemAssigned</span></span>
- <span data-ttu-id="616a8-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="616a8-154">UserAssigned</span></span>
- <span data-ttu-id="616a8-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="616a8-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="616a8-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="616a8-156">None</span></span>

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

### <span data-ttu-id="616a8-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="616a8-157">-ImageReferenceId</span></span>
<span data-ttu-id="616a8-158">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="616a8-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="616a8-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="616a8-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="616a8-160">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="616a8-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="616a8-161">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="616a8-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="616a8-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="616a8-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="616a8-163">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="616a8-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="616a8-164">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="616a8-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="616a8-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="616a8-165">-ImageReferenceSku</span></span>
<span data-ttu-id="616a8-166">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="616a8-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="616a8-167">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="616a8-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="616a8-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="616a8-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="616a8-169">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="616a8-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="616a8-170">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="616a8-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="616a8-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="616a8-171">-ImageUri</span></span>
<span data-ttu-id="616a8-172">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="616a8-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="616a8-173">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="616a8-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="616a8-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="616a8-174">-LicenseType</span></span>
<span data-ttu-id="616a8-175">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="616a8-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="616a8-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="616a8-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="616a8-177">Określa typ konta magazynu dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="616a8-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="616a8-178">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="616a8-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="616a8-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="616a8-179">StandardLRS</span></span>
- <span data-ttu-id="616a8-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="616a8-180">PremiumLRS</span></span>

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

### <span data-ttu-id="616a8-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="616a8-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="616a8-182">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="616a8-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="616a8-183">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="616a8-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="616a8-184">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="616a8-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="616a8-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="616a8-185">-MaxPrice</span></span>
<span data-ttu-id="616a8-186">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="616a8-187">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="616a8-187">This price is in US Dollars.</span></span> <span data-ttu-id="616a8-188">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="616a8-189">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="616a8-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="616a8-190">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="616a8-191">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="616a8-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="616a8-192">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="616a8-192">Example: 0.01538.</span></span>  <span data-ttu-id="616a8-193">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="616a8-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="616a8-194">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="616a8-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="616a8-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="616a8-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="616a8-196">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="616a8-197">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="616a8-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="616a8-198">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="616a8-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="616a8-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="616a8-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="616a8-200">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="616a8-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="616a8-201">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="616a8-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="616a8-202">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="616a8-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="616a8-203">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="616a8-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="616a8-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="616a8-204">-OsDiskCaching</span></span>
<span data-ttu-id="616a8-205">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="616a8-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="616a8-206">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="616a8-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="616a8-207">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="616a8-207">None</span></span>
- <span data-ttu-id="616a8-208">Odczytu</span><span class="sxs-lookup"><span data-stu-id="616a8-208">ReadOnly</span></span>
- <span data-ttu-id="616a8-209">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="616a8-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="616a8-210">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="616a8-211">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="616a8-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="616a8-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="616a8-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="616a8-213">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="616a8-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="616a8-214">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="616a8-214">-Overprovision</span></span>
<span data-ttu-id="616a8-215">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="616a8-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="616a8-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="616a8-217">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="616a8-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="616a8-218">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="616a8-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="616a8-219">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="616a8-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="616a8-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="616a8-220">-PlanName</span></span>
<span data-ttu-id="616a8-221">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="616a8-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="616a8-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="616a8-222">-PlanProduct</span></span>
<span data-ttu-id="616a8-223">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="616a8-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="616a8-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="616a8-224">-PlanPromotionCode</span></span>
<span data-ttu-id="616a8-225">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="616a8-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="616a8-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="616a8-226">-PlanPublisher</span></span>
<span data-ttu-id="616a8-227">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="616a8-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="616a8-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="616a8-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="616a8-229">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych systemu Windows w VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="616a8-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="616a8-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="616a8-231">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="616a8-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="616a8-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="616a8-232">-ResourceGroupName</span></span>
<span data-ttu-id="616a8-233">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="616a8-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="616a8-234">-ScaleInPolicy</span></span>
<span data-ttu-id="616a8-235">Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="616a8-236">Możliwe wartości: "default", "OldestVM" i "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="616a8-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="616a8-237">"Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.</span><span class="sxs-lookup"><span data-stu-id="616a8-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="616a8-238">Następnie będzie on w miarę możliwości równoważony między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="616a8-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="616a8-239">W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.</span><span class="sxs-lookup"><span data-stu-id="616a8-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="616a8-240">OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="616a8-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="616a8-241">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="616a8-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="616a8-242">W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="616a8-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="616a8-243">NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="616a8-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="616a8-244">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="616a8-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="616a8-245">W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="616a8-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="616a8-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="616a8-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="616a8-247">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="616a8-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="616a8-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="616a8-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="616a8-249">Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="616a8-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="616a8-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="616a8-250">-SkuCapacity</span></span>
<span data-ttu-id="616a8-251">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="616a8-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="616a8-252">-SkuName</span></span>
<span data-ttu-id="616a8-253">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="616a8-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="616a8-254">-SkuTier</span></span>
<span data-ttu-id="616a8-255">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="616a8-256">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="616a8-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="616a8-257">Standard</span><span class="sxs-lookup"><span data-stu-id="616a8-257">Standard</span></span>
- <span data-ttu-id="616a8-258">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="616a8-258">Basic</span></span>

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

### <span data-ttu-id="616a8-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="616a8-259">-Tag</span></span>
<span data-ttu-id="616a8-260">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="616a8-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="616a8-261">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="616a8-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="616a8-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="616a8-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="616a8-263">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="616a8-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="616a8-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="616a8-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="616a8-265">Określa, czy zdarzenie Zakończ zaplanowane jest włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="616a8-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="616a8-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="616a8-266">-TimeZone</span></span>
<span data-ttu-id="616a8-267">Określa strefę czasową dla systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="616a8-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="616a8-268">na przykład \" Pacyfik (czas standardowy) \" .</span><span class="sxs-lookup"><span data-stu-id="616a8-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="616a8-269">Możliwe wartości mogą być [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) wartością ze stref czasowych zwróconych przez [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="616a8-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="616a8-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="616a8-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="616a8-271">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="616a8-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="616a8-272">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="616a8-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="616a8-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="616a8-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="616a8-274">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="616a8-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="616a8-275">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="616a8-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="616a8-276">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="616a8-276">Automatic</span></span>
- <span data-ttu-id="616a8-277">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="616a8-277">Manual</span></span>
- <span data-ttu-id="616a8-278">System</span><span class="sxs-lookup"><span data-stu-id="616a8-278">Rolling</span></span>

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

### <span data-ttu-id="616a8-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="616a8-279">-VhdContainer</span></span>
<span data-ttu-id="616a8-280">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="616a8-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="616a8-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="616a8-282">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="616a8-283">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="616a8-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="616a8-284">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="616a8-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="616a8-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="616a8-285">-VMScaleSetName</span></span>
<span data-ttu-id="616a8-286">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="616a8-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="616a8-287">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="616a8-287">-Confirm</span></span>
<span data-ttu-id="616a8-288">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="616a8-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="616a8-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="616a8-289">-WhatIf</span></span>
<span data-ttu-id="616a8-290">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="616a8-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="616a8-291">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="616a8-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="616a8-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616a8-292">CommonParameters</span></span>
<span data-ttu-id="616a8-293">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616a8-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616a8-294">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="616a8-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616a8-295">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="616a8-295">INPUTS</span></span>

### <span data-ttu-id="616a8-296">System. String</span><span class="sxs-lookup"><span data-stu-id="616a8-296">System.String</span></span>

### <span data-ttu-id="616a8-297">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="616a8-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="616a8-298">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="616a8-298">System.Boolean</span></span>

## <span data-ttu-id="616a8-299">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="616a8-299">OUTPUTS</span></span>

### <span data-ttu-id="616a8-300">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="616a8-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="616a8-301">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="616a8-301">NOTES</span></span>

## <span data-ttu-id="616a8-302">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="616a8-302">RELATED LINKS</span></span>

[<span data-ttu-id="616a8-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="616a8-304">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="616a8-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="616a8-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="616a8-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="616a8-308">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="616a8-309">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="616a8-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


