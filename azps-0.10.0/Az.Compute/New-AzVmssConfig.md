---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893605"
---
# <span data-ttu-id="c08c1-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c08c1-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="c08c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c08c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c08c1-103">Tworzy obiekt konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="c08c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c08c1-104">SYNTAX</span></span>

### <span data-ttu-id="c08c1-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c08c1-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08c1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c08c1-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08c1-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c08c1-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c08c1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c08c1-108">DESCRIPTION</span></span>
<span data-ttu-id="c08c1-109">Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c08c1-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="c08c1-110">Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c08c1-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="c08c1-111">Te polecenia cmdlet są następujące:</span><span class="sxs-lookup"><span data-stu-id="c08c1-111">These cmdlets are:</span></span>

- <span data-ttu-id="c08c1-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="c08c1-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="c08c1-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c08c1-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="c08c1-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c08c1-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="c08c1-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c08c1-116">EXAMPLES</span></span>

### <span data-ttu-id="c08c1-117">Przykład 1. Tworzenie obiektu konfiguracji VMSS</span><span class="sxs-lookup"><span data-stu-id="c08c1-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="c08c1-118">W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="c08c1-119">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="c08c1-120">W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="c08c1-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c08c1-121">PARAMETERS</span></span>

### <span data-ttu-id="c08c1-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c08c1-122">-AssignIdentity</span></span>
<span data-ttu-id="c08c1-123">Określ tożsamość przypisanego systemu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c08c1-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="c08c1-125">Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="c08c1-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c08c1-126">-BootDiagnostic</span></span>
<span data-ttu-id="c08c1-127">Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="c08c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-128">-DefaultProfile</span></span>
<span data-ttu-id="c08c1-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c08c1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c08c1-130">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="c08c1-130">-Extension</span></span>
<span data-ttu-id="c08c1-131">Określa obiekt informacji o rozszerzeniu dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="c08c1-132">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="c08c1-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="c08c1-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="c08c1-133">-HealthProbeId</span></span>
<span data-ttu-id="c08c1-134">Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="c08c1-135">HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="c08c1-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="c08c1-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c08c1-136">-IdentityId</span></span>
<span data-ttu-id="c08c1-137">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c08c1-138">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="c08c1-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c08c1-139">-IdentityType</span></span>
<span data-ttu-id="c08c1-140">Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="c08c1-141">Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c08c1-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="c08c1-142">Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="c08c1-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c08c1-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c08c1-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c08c1-144">SystemAssigned</span></span>
- <span data-ttu-id="c08c1-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c08c1-145">UserAssigned</span></span>
- <span data-ttu-id="c08c1-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="c08c1-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="c08c1-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c08c1-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c08c1-148">-LicenseType</span></span>
<span data-ttu-id="c08c1-149">Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="c08c1-149">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="c08c1-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c08c1-150">-Location</span></span>
<span data-ttu-id="c08c1-151">Określa lokalizację platformy Azure, w której jest tworzony VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-151">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="c08c1-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c08c1-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="c08c1-153">Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="c08c1-154">Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="c08c1-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="c08c1-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-155">-OsProfile</span></span>
<span data-ttu-id="c08c1-156">Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="c08c1-157">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="c08c1-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="c08c1-158">-Przekazanie</span><span class="sxs-lookup"><span data-stu-id="c08c1-158">-Overprovision</span></span>
<span data-ttu-id="c08c1-159">Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="c08c1-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c08c1-160">-PlanName</span></span>
<span data-ttu-id="c08c1-161">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-161">Specifies the plan name.</span></span>

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

### <span data-ttu-id="c08c1-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c08c1-162">-PlanProduct</span></span>
<span data-ttu-id="c08c1-163">Określa plan produktu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-163">Specifies the plan product.</span></span>

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

### <span data-ttu-id="c08c1-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c08c1-164">-PlanPromotionCode</span></span>
<span data-ttu-id="c08c1-165">Umożliwia określenie kodu promocyjnego planu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-165">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="c08c1-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c08c1-166">-PlanPublisher</span></span>
<span data-ttu-id="c08c1-167">Umożliwia określenie wydawcy planu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-167">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="c08c1-168">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="c08c1-168">-Priority</span></span>
<span data-ttu-id="c08c1-169">Określa priorytet maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="c08c1-169">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="c08c1-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="c08c1-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="c08c1-171">Określa zasady uaktualnienia stopniowego.</span><span class="sxs-lookup"><span data-stu-id="c08c1-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c08c1-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="c08c1-173">Umożliwia określenie pojedynczej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="c08c1-173">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="c08c1-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c08c1-174">-SkuCapacity</span></span>
<span data-ttu-id="c08c1-175">Określa liczbę wystąpień w VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c08c1-176">-SkuName</span></span>
<span data-ttu-id="c08c1-177">Określa rozmiar wszystkich wystąpień VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-177">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="c08c1-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c08c1-178">-SkuTier</span></span>
<span data-ttu-id="c08c1-179">Określa poziom VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="c08c1-180">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c08c1-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c08c1-181">Standard</span><span class="sxs-lookup"><span data-stu-id="c08c1-181">Standard</span></span>
- <span data-ttu-id="c08c1-182">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="c08c1-182">Basic</span></span>

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

### <span data-ttu-id="c08c1-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-183">-StorageProfile</span></span>
<span data-ttu-id="c08c1-184">Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.</span><span class="sxs-lookup"><span data-stu-id="c08c1-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="c08c1-185">Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="c08c1-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="c08c1-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="c08c1-186">-Tag</span></span>
<span data-ttu-id="c08c1-187">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c08c1-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c08c1-188">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c08c1-188">For example:</span></span>

<span data-ttu-id="c08c1-189">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="c08c1-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c08c1-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c08c1-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="c08c1-191">W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c08c1-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="c08c1-192">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c08c1-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c08c1-193">Automatyczne</span><span class="sxs-lookup"><span data-stu-id="c08c1-193">Automatic</span></span>
- <span data-ttu-id="c08c1-194">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="c08c1-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="c08c1-195">-Zone</span></span>
<span data-ttu-id="c08c1-196">Określa listę stref dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c08c1-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08c1-197">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c08c1-197">-Confirm</span></span>
<span data-ttu-id="c08c1-198">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c08c1-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08c1-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08c1-199">-WhatIf</span></span>
<span data-ttu-id="c08c1-200">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c08c1-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c08c1-201">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c08c1-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08c1-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08c1-202">CommonParameters</span></span>
<span data-ttu-id="c08c1-203">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c08c1-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08c1-204">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08c1-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08c1-205">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c08c1-205">INPUTS</span></span>

### <span data-ttu-id="c08c1-206">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c08c1-206">None</span></span>
<span data-ttu-id="c08c1-207">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c08c1-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c08c1-208">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c08c1-208">OUTPUTS</span></span>

### <span data-ttu-id="c08c1-209">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c08c1-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c08c1-210">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c08c1-210">NOTES</span></span>

## <span data-ttu-id="c08c1-211">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c08c1-211">RELATED LINKS</span></span>

[<span data-ttu-id="c08c1-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="c08c1-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c08c1-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="c08c1-214">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c08c1-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c08c1-215">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c08c1-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="c08c1-216">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="c08c1-216">New-AzVmss</span></span>](./New-AzVmss.md)
