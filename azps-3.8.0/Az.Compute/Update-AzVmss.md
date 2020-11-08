---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053553"
---
# <span data-ttu-id="5e5dd-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-101">Update-AzVmss</span></span>

## <span data-ttu-id="5e5dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5dd-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="5e5dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e5dd-104">SYNTAX</span></span>

### <span data-ttu-id="5e5dd-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e5dd-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e5dd-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e5dd-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e5dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5e5dd-107">DESCRIPTION</span></span>
<span data-ttu-id="5e5dd-108">Polecenie cmdlet **Update-AzVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="5e5dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e5dd-109">EXAMPLES</span></span>

### <span data-ttu-id="5e5dd-110">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="5e5dd-111">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="5e5dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e5dd-112">PARAMETERS</span></span>

### <span data-ttu-id="5e5dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e5dd-113">-AsJob</span></span>
<span data-ttu-id="5e5dd-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5e5dd-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5e5dd-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="5e5dd-116">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="5e5dd-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="5e5dd-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="5e5dd-118">Ilość czasu, w której automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="5e5dd-119">Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="5e5dd-120">Pomaga to uniknąć przedwczesnych lub przypadkowych napraw.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="5e5dd-121">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="5e5dd-122">Wartość domyślna to 5 minut (PT5M).</span><span class="sxs-lookup"><span data-stu-id="5e5dd-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="5e5dd-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="5e5dd-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="5e5dd-124">Procent (pojemność scaleset) maszyn wirtualnych, które zostaną jednocześnie naprawione.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="5e5dd-125">Wartość domyślna to 20%.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="5e5dd-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="5e5dd-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="5e5dd-127">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5e5dd-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="5e5dd-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="5e5dd-129">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="5e5dd-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="5e5dd-130">-CustomData</span></span>
<span data-ttu-id="5e5dd-131">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="5e5dd-132">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="5e5dd-133">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="5e5dd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5dd-134">-DefaultProfile</span></span>
<span data-ttu-id="5e5dd-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e5dd-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="5e5dd-136">-DisableAutoRollback</span></span>
<span data-ttu-id="5e5dd-137">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="5e5dd-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="5e5dd-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="5e5dd-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="5e5dd-139">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła dla systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="5e5dd-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="5e5dd-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="5e5dd-141">Włączanie lub wyłączanie automatycznego naprawiania w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5e5dd-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="5e5dd-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="5e5dd-143">Wskazuje, czy na komputerach wirtualnych systemu Windows w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="5e5dd-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5e5dd-144">-IdentityId</span></span>
<span data-ttu-id="5e5dd-145">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5e5dd-146">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="5e5dd-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5e5dd-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5e5dd-147">-IdentityType</span></span>
<span data-ttu-id="5e5dd-148">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="5e5dd-149">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="5e5dd-150">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="5e5dd-151">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e5dd-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e5dd-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5e5dd-152">SystemAssigned</span></span>
- <span data-ttu-id="5e5dd-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="5e5dd-153">UserAssigned</span></span>
- <span data-ttu-id="5e5dd-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="5e5dd-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="5e5dd-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e5dd-155">None</span></span>

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

### <span data-ttu-id="5e5dd-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="5e5dd-156">-ImageReferenceId</span></span>
<span data-ttu-id="5e5dd-157">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="5e5dd-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="5e5dd-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="5e5dd-159">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="5e5dd-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="5e5dd-160">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="5e5dd-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="5e5dd-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="5e5dd-162">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5e5dd-163">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5e5dd-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="5e5dd-164">-ImageReferenceSku</span></span>
<span data-ttu-id="5e5dd-165">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="5e5dd-166">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="5e5dd-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="5e5dd-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="5e5dd-168">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="5e5dd-169">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="5e5dd-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="5e5dd-170">-ImageUri</span></span>
<span data-ttu-id="5e5dd-171">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="5e5dd-172">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="5e5dd-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5e5dd-173">-LicenseType</span></span>
<span data-ttu-id="5e5dd-174">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5e5dd-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5e5dd-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="5e5dd-176">Określa typ konta magazynu dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="5e5dd-177">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e5dd-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e5dd-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="5e5dd-178">StandardLRS</span></span>
- <span data-ttu-id="5e5dd-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="5e5dd-179">PremiumLRS</span></span>

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

