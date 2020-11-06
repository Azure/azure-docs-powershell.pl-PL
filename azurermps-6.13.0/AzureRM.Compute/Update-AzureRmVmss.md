---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548804"
---
# <span data-ttu-id="f751d-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="f751d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f751d-102">SYNOPSIS</span></span>
<span data-ttu-id="f751d-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f751d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f751d-104">SYNTAX</span></span>

### <span data-ttu-id="f751d-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f751d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f751d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f751d-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f751d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f751d-107">DESCRIPTION</span></span>
<span data-ttu-id="f751d-108">Polecenie cmdlet **Update-AzureRmVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="f751d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f751d-109">EXAMPLES</span></span>

### <span data-ttu-id="f751d-110">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="f751d-111">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="f751d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f751d-112">PARAMETERS</span></span>

### <span data-ttu-id="f751d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f751d-113">-AsJob</span></span>
<span data-ttu-id="f751d-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="f751d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f751d-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f751d-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="f751d-116">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="f751d-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="f751d-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="f751d-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="f751d-118">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f751d-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="f751d-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="f751d-120">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="f751d-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="f751d-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="f751d-121">-CustomData</span></span>
<span data-ttu-id="f751d-122">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="f751d-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="f751d-123">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="f751d-124">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="f751d-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="f751d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f751d-125">-DefaultProfile</span></span>
<span data-ttu-id="f751d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f751d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751d-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="f751d-127">-DisableAutoRollback</span></span>
<span data-ttu-id="f751d-128">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="f751d-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="f751d-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="f751d-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="f751d-130">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła dla systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="f751d-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="f751d-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="f751d-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="f751d-132">Wskazuje, czy na komputerach wirtualnych systemu Windows w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="f751d-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="f751d-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="f751d-133">-IdentityId</span></span>
<span data-ttu-id="f751d-134">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="f751d-135">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="f751d-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="f751d-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f751d-136">-IdentityType</span></span>
<span data-ttu-id="f751d-137">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="f751d-138">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f751d-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="f751d-139">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="f751d-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f751d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751d-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f751d-141">SystemAssigned</span></span>
- <span data-ttu-id="f751d-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="f751d-142">UserAssigned</span></span>
- <span data-ttu-id="f751d-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="f751d-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="f751d-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f751d-144">None</span></span>

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

### <span data-ttu-id="f751d-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="f751d-145">-ImageReferenceId</span></span>
<span data-ttu-id="f751d-146">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="f751d-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="f751d-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="f751d-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="f751d-148">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="f751d-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="f751d-149">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="f751d-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="f751d-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="f751d-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="f751d-151">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="f751d-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f751d-152">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="f751d-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f751d-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="f751d-153">-ImageReferenceSku</span></span>
<span data-ttu-id="f751d-154">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="f751d-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="f751d-155">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="f751d-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f751d-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="f751d-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="f751d-157">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="f751d-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="f751d-158">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="f751d-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="f751d-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="f751d-159">-ImageUri</span></span>
<span data-ttu-id="f751d-160">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f751d-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="f751d-161">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f751d-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="f751d-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f751d-162">-LicenseType</span></span>
<span data-ttu-id="f751d-163">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="f751d-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="f751d-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f751d-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="f751d-165">Określa typ konta magazynu dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="f751d-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="f751d-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f751d-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751d-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="f751d-167">StandardLRS</span></span>
- <span data-ttu-id="f751d-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="f751d-168">PremiumLRS</span></span>

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

