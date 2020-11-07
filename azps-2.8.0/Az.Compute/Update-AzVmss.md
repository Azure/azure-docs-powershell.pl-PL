---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706116"
---
# <span data-ttu-id="91067-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-101">Update-AzVmss</span></span>

## <span data-ttu-id="91067-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91067-102">SYNOPSIS</span></span>
<span data-ttu-id="91067-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="91067-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91067-104">SYNTAX</span></span>

### <span data-ttu-id="91067-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91067-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91067-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="91067-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91067-107">Opis</span><span class="sxs-lookup"><span data-stu-id="91067-107">DESCRIPTION</span></span>
<span data-ttu-id="91067-108">Polecenie cmdlet **Update-AzVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="91067-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91067-109">EXAMPLES</span></span>

### <span data-ttu-id="91067-110">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="91067-111">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="91067-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91067-112">PARAMETERS</span></span>

### <span data-ttu-id="91067-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91067-113">-AsJob</span></span>
<span data-ttu-id="91067-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="91067-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91067-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="91067-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="91067-116">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="91067-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="91067-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="91067-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="91067-118">Czy należy włączyć diagnostykę rozruchu na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="91067-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="91067-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="91067-120">Identyfikator URI konta magazynu, który ma być używany do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="91067-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="91067-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="91067-121">-CustomData</span></span>
<span data-ttu-id="91067-122">Określa zakodowany ciąg Base-64 z danymi niestandardowymi.</span><span class="sxs-lookup"><span data-stu-id="91067-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="91067-123">Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="91067-124">Maksymalna długość tablicy binarnej to 65535 bajtów.</span><span class="sxs-lookup"><span data-stu-id="91067-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="91067-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91067-125">-DefaultProfile</span></span>
<span data-ttu-id="91067-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91067-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91067-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="91067-127">-DisableAutoRollback</span></span>
<span data-ttu-id="91067-128">Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="91067-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="91067-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="91067-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="91067-130">Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła dla systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="91067-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="91067-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="91067-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="91067-132">Wskazuje, czy na komputerach wirtualnych systemu Windows w VMSS są włączone aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="91067-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="91067-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="91067-133">-IdentityId</span></span>
<span data-ttu-id="91067-134">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="91067-135">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="91067-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="91067-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="91067-136">-IdentityType</span></span>
<span data-ttu-id="91067-137">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="91067-138">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91067-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="91067-139">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="91067-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91067-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91067-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="91067-141">SystemAssigned</span></span>
- <span data-ttu-id="91067-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="91067-142">UserAssigned</span></span>
- <span data-ttu-id="91067-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="91067-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="91067-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="91067-144">None</span></span>

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

### <span data-ttu-id="91067-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="91067-145">-ImageReferenceId</span></span>
<span data-ttu-id="91067-146">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="91067-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="91067-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="91067-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="91067-148">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="91067-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="91067-149">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="91067-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="91067-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="91067-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="91067-151">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="91067-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="91067-152">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="91067-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="91067-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="91067-153">-ImageReferenceSku</span></span>
<span data-ttu-id="91067-154">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="91067-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="91067-155">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="91067-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="91067-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="91067-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="91067-157">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="91067-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="91067-158">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="91067-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="91067-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="91067-159">-ImageUri</span></span>
<span data-ttu-id="91067-160">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91067-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="91067-161">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91067-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="91067-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91067-162">-LicenseType</span></span>
<span data-ttu-id="91067-163">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="91067-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="91067-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="91067-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="91067-165">Określa typ konta magazynu dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="91067-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="91067-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91067-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91067-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="91067-167">StandardLRS</span></span>
- <span data-ttu-id="91067-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="91067-168">PremiumLRS</span></span>

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

