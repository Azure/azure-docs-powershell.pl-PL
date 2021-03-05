---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991495"
---
# <span data-ttu-id="b4153-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b4153-101">New-AzVMConfig</span></span>

## <span data-ttu-id="b4153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4153-102">SYNOPSIS</span></span>
<span data-ttu-id="b4153-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="b4153-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4153-104">SYNTAX</span></span>

### <span data-ttu-id="b4153-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4153-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4153-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4153-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4153-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4153-107">DESCRIPTION</span></span>
<span data-ttu-id="b4153-108">Polecenie **cmdlet New-AzVMConfig** tworzy konfigurowalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4153-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="b4153-109">Inne polecenia cmdlet mogą być używane do konfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSSystem.</span><span class="sxs-lookup"><span data-stu-id="b4153-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="b4153-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4153-110">EXAMPLES</span></span>

### <span data-ttu-id="b4153-111">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b4153-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="b4153-112">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4153-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b4153-113">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="b4153-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b4153-114">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b4153-115">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="b4153-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="b4153-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4153-116">PARAMETERS</span></span>

### <span data-ttu-id="b4153-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="b4153-117">-AvailabilitySetId</span></span>
<span data-ttu-id="b4153-118">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="b4153-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="b4153-119">Aby uzyskać obiekt zestawu dostępności, użyj Get-AzAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4153-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="b4153-120">Obiekt zestawu dostępności zawiera właściwość Identyfikator.</span><span class="sxs-lookup"><span data-stu-id="b4153-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="b4153-121">Maszyny wirtualne określone w tym samym zestawie dostępności są przydzielane do różnych węzłów w celu zmaksymalizowania dostępności.</span><span class="sxs-lookup"><span data-stu-id="b4153-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="b4153-122">Aby uzyskać więcej informacji na temat zestawów dostępności, zobacz [Zarządzanie dostępnością maszyn wirtualnych.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="b4153-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="b4153-123">Aby uzyskać więcej informacji na temat planowanej konserwacji platformy Azure, zobacz [Planowane konserwacje maszyn wirtualnych na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="b4153-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="b4153-124">Obecnie maszyny wirtualnej można dodać tylko do zestawu dostępności podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="b4153-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="b4153-125">Zestaw dostępności, do którego jest dodawana maszyny wirtualnej, powinien być w tej samej grupie zasobów, do której jest dodawany zasób zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="b4153-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="b4153-126">Istniejącej maszyny wirtualnej nie można dodać do zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="b4153-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="b4153-127">Ta właściwość nie może istnieć wraz z odwołaniem do właściwości innych niż null.virtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="b4153-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="b4153-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4153-128">-DefaultProfile</span></span>
<span data-ttu-id="b4153-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4153-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4153-130">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="b4153-130">-EnableUltraSSD</span></span>
<span data-ttu-id="b4153-131">Umożliwia możliwość, że jedna lub więcej zarządzanych dysków danych UltraSSD_LRS typ konta magazynu w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="b4153-132">Dysk zarządzany z kontem magazynu typu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b4153-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="b4153-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4153-133">-EvictionPolicy</span></span>
<span data-ttu-id="b4153-134">Zasady eksmisji dla maszyny wirtualnej usługi Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="b4153-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="b4153-135">Obsługiwane wartości to "Deallocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="b4153-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="b4153-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="b4153-136">-HostId</span></span>
<span data-ttu-id="b4153-137">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="b4153-137">The Id of Host</span></span>

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

### <span data-ttu-id="b4153-138">- IdentityId</span><span class="sxs-lookup"><span data-stu-id="b4153-138">-IdentityId</span></span>
<span data-ttu-id="b4153-139">Określa listę tożsamości użytkowników skojarzonych z zestawem skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b4153-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="b4153-140">Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="b4153-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b4153-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b4153-141">-IdentityType</span></span>
<span data-ttu-id="b4153-142">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="b4153-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="b4153-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b4153-143">-LicenseType</span></span>
<span data-ttu-id="b4153-144">Określa typ licencji, który wskazuje, że obraz lub dysk maszyny wirtualnej został licencjonowany lokalnie.</span><span class="sxs-lookup"><span data-stu-id="b4153-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="b4153-145">Możliwe wartości dla systemu Windows Server to:</span><span class="sxs-lookup"><span data-stu-id="b4153-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="b4153-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b4153-146">Windows_Client</span></span>
- <span data-ttu-id="b4153-147">Windows_Server możliwe wartości dla systemu operacyjnego Linux Server to:</span><span class="sxs-lookup"><span data-stu-id="b4153-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="b4153-148">RHEL_BYOS (dla RBLOCK)</span><span class="sxs-lookup"><span data-stu-id="b4153-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="b4153-149">SLES_BYOS (dla SUSE)</span><span class="sxs-lookup"><span data-stu-id="b4153-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="b4153-150">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="b4153-150">-MaxPrice</span></span>
<span data-ttu-id="b4153-151">Określa maksymalną cenę za niską płatność za maszyny wirtualne/maszyny wirtualne o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b4153-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="b4153-152">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="b4153-152">This price is in US Dollars.</span></span> <span data-ttu-id="b4153-153">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="b4153-154">Ponadto ceny są porównywane w czasie tworzenia/aktualizacji maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż obecna cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b4153-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="b4153-155">Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, jeśli bieżąca cena o niskim priorytecie przekracza wartość maxCena po utworzeniu maszyny wirtualnej/maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="b4153-156">Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="b4153-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="b4153-157">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="b4153-157">Example: 0.01538.</span></span>  <span data-ttu-id="b4153-158">-1 oznacza, że maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie nie należy ich ujednać ze względu na cenę.</span><span class="sxs-lookup"><span data-stu-id="b4153-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="b4153-159">Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.</span><span class="sxs-lookup"><span data-stu-id="b4153-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="b4153-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="b4153-160">-EncryptionAtHost</span></span>
<span data-ttu-id="b4153-161">Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="b4153-162">Spowoduje to włączenie szyfrowania dla wszystkich dysków, w tym dysku zasobu/tempa na samym hoście.</span><span class="sxs-lookup"><span data-stu-id="b4153-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="b4153-163">Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="b4153-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="b4153-164">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b4153-164">-Priority</span></span>
<span data-ttu-id="b4153-165">Priorytet maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="b4153-166">Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".</span><span class="sxs-lookup"><span data-stu-id="b4153-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="b4153-167">"Zwykła" jest dla zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="b4153-168">"Spot" jest dla maszyny wirtualnej spot.</span><span class="sxs-lookup"><span data-stu-id="b4153-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="b4153-169">"Low" jest również dla spot virtual machine, ale jest zastępowany przez "Spot".</span><span class="sxs-lookup"><span data-stu-id="b4153-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="b4153-170">Użyj pozycji Spot (Spot) zamiast "Low" (Najniszej).</span><span class="sxs-lookup"><span data-stu-id="b4153-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="b4153-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b4153-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="b4153-172">Identyfikator zasobu grupy Położenie odległości, która ma być używania z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="b4153-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="b4153-173">— Tagi</span><span class="sxs-lookup"><span data-stu-id="b4153-173">-Tags</span></span>
<span data-ttu-id="b4153-174">Tagi dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4153-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="b4153-175">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="b4153-175">-VMName</span></span>
<span data-ttu-id="b4153-176">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="b4153-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="b4153-177">-VMSize</span></span>
<span data-ttu-id="b4153-178">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="b4153-179">- Maszyny wirtualne</span><span class="sxs-lookup"><span data-stu-id="b4153-179">-VmssId</span></span>
<span data-ttu-id="b4153-180">Identyfikator zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b4153-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="b4153-181">— Strefa</span><span class="sxs-lookup"><span data-stu-id="b4153-181">-Zone</span></span>
<span data-ttu-id="b4153-182">Określa listę stref dostępności dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4153-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="b4153-183">Dozwolone wartości zależą od możliwości regionu.</span><span class="sxs-lookup"><span data-stu-id="b4153-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="b4153-184">Dozwolone wartości zwykle to 1;2;3.</span><span class="sxs-lookup"><span data-stu-id="b4153-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="b4153-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4153-185">CommonParameters</span></span>
<span data-ttu-id="b4153-186">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4153-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4153-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4153-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4153-188">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4153-188">INPUTS</span></span>

### <span data-ttu-id="b4153-189">System.String</span><span class="sxs-lookup"><span data-stu-id="b4153-189">System.String</span></span>

### <span data-ttu-id="b4153-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b4153-190">System.String[]</span></span>

### <span data-ttu-id="b4153-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4153-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b4153-192">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="b4153-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4153-193">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4153-193">OUTPUTS</span></span>

### <span data-ttu-id="b4153-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4153-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b4153-195">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4153-195">NOTES</span></span>

## <span data-ttu-id="b4153-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4153-196">RELATED LINKS</span></span>

[<span data-ttu-id="b4153-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4153-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="b4153-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b4153-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="b4153-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="b4153-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="b4153-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b4153-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


