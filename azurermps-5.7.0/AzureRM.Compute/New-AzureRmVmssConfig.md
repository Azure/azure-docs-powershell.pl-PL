---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542704"
---
# <span data-ttu-id="3f20f-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3f20f-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="3f20f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f20f-102">SYNOPSIS</span></span>
<span data-ttu-id="3f20f-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f20f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f20f-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f20f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f20f-105">DESCRIPTION</span></span>
<span data-ttu-id="3f20f-106">Polecenie cmdlet **New-AzureRmVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3f20f-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="3f20f-107">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f20f-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="3f20f-108">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="3f20f-108">These cmdlets are:</span></span>

- <span data-ttu-id="3f20f-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="3f20f-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="3f20f-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f20f-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="3f20f-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3f20f-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="3f20f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f20f-113">EXAMPLES</span></span>

### <span data-ttu-id="3f20f-114">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="3f20f-114">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="3f20f-115">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="3f20f-116">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="3f20f-117">W drugim poleceniu użyto polecenia cmdlet **New-AzureRmVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="3f20f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f20f-118">PARAMETERS</span></span>

### <span data-ttu-id="3f20f-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3f20f-119">-BootDiagnostic</span></span>
<span data-ttu-id="3f20f-120">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-121">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="3f20f-121">-Extension</span></span>
<span data-ttu-id="3f20f-122">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="3f20f-123">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="3f20f-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3f20f-124">-IdentityType</span></span>
<span data-ttu-id="3f20f-125">Określ tożsamość zestawu skali maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="3f20f-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3f20f-126">-LicenseType</span></span>
<span data-ttu-id="3f20f-127">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="3f20f-127">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3f20f-128">-Location</span></span>
<span data-ttu-id="3f20f-129">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-129">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f20f-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="3f20f-131">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="3f20f-132">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="3f20f-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-133">-OsProfile</span></span>
<span data-ttu-id="3f20f-134">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="3f20f-135">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="3f20f-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-136">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="3f20f-136">-Overprovision</span></span>
<span data-ttu-id="3f20f-137">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="3f20f-138">-PlanName</span></span>
<span data-ttu-id="3f20f-139">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-139">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="3f20f-140">-PlanProduct</span></span>
<span data-ttu-id="3f20f-141">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-141">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="3f20f-142">-PlanPromotionCode</span></span>
<span data-ttu-id="3f20f-143">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-143">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="3f20f-144">-PlanPublisher</span></span>
<span data-ttu-id="3f20f-145">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="3f20f-145">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="3f20f-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="3f20f-147">Określ zasady odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f20f-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3f20f-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="3f20f-149">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="3f20f-149">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3f20f-150">-SkuCapacity</span></span>
<span data-ttu-id="3f20f-151">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3f20f-152">-SkuName</span></span>
<span data-ttu-id="3f20f-153">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-153">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3f20f-154">-SkuTier</span></span>
<span data-ttu-id="3f20f-155">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="3f20f-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3f20f-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f20f-157">Standard</span><span class="sxs-lookup"><span data-stu-id="3f20f-157">Standard</span></span>
- <span data-ttu-id="3f20f-158">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3f20f-158">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-159">-StorageProfile</span></span>
<span data-ttu-id="3f20f-160">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="3f20f-161">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="3f20f-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f20f-162">-Tag</span></span>
<span data-ttu-id="3f20f-163">Określa Tagi, które zostaną przydzielone do VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f20f-163">Specifies the tags that will be assigned to the VMSS.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="3f20f-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="3f20f-165">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3f20f-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="3f20f-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3f20f-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f20f-167">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="3f20f-167">Automatic</span></span>
- <span data-ttu-id="3f20f-168">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="3f20f-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f20f-169">-Confirm</span></span>
<span data-ttu-id="3f20f-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f20f-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f20f-171">-WhatIf</span></span>
<span data-ttu-id="3f20f-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f20f-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f20f-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f20f-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f20f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f20f-174">CommonParameters</span></span>
<span data-ttu-id="3f20f-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f20f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f20f-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f20f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f20f-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f20f-177">INPUTS</span></span>

### <span data-ttu-id="3f20f-178">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f20f-178">None</span></span>
<span data-ttu-id="3f20f-179">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3f20f-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f20f-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f20f-180">OUTPUTS</span></span>

### <span data-ttu-id="3f20f-181">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3f20f-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3f20f-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f20f-182">NOTES</span></span>

## <span data-ttu-id="3f20f-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f20f-183">RELATED LINKS</span></span>

[<span data-ttu-id="3f20f-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="3f20f-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="3f20f-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="3f20f-186">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f20f-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="3f20f-187">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3f20f-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="3f20f-188">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3f20f-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


