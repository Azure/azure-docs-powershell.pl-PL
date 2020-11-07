---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 5dda2e33496e3391d55e7be20348fef681bc22b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706322"
---
# <span data-ttu-id="90bf7-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="90bf7-101">New-AzVMConfig</span></span>

## <span data-ttu-id="90bf7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="90bf7-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="90bf7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90bf7-104">SYNTAX</span></span>

### <span data-ttu-id="90bf7-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90bf7-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90bf7-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="90bf7-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90bf7-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="90bf7-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90bf7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="90bf7-108">DESCRIPTION</span></span>
<span data-ttu-id="90bf7-109">Polecenie cmdlet **New-AzVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90bf7-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="90bf7-110">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="90bf7-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="90bf7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90bf7-111">EXAMPLES</span></span>

### <span data-ttu-id="90bf7-112">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="90bf7-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="90bf7-113">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="90bf7-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="90bf7-114">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="90bf7-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="90bf7-115">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="90bf7-116">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="90bf7-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="90bf7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90bf7-117">PARAMETERS</span></span>

### <span data-ttu-id="90bf7-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="90bf7-118">-AssignIdentity</span></span>
<span data-ttu-id="90bf7-119">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="90bf7-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="90bf7-120">-AvailabilitySetId</span></span>
<span data-ttu-id="90bf7-121">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="90bf7-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="90bf7-122">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="90bf7-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="90bf7-123">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="90bf7-123">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bf7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bf7-124">-DefaultProfile</span></span>
<span data-ttu-id="90bf7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90bf7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90bf7-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="90bf7-126">-EnableUltraSSD</span></span>
<span data-ttu-id="90bf7-127">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="90bf7-128">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="90bf7-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="90bf7-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="90bf7-129">-EvictionPolicy</span></span>
<span data-ttu-id="90bf7-130">Zasady wykluczenia dla maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="90bf7-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="90bf7-131">Jedyną obsługiwaną wartością jest "deallocate".</span><span class="sxs-lookup"><span data-stu-id="90bf7-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="90bf7-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="90bf7-132">-HostId</span></span>
<span data-ttu-id="90bf7-133">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="90bf7-133">The Id of Host</span></span>

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

### <span data-ttu-id="90bf7-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="90bf7-134">-IdentityId</span></span>
<span data-ttu-id="90bf7-135">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="90bf7-136">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="90bf7-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="90bf7-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="90bf7-137">-IdentityType</span></span>
<span data-ttu-id="90bf7-138">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="90bf7-138">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bf7-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="90bf7-139">-LicenseType</span></span>
<span data-ttu-id="90bf7-140">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="90bf7-140">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bf7-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="90bf7-141">-MaxPrice</span></span>
<span data-ttu-id="90bf7-142">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="90bf7-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="90bf7-143">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="90bf7-143">This price is in US Dollars.</span></span> <span data-ttu-id="90bf7-144">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="90bf7-145">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="90bf7-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="90bf7-146">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="90bf7-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="90bf7-147">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="90bf7-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="90bf7-148">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="90bf7-148">Example: 0.01538.</span></span>  <span data-ttu-id="90bf7-149">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="90bf7-150">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="90bf7-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="90bf7-151">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="90bf7-151">-Priority</span></span>
<span data-ttu-id="90bf7-152">Priorytet maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="90bf7-153">Obsługiwane są tylko wartości "zwykła" i "niskie".</span><span class="sxs-lookup"><span data-stu-id="90bf7-153">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="90bf7-154">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="90bf7-154">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="90bf7-155">Identyfikator ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="90bf7-155">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="90bf7-156">-Tagi</span><span class="sxs-lookup"><span data-stu-id="90bf7-156">-Tags</span></span>
<span data-ttu-id="90bf7-157">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="90bf7-157">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bf7-158">-VMName</span><span class="sxs-lookup"><span data-stu-id="90bf7-158">-VMName</span></span>
<span data-ttu-id="90bf7-159">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-159">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bf7-160">-VMSize</span><span class="sxs-lookup"><span data-stu-id="90bf7-160">-VMSize</span></span>
<span data-ttu-id="90bf7-161">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-161">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="90bf7-162">-VmssId</span><span class="sxs-lookup"><span data-stu-id="90bf7-162">-VmssId</span></span>
<span data-ttu-id="90bf7-163">Identyfikator zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="90bf7-163">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="90bf7-164">-Zone</span><span class="sxs-lookup"><span data-stu-id="90bf7-164">-Zone</span></span>
<span data-ttu-id="90bf7-165">Określa listę stref dostępności dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90bf7-165">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="90bf7-166">Dozwolone wartości są zależne od możliwości obszaru tego regionu.</span><span class="sxs-lookup"><span data-stu-id="90bf7-166">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="90bf7-167">Dozwolone wartości będą zwykle 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="90bf7-167">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="90bf7-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bf7-168">CommonParameters</span></span>
<span data-ttu-id="90bf7-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90bf7-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bf7-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90bf7-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bf7-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90bf7-171">INPUTS</span></span>

### <span data-ttu-id="90bf7-172">System. String</span><span class="sxs-lookup"><span data-stu-id="90bf7-172">System.String</span></span>

### <span data-ttu-id="90bf7-173">System. String []</span><span class="sxs-lookup"><span data-stu-id="90bf7-173">System.String[]</span></span>

### <span data-ttu-id="90bf7-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90bf7-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="90bf7-175">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90bf7-175">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90bf7-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90bf7-176">OUTPUTS</span></span>

### <span data-ttu-id="90bf7-177">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="90bf7-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="90bf7-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90bf7-178">NOTES</span></span>

## <span data-ttu-id="90bf7-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90bf7-179">RELATED LINKS</span></span>

[<span data-ttu-id="90bf7-180">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="90bf7-180">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="90bf7-181">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="90bf7-181">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="90bf7-182">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="90bf7-182">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="90bf7-183">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90bf7-183">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


