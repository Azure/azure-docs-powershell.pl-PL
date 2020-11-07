---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898010"
---
# <span data-ttu-id="6a0c6-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="6a0c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0c6-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a0c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a0c6-104">SYNTAX</span></span>

### <span data-ttu-id="6a0c6-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a0c6-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0c6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a0c6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6a0c6-107">DESCRIPTION</span></span>
<span data-ttu-id="6a0c6-108">Polecenie cmdlet **Update-AzureRmVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="6a0c6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a0c6-109">EXAMPLES</span></span>

### <span data-ttu-id="6a0c6-110">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="6a0c6-111">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="6a0c6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a0c6-112">PARAMETERS</span></span>

### <span data-ttu-id="6a0c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a0c6-113">-AsJob</span></span>
<span data-ttu-id="6a0c6-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a0c6-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="6a0c6-116">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="6a0c6-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="6a0c6-118">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="6a0c6-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="6a0c6-120">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="6a0c6-121">-CustomData</span></span>
<span data-ttu-id="6a0c6-122">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="6a0c6-123">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="6a0c6-124">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0c6-125">-DefaultProfile</span></span>
<span data-ttu-id="6a0c6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="6a0c6-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="6a0c6-128">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła dla systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="6a0c6-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="6a0c6-130">Wskazuje, czy na komputerach wirtualnych systemu Windows w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6a0c6-131">-IdentityId</span></span>
<span data-ttu-id="6a0c6-132">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6a0c6-133">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="6a0c6-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6a0c6-134">-IdentityType</span></span>
<span data-ttu-id="6a0c6-135">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="6a0c6-136">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="6a0c6-137">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="6a0c6-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a0c6-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6a0c6-139">SystemAssigned</span></span>
- <span data-ttu-id="6a0c6-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="6a0c6-140">UserAssigned</span></span>
- <span data-ttu-id="6a0c6-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="6a0c6-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="6a0c6-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a0c6-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="6a0c6-143">-ImageReferenceId</span></span>
<span data-ttu-id="6a0c6-144">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="6a0c6-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="6a0c6-146">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="6a0c6-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="6a0c6-147">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-147">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="6a0c6-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="6a0c6-149">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6a0c6-150">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-150">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="6a0c6-151">-ImageReferenceSku</span></span>
<span data-ttu-id="6a0c6-152">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="6a0c6-153">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-153">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="6a0c6-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="6a0c6-155">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="6a0c6-156">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="6a0c6-157">-ImageUri</span></span>
<span data-ttu-id="6a0c6-158">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="6a0c6-159">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6a0c6-160">-LicenseType</span></span>
<span data-ttu-id="6a0c6-161">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6a0c6-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="6a0c6-163">Określa typ konta magazynu dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="6a0c6-164">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a0c6-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="6a0c6-165">StandardLRS</span></span>
- <span data-ttu-id="6a0c6-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="6a0c6-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6a0c6-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="6a0c6-168">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="6a0c6-169">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="6a0c6-170">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6a0c6-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="6a0c6-172">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="6a0c6-173">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="6a0c6-174">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6a0c6-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="6a0c6-176">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="6a0c6-177">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="6a0c6-178">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="6a0c6-179">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="6a0c6-180">-OsDiskCaching</span></span>
<span data-ttu-id="6a0c6-181">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="6a0c6-182">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a0c6-183">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a0c6-183">None</span></span>
- <span data-ttu-id="6a0c6-184">Odczytu</span><span class="sxs-lookup"><span data-stu-id="6a0c6-184">ReadOnly</span></span>
- <span data-ttu-id="6a0c6-185">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6a0c6-185">ReadWrite</span></span>

<span data-ttu-id="6a0c6-186">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="6a0c6-187">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="6a0c6-188">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6a0c6-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="6a0c6-190">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-191">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="6a0c6-191">-Overprovision</span></span>
<span data-ttu-id="6a0c6-192">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="6a0c6-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="6a0c6-194">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="6a0c6-195">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="6a0c6-196">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="6a0c6-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-197">-PlanName</span></span>
<span data-ttu-id="6a0c6-198">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6a0c6-199">-PlanProduct</span></span>
<span data-ttu-id="6a0c6-200">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="6a0c6-201">-PlanPromotionCode</span></span>
<span data-ttu-id="6a0c6-202">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6a0c6-203">-PlanPublisher</span></span>
<span data-ttu-id="6a0c6-204">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="6a0c6-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="6a0c6-206">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych systemu Windows w VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-207">-ResourceGroupName</span></span>
<span data-ttu-id="6a0c6-208">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6a0c6-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="6a0c6-210">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6a0c6-211">-SkuCapacity</span></span>
<span data-ttu-id="6a0c6-212">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-213">-SkuName</span></span>
<span data-ttu-id="6a0c6-214">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6a0c6-215">-SkuTier</span></span>
<span data-ttu-id="6a0c6-216">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="6a0c6-217">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a0c6-218">Standard</span><span class="sxs-lookup"><span data-stu-id="6a0c6-218">Standard</span></span>
- <span data-ttu-id="6a0c6-219">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="6a0c6-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-220">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a0c6-220">-Tag</span></span>
<span data-ttu-id="6a0c6-221">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a0c6-222">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-222">For example:</span></span>

<span data-ttu-id="6a0c6-223">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6a0c6-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="6a0c6-224">-TimeZone</span></span>
<span data-ttu-id="6a0c6-225">Określa strefę czasową dla systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6a0c6-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="6a0c6-227">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="6a0c6-228">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a0c6-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a0c6-229">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="6a0c6-229">Automatic</span></span>
- <span data-ttu-id="6a0c6-230">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="6a0c6-230">Manual</span></span>
- <span data-ttu-id="6a0c6-231">System</span><span class="sxs-lookup"><span data-stu-id="6a0c6-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="6a0c6-232">-VhdContainer</span></span>
<span data-ttu-id="6a0c6-233">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6a0c6-235">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="6a0c6-236">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-236">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="6a0c6-237">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6a0c6-238">-VMScaleSetName</span></span>
<span data-ttu-id="6a0c6-239">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-240">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a0c6-240">-Confirm</span></span>
<span data-ttu-id="6a0c6-241">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0c6-242">-WhatIf</span></span>
<span data-ttu-id="6a0c6-243">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6a0c6-244">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c6-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0c6-245">CommonParameters</span></span>
<span data-ttu-id="6a0c6-246">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0c6-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0c6-247">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0c6-247">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0c6-248">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a0c6-248">INPUTS</span></span>

### <span data-ttu-id="6a0c6-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="6a0c6-250">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6a0c6-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="6a0c6-251">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a0c6-251">OUTPUTS</span></span>

### <span data-ttu-id="6a0c6-252">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a0c6-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6a0c6-253">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a0c6-253">NOTES</span></span>

## <span data-ttu-id="6a0c6-254">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a0c6-254">RELATED LINKS</span></span>

[<span data-ttu-id="6a0c6-255">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-255">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-256">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-256">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-257">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-257">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-258">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-258">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-259">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-259">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-260">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-260">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="6a0c6-261">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6a0c6-261">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


