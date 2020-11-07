---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719042"
---
# <span data-ttu-id="24e1b-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="24e1b-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="24e1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="24e1b-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24e1b-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="24e1b-106">Polecenie cmdlet **New-AzureRmVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="24e1b-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="24e1b-107">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e1b-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="24e1b-108">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="24e1b-108">These cmdlets are:</span></span>

- <span data-ttu-id="24e1b-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="24e1b-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="24e1b-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="24e1b-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="24e1b-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24e1b-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="24e1b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24e1b-113">EXAMPLES</span></span>

### <span data-ttu-id="24e1b-114">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="24e1b-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="24e1b-115">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="24e1b-116">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="24e1b-117">W drugim poleceniu użyto polecenia cmdlet **New-AzureRmVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="24e1b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24e1b-118">PARAMETERS</span></span>

### <span data-ttu-id="24e1b-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="24e1b-119">-AssignIdentity</span></span>
<span data-ttu-id="24e1b-120">Określ tożsamość przypisanego systemu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="24e1b-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e1b-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="24e1b-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="24e1b-122">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e1b-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="24e1b-123">-BootDiagnostic</span></span>
<span data-ttu-id="24e1b-124">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="24e1b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-125">-DefaultProfile</span></span>
<span data-ttu-id="24e1b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24e1b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24e1b-127">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="24e1b-127">-Extension</span></span>
<span data-ttu-id="24e1b-128">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="24e1b-129">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="24e1b-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="24e1b-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="24e1b-130">-HealthProbeId</span></span>
<span data-ttu-id="24e1b-131">Określ identyfikator sondy modułu równoważenia obciążenia użytego do określenia kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="24e1b-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="24e1b-132">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="24e1b-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="24e1b-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="24e1b-133">-IdentityType</span></span>
<span data-ttu-id="24e1b-134">Określ tożsamość zestawu skali maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="24e1b-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e1b-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="24e1b-135">-LicenseType</span></span>
<span data-ttu-id="24e1b-136">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="24e1b-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="24e1b-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="24e1b-137">-Location</span></span>
<span data-ttu-id="24e1b-138">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="24e1b-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="24e1b-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="24e1b-140">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="24e1b-141">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="24e1b-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="24e1b-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-142">-OsProfile</span></span>
<span data-ttu-id="24e1b-143">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="24e1b-144">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="24e1b-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="24e1b-145">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="24e1b-145">-Overprovision</span></span>
<span data-ttu-id="24e1b-146">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="24e1b-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="24e1b-147">-PlanName</span></span>
<span data-ttu-id="24e1b-148">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="24e1b-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="24e1b-149">-PlanProduct</span></span>
<span data-ttu-id="24e1b-150">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="24e1b-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="24e1b-151">-PlanPromotionCode</span></span>
<span data-ttu-id="24e1b-152">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="24e1b-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="24e1b-153">-PlanPublisher</span></span>
<span data-ttu-id="24e1b-154">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="24e1b-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="24e1b-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="24e1b-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="24e1b-156">Określ zasady odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="24e1b-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e1b-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="24e1b-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="24e1b-158">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="24e1b-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="24e1b-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="24e1b-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="24e1b-160">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="24e1b-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="24e1b-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="24e1b-161">-SkuCapacity</span></span>
<span data-ttu-id="24e1b-162">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e1b-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="24e1b-163">-SkuName</span></span>
<span data-ttu-id="24e1b-164">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="24e1b-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="24e1b-165">-SkuTier</span></span>
<span data-ttu-id="24e1b-166">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="24e1b-167">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="24e1b-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24e1b-168">Standard</span><span class="sxs-lookup"><span data-stu-id="24e1b-168">Standard</span></span>
- <span data-ttu-id="24e1b-169">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="24e1b-169">Basic</span></span>

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

### <span data-ttu-id="24e1b-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-170">-StorageProfile</span></span>
<span data-ttu-id="24e1b-171">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="24e1b-172">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="24e1b-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="24e1b-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="24e1b-173">-Tag</span></span>
<span data-ttu-id="24e1b-174">Określa Tagi, które zostaną przydzielone do VMSS.</span><span class="sxs-lookup"><span data-stu-id="24e1b-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="24e1b-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="24e1b-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="24e1b-176">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="24e1b-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="24e1b-177">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="24e1b-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24e1b-178">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="24e1b-178">Automatic</span></span>
- <span data-ttu-id="24e1b-179">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="24e1b-179">Manual</span></span>

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

### <span data-ttu-id="24e1b-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="24e1b-180">-Zone</span></span>
<span data-ttu-id="24e1b-181">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="24e1b-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="24e1b-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24e1b-182">-Confirm</span></span>
<span data-ttu-id="24e1b-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e1b-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e1b-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e1b-184">-WhatIf</span></span>
<span data-ttu-id="24e1b-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e1b-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24e1b-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24e1b-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e1b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e1b-187">CommonParameters</span></span>
<span data-ttu-id="24e1b-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e1b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e1b-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e1b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e1b-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e1b-190">INPUTS</span></span>

## <span data-ttu-id="24e1b-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24e1b-191">OUTPUTS</span></span>

### <span data-ttu-id="24e1b-192">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="24e1b-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="24e1b-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24e1b-193">NOTES</span></span>

## <span data-ttu-id="24e1b-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24e1b-194">RELATED LINKS</span></span>

[<span data-ttu-id="24e1b-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="24e1b-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="24e1b-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="24e1b-197">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="24e1b-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="24e1b-198">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24e1b-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="24e1b-199">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24e1b-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