### <span data-ttu-id="91067-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="91067-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="91067-170">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="91067-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="91067-171">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="91067-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="91067-172">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="91067-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="91067-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="91067-173">-MaxPrice</span></span>
<span data-ttu-id="91067-174">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="91067-175">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="91067-175">This price is in US Dollars.</span></span> <span data-ttu-id="91067-176">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="91067-177">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="91067-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="91067-178">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="91067-179">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="91067-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="91067-180">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="91067-180">Example: 0.01538.</span></span>  <span data-ttu-id="91067-181">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="91067-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="91067-182">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="91067-182">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="91067-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="91067-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="91067-184">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="91067-185">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="91067-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="91067-186">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="91067-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="91067-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="91067-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="91067-188">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="91067-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="91067-189">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="91067-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="91067-190">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="91067-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="91067-191">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="91067-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="91067-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="91067-192">-OsDiskCaching</span></span>
<span data-ttu-id="91067-193">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="91067-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="91067-194">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91067-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91067-195">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="91067-195">None</span></span>
- <span data-ttu-id="91067-196">Odczytu</span><span class="sxs-lookup"><span data-stu-id="91067-196">ReadOnly</span></span>
- <span data-ttu-id="91067-197">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="91067-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="91067-198">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="91067-199">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="91067-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="91067-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="91067-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="91067-201">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="91067-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="91067-202">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="91067-202">-Overprovision</span></span>
<span data-ttu-id="91067-203">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="91067-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="91067-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="91067-205">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="91067-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="91067-206">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="91067-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="91067-207">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="91067-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="91067-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="91067-208">-PlanName</span></span>
<span data-ttu-id="91067-209">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="91067-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="91067-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="91067-210">-PlanProduct</span></span>
<span data-ttu-id="91067-211">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="91067-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="91067-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="91067-212">-PlanPromotionCode</span></span>
<span data-ttu-id="91067-213">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="91067-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="91067-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="91067-214">-PlanPublisher</span></span>
<span data-ttu-id="91067-215">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="91067-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="91067-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="91067-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="91067-217">Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych systemu Windows w VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="91067-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91067-218">-ResourceGroupName</span></span>
<span data-ttu-id="91067-219">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="91067-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="91067-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="91067-221">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="91067-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="91067-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="91067-222">-SkuCapacity</span></span>
<span data-ttu-id="91067-223">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="91067-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="91067-224">-SkuName</span></span>
<span data-ttu-id="91067-225">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="91067-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="91067-226">-SkuTier</span></span>
<span data-ttu-id="91067-227">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="91067-228">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91067-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91067-229">Standard</span><span class="sxs-lookup"><span data-stu-id="91067-229">Standard</span></span>
- <span data-ttu-id="91067-230">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="91067-230">Basic</span></span>

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

### <span data-ttu-id="91067-231">-Tag</span><span class="sxs-lookup"><span data-stu-id="91067-231">-Tag</span></span>
<span data-ttu-id="91067-232">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="91067-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="91067-233">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="91067-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="91067-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="91067-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="91067-235">Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).</span><span class="sxs-lookup"><span data-stu-id="91067-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="91067-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="91067-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="91067-237">Określa, czy zdarzenie Zakończ zaplanowane jest włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="91067-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="91067-238">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="91067-238">-TimeZone</span></span>
<span data-ttu-id="91067-239">Określa strefę czasową dla systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="91067-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="91067-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="91067-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="91067-241">Flaga, która umożliwia lub wyłącza możliwość posiadania jednego lub większej liczby zarządzanych dysków z danymi, UltraSSD_LRS typ konta magazynu w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="91067-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="91067-242">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="91067-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="91067-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="91067-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="91067-244">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="91067-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="91067-245">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91067-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91067-246">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="91067-246">Automatic</span></span>
- <span data-ttu-id="91067-247">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="91067-247">Manual</span></span>
- <span data-ttu-id="91067-248">System</span><span class="sxs-lookup"><span data-stu-id="91067-248">Rolling</span></span>

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

### <span data-ttu-id="91067-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="91067-249">-VhdContainer</span></span>
<span data-ttu-id="91067-250">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="91067-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91067-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="91067-252">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="91067-253">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="91067-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="91067-254">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="91067-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="91067-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="91067-255">-VMScaleSetName</span></span>
<span data-ttu-id="91067-256">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91067-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="91067-257">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91067-257">-Confirm</span></span>
<span data-ttu-id="91067-258">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91067-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91067-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91067-259">-WhatIf</span></span>
<span data-ttu-id="91067-260">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91067-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91067-261">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91067-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91067-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91067-262">CommonParameters</span></span>
<span data-ttu-id="91067-263">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91067-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91067-264">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91067-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91067-265">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91067-265">INPUTS</span></span>

### <span data-ttu-id="91067-266">System. String</span><span class="sxs-lookup"><span data-stu-id="91067-266">System.String</span></span>

### <span data-ttu-id="91067-267">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91067-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="91067-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91067-268">System.Boolean</span></span>

## <span data-ttu-id="91067-269">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91067-269">OUTPUTS</span></span>

### <span data-ttu-id="91067-270">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91067-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="91067-271">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91067-271">NOTES</span></span>

## <span data-ttu-id="91067-272">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91067-272">RELATED LINKS</span></span>

[<span data-ttu-id="91067-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="91067-274">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="91067-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="91067-276">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="91067-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="91067-278">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="91067-279">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="91067-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