### <span data-ttu-id="f751d-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f751d-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="f751d-170">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="f751d-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="f751d-171">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="f751d-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="f751d-172">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="f751d-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="f751d-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f751d-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="f751d-174">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="f751d-175">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="f751d-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="f751d-176">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="f751d-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="f751d-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f751d-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="f751d-178">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="f751d-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="f751d-179">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="f751d-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="f751d-180">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="f751d-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="f751d-181">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="f751d-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="f751d-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="f751d-182">-OsDiskCaching</span></span>
<span data-ttu-id="f751d-183">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f751d-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="f751d-184">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f751d-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751d-185">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f751d-185">None</span></span>
- <span data-ttu-id="f751d-186">Odczytu</span><span class="sxs-lookup"><span data-stu-id="f751d-186">ReadOnly</span></span>
- <span data-ttu-id="f751d-187">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="f751d-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="f751d-188">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="f751d-189">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="f751d-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="f751d-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f751d-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="f751d-191">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f751d-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="f751d-192">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="f751d-192">-Overprovision</span></span>
<span data-ttu-id="f751d-193">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="f751d-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="f751d-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="f751d-195">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="f751d-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="f751d-196">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="f751d-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="f751d-197">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="f751d-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="f751d-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f751d-198">-PlanName</span></span>
<span data-ttu-id="f751d-199">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="f751d-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="f751d-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="f751d-200">-PlanProduct</span></span>
<span data-ttu-id="f751d-201">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="f751d-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="f751d-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="f751d-202">-PlanPromotionCode</span></span>
<span data-ttu-id="f751d-203">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="f751d-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="f751d-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f751d-204">-PlanPublisher</span></span>
<span data-ttu-id="f751d-205">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="f751d-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="f751d-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="f751d-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="f751d-207">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych systemu Windows w VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="f751d-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f751d-208">-ResourceGroupName</span></span>
<span data-ttu-id="f751d-209">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f751d-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f751d-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="f751d-211">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="f751d-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="f751d-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f751d-212">-SkuCapacity</span></span>
<span data-ttu-id="f751d-213">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="f751d-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f751d-214">-SkuName</span></span>
<span data-ttu-id="f751d-215">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="f751d-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f751d-216">-SkuTier</span></span>
<span data-ttu-id="f751d-217">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="f751d-218">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f751d-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751d-219">Standard</span><span class="sxs-lookup"><span data-stu-id="f751d-219">Standard</span></span>
- <span data-ttu-id="f751d-220">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="f751d-220">Basic</span></span>

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

### <span data-ttu-id="f751d-221">-Tag</span><span class="sxs-lookup"><span data-stu-id="f751d-221">-Tag</span></span>
<span data-ttu-id="f751d-222">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f751d-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f751d-223">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f751d-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f751d-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="f751d-224">-TimeZone</span></span>
<span data-ttu-id="f751d-225">Określa strefę czasową dla systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="f751d-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="f751d-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="f751d-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="f751d-227">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f751d-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="f751d-228">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="f751d-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="f751d-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="f751d-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="f751d-230">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f751d-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="f751d-231">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f751d-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751d-232">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="f751d-232">Automatic</span></span>
- <span data-ttu-id="f751d-233">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="f751d-233">Manual</span></span>
- <span data-ttu-id="f751d-234">System</span><span class="sxs-lookup"><span data-stu-id="f751d-234">Rolling</span></span>

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

### <span data-ttu-id="f751d-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="f751d-235">-VhdContainer</span></span>
<span data-ttu-id="f751d-236">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="f751d-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f751d-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f751d-238">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="f751d-239">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="f751d-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="f751d-240">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="f751d-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f751d-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f751d-241">-VMScaleSetName</span></span>
<span data-ttu-id="f751d-242">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f751d-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f751d-243">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f751d-243">-Confirm</span></span>
<span data-ttu-id="f751d-244">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f751d-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f751d-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f751d-245">-WhatIf</span></span>
<span data-ttu-id="f751d-246">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f751d-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f751d-247">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f751d-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f751d-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f751d-248">CommonParameters</span></span>
<span data-ttu-id="f751d-249">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f751d-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f751d-250">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f751d-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f751d-251">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f751d-251">INPUTS</span></span>

### <span data-ttu-id="f751d-252">System. String</span><span class="sxs-lookup"><span data-stu-id="f751d-252">System.String</span></span>

### <span data-ttu-id="f751d-253">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f751d-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="f751d-254">Parametry: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f751d-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="f751d-255">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f751d-255">OUTPUTS</span></span>

### <span data-ttu-id="f751d-256">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f751d-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f751d-257">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f751d-257">NOTES</span></span>

## <span data-ttu-id="f751d-258">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f751d-258">RELATED LINKS</span></span>

[<span data-ttu-id="f751d-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="f751d-260">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f751d-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f751d-262">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f751d-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="f751d-264">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f751d-265">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f751d-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