### <span data-ttu-id="5e5dd-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5e5dd-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="5e5dd-181">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="5e5dd-182">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="5e5dd-183">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5e5dd-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5e5dd-184">-MaxPrice</span></span>
<span data-ttu-id="5e5dd-185">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="5e5dd-186">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-186">This price is in US Dollars.</span></span> <span data-ttu-id="5e5dd-187">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="5e5dd-188">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="5e5dd-189">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="5e5dd-190">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="5e5dd-191">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-191">Example: 0.01538.</span></span>  <span data-ttu-id="5e5dd-192">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="5e5dd-193">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="5e5dd-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5e5dd-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="5e5dd-195">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="5e5dd-196">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="5e5dd-197">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5e5dd-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5e5dd-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="5e5dd-199">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="5e5dd-200">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="5e5dd-201">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="5e5dd-202">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5e5dd-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="5e5dd-203">-OsDiskCaching</span></span>
<span data-ttu-id="5e5dd-204">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="5e5dd-205">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e5dd-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e5dd-206">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e5dd-206">None</span></span>
- <span data-ttu-id="5e5dd-207">Odczytu</span><span class="sxs-lookup"><span data-stu-id="5e5dd-207">ReadOnly</span></span>
- <span data-ttu-id="5e5dd-208">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="5e5dd-209">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="5e5dd-210">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="5e5dd-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="5e5dd-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="5e5dd-212">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="5e5dd-213">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="5e5dd-213">-Overprovision</span></span>
<span data-ttu-id="5e5dd-214">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="5e5dd-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="5e5dd-216">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="5e5dd-217">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="5e5dd-218">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="5e5dd-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="5e5dd-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5e5dd-219">-PlanName</span></span>
<span data-ttu-id="5e5dd-220">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="5e5dd-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5e5dd-221">-PlanProduct</span></span>
<span data-ttu-id="5e5dd-222">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="5e5dd-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5e5dd-223">-PlanPromotionCode</span></span>
<span data-ttu-id="5e5dd-224">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="5e5dd-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5e5dd-225">-PlanPublisher</span></span>
<span data-ttu-id="5e5dd-226">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="5e5dd-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="5e5dd-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="5e5dd-228">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych systemu Windows w VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5e5dd-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5e5dd-230">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="5e5dd-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5dd-231">-ResourceGroupName</span></span>
<span data-ttu-id="5e5dd-232">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="5e5dd-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="5e5dd-233">-ScaleInPolicy</span></span>
<span data-ttu-id="5e5dd-234">Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="5e5dd-235">Możliwe wartości: "default", "OldestVM" i "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="5e5dd-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="5e5dd-236">"Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="5e5dd-237">Następnie będzie on w miarę możliwości równoważony między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="5e5dd-238">W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="5e5dd-239">OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5e5dd-240">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5e5dd-241">W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="5e5dd-242">NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5e5dd-243">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5e5dd-244">W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="5e5dd-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5e5dd-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="5e5dd-246">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="5e5dd-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="5e5dd-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="5e5dd-248">Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="5e5dd-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5e5dd-249">-SkuCapacity</span></span>
<span data-ttu-id="5e5dd-250">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e5dd-251">-SkuName</span></span>
<span data-ttu-id="5e5dd-252">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5e5dd-253">-SkuTier</span></span>
<span data-ttu-id="5e5dd-254">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="5e5dd-255">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e5dd-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e5dd-256">Standard</span><span class="sxs-lookup"><span data-stu-id="5e5dd-256">Standard</span></span>
- <span data-ttu-id="5e5dd-257">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="5e5dd-257">Basic</span></span>

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

### <span data-ttu-id="5e5dd-258">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e5dd-258">-Tag</span></span>
<span data-ttu-id="5e5dd-259">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e5dd-260">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5e5dd-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e5dd-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5e5dd-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="5e5dd-262">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="5e5dd-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="5e5dd-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="5e5dd-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="5e5dd-264">Określa, czy zdarzenie Zakończ zaplanowane jest włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="5e5dd-265">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5e5dd-265">-TimeZone</span></span>
<span data-ttu-id="5e5dd-266">Określa strefę czasową dla systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="5e5dd-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="5e5dd-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="5e5dd-268">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="5e5dd-269">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="5e5dd-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5e5dd-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="5e5dd-271">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="5e5dd-272">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e5dd-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e5dd-273">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="5e5dd-273">Automatic</span></span>
- <span data-ttu-id="5e5dd-274">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="5e5dd-274">Manual</span></span>
- <span data-ttu-id="5e5dd-275">System</span><span class="sxs-lookup"><span data-stu-id="5e5dd-275">Rolling</span></span>

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

### <span data-ttu-id="5e5dd-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="5e5dd-276">-VhdContainer</span></span>
<span data-ttu-id="5e5dd-277">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5e5dd-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5e5dd-279">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="5e5dd-280">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="5e5dd-281">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="5e5dd-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5e5dd-282">-VMScaleSetName</span></span>
<span data-ttu-id="5e5dd-283">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5e5dd-284">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e5dd-284">-Confirm</span></span>
<span data-ttu-id="5e5dd-285">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e5dd-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e5dd-286">-WhatIf</span></span>
<span data-ttu-id="5e5dd-287">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e5dd-288">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e5dd-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5dd-289">CommonParameters</span></span>
<span data-ttu-id="5e5dd-290">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e5dd-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5dd-291">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e5dd-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5dd-292">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e5dd-292">INPUTS</span></span>

### <span data-ttu-id="5e5dd-293">System. String</span><span class="sxs-lookup"><span data-stu-id="5e5dd-293">System.String</span></span>

### <span data-ttu-id="5e5dd-294">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5e5dd-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5e5dd-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e5dd-295">System.Boolean</span></span>

## <span data-ttu-id="5e5dd-296">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e5dd-296">OUTPUTS</span></span>

### <span data-ttu-id="5e5dd-297">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5e5dd-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5e5dd-298">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e5dd-298">NOTES</span></span>

## <span data-ttu-id="5e5dd-299">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e5dd-299">RELATED LINKS</span></span>

[<span data-ttu-id="5e5dd-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="5e5dd-301">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="5e5dd-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="5e5dd-303">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="5e5dd-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="5e5dd-305">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="5e5dd-306">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e5dd-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


