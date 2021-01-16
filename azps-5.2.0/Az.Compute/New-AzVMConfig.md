---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352033"
---
# <span data-ttu-id="2edf5-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2edf5-101">New-AzVMConfig</span></span>

## <span data-ttu-id="2edf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2edf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2edf5-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="2edf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2edf5-104">SYNTAX</span></span>

### <span data-ttu-id="2edf5-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2edf5-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edf5-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2edf5-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2edf5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2edf5-107">DESCRIPTION</span></span>
<span data-ttu-id="2edf5-108">Polecenie cmdlet **New-AzVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2edf5-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="2edf5-109">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="2edf5-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="2edf5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2edf5-110">EXAMPLES</span></span>

### <span data-ttu-id="2edf5-111">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2edf5-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="2edf5-112">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2edf5-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2edf5-113">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2edf5-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2edf5-114">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2edf5-115">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2edf5-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="2edf5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2edf5-116">PARAMETERS</span></span>

### <span data-ttu-id="2edf5-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="2edf5-117">-AvailabilitySetId</span></span>
<span data-ttu-id="2edf5-118">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="2edf5-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="2edf5-119">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2edf5-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="2edf5-120">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="2edf5-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="2edf5-121">Maszyny wirtualne określone w tym samym zbiorze dostępności są przydzielane do różnych węzłów, aby zmaksymalizować dostępność.</span><span class="sxs-lookup"><span data-stu-id="2edf5-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="2edf5-122">Aby uzyskać więcej informacji na temat zestawów dostępności, zobacz [Zarządzanie dostępnością maszyn wirtualnych](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="2edf5-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="2edf5-123">Aby uzyskać więcej informacji na temat planowanej konserwacji platformy Azure, zobacz [Planowana konserwacja maszyn wirtualnych na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="2edf5-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="2edf5-124">Obecnie maszyna wirtualna może być dodana do zestawu dostępności tylko w czasie tworzenia.</span><span class="sxs-lookup"><span data-stu-id="2edf5-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="2edf5-125">Zestaw dostępności, do którego jest dodawana maszyna wirtualna, powinien znajdować się w tej samej grupie zasobów co zasób zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="2edf5-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="2edf5-126">Istniejącej maszyny wirtualnej nie można dodać do zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="2edf5-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="2edf5-127">Ta właściwość nie może istnieć wraz z właściwościami innymi niż null. virtualMachineScaleSet, odwołanie.</span><span class="sxs-lookup"><span data-stu-id="2edf5-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="2edf5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edf5-128">-DefaultProfile</span></span>
<span data-ttu-id="2edf5-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2edf5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edf5-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="2edf5-130">-EnableUltraSSD</span></span>
<span data-ttu-id="2edf5-131">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="2edf5-132">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="2edf5-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="2edf5-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="2edf5-133">-EvictionPolicy</span></span>
<span data-ttu-id="2edf5-134">Zasady wykluczenia dla maszyny wirtualnej Azure spot.</span><span class="sxs-lookup"><span data-stu-id="2edf5-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="2edf5-135">Obsługiwane wartości to "allocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="2edf5-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="2edf5-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="2edf5-136">-HostId</span></span>
<span data-ttu-id="2edf5-137">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="2edf5-137">The Id of Host</span></span>

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

### <span data-ttu-id="2edf5-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2edf5-138">-IdentityId</span></span>
<span data-ttu-id="2edf5-139">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2edf5-140">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="2edf5-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2edf5-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2edf5-141">-IdentityType</span></span>
<span data-ttu-id="2edf5-142">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="2edf5-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="2edf5-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2edf5-143">-LicenseType</span></span>
<span data-ttu-id="2edf5-144">Określa typ licencji wskazujący, że obraz lub dysk maszyny wirtualnej jest licencjonowany lokalnie.</span><span class="sxs-lookup"><span data-stu-id="2edf5-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="2edf5-145">Możliwe wartości dla systemu Windows Server są następujące:</span><span class="sxs-lookup"><span data-stu-id="2edf5-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="2edf5-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="2edf5-146">Windows_Client</span></span>
- <span data-ttu-id="2edf5-147">Windows_Server możliwych wartości dla systemu operacyjnego serwera Linux są następujące:</span><span class="sxs-lookup"><span data-stu-id="2edf5-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="2edf5-148">RHEL_BYOS (dla RHEL)</span><span class="sxs-lookup"><span data-stu-id="2edf5-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="2edf5-149">SLES_BYOS (dla SUSE)</span><span class="sxs-lookup"><span data-stu-id="2edf5-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="2edf5-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="2edf5-150">-MaxPrice</span></span>
<span data-ttu-id="2edf5-151">Określa cenę maksymalną, jaką można zapłacić za niski priorytet maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="2edf5-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="2edf5-152">Ta cena jest w dolarach amerykańskich.</span><span class="sxs-lookup"><span data-stu-id="2edf5-152">This price is in US Dollars.</span></span> <span data-ttu-id="2edf5-153">Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="2edf5-154">Ceny są również porównywane w czasie tworzenia/aktualizowania o niskim priorytecie maszyny wirtualnej/VMSS, a operacja będzie dostępna tylko wtedy, gdy maxPrice jest większa niż bieżąca cena o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="2edf5-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="2edf5-155">MaxPrice będzie również stosowany do wykluczania niewielkiego priorytetu maszyn wirtualnych/VMSS, jeśli obecna cena o niskim priorytecie wykracza poza maxPrice po utworzeniu maszyny wirtualnej/VMSS.</span><span class="sxs-lookup"><span data-stu-id="2edf5-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="2edf5-156">Możliwe wartości: Każda wartość dziesiętna większa niż zero.</span><span class="sxs-lookup"><span data-stu-id="2edf5-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="2edf5-157">Przykład: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="2edf5-157">Example: 0.01538.</span></span>  <span data-ttu-id="2edf5-158">-1 wskazuje, że nie można wykluczyć niskiego priorytetu maszyn wirtualnych/VMSS w celu uzyskania podstawy cenowej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="2edf5-159">Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="2edf5-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="2edf5-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="2edf5-160">-EncryptionAtHost</span></span>
<span data-ttu-id="2edf5-161">Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu do włączania lub wyłączania szyfrowania hosta dla maszyny wirtualnej lub zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="2edf5-162">Spowoduje to włączenie szyfrowania wszystkich dysków, w tym dysku Resource/temp, na hoście.</span><span class="sxs-lookup"><span data-stu-id="2edf5-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="2edf5-163">Wartość domyślna: szyfrowanie na hoście zostanie wyłączone, chyba że dla tego zasobu zostanie ustawiona wartość true dla tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="2edf5-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="2edf5-164">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="2edf5-164">-Priority</span></span>
<span data-ttu-id="2edf5-165">Priorytet maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="2edf5-166">Obsługiwane są tylko wartości "Regular", "spot" i "Low".</span><span class="sxs-lookup"><span data-stu-id="2edf5-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="2edf5-167">"Zwykła" dotyczy zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="2edf5-168">"Miejsce na maszynie wirtualnej" jest na miejscu.</span><span class="sxs-lookup"><span data-stu-id="2edf5-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="2edf5-169">"Niski" jest również na odniesieniu do maszyny wirtualnej, ale został zastąpiony przez "punkt".</span><span class="sxs-lookup"><span data-stu-id="2edf5-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="2edf5-170">Użyj "spot" zamiast "niski".</span><span class="sxs-lookup"><span data-stu-id="2edf5-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="2edf5-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="2edf5-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="2edf5-172">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2edf5-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="2edf5-173">-Tagi</span><span class="sxs-lookup"><span data-stu-id="2edf5-173">-Tags</span></span>
<span data-ttu-id="2edf5-174">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="2edf5-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="2edf5-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="2edf5-175">-VMName</span></span>
<span data-ttu-id="2edf5-176">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="2edf5-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="2edf5-177">-VMSize</span></span>
<span data-ttu-id="2edf5-178">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="2edf5-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="2edf5-179">-VmssId</span></span>
<span data-ttu-id="2edf5-180">Identyfikator zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2edf5-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="2edf5-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="2edf5-181">-Zone</span></span>
<span data-ttu-id="2edf5-182">Określa listę stref dostępności dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2edf5-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="2edf5-183">Dozwolone wartości są zależne od możliwości obszaru tego regionu.</span><span class="sxs-lookup"><span data-stu-id="2edf5-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="2edf5-184">Dozwolone wartości będą zwykle 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="2edf5-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="2edf5-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edf5-185">CommonParameters</span></span>
<span data-ttu-id="2edf5-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edf5-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edf5-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2edf5-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edf5-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2edf5-188">INPUTS</span></span>

### <span data-ttu-id="2edf5-189">System. String</span><span class="sxs-lookup"><span data-stu-id="2edf5-189">System.String</span></span>

### <span data-ttu-id="2edf5-190">System. String []</span><span class="sxs-lookup"><span data-stu-id="2edf5-190">System.String[]</span></span>

### <span data-ttu-id="2edf5-191">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2edf5-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2edf5-192">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2edf5-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2edf5-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2edf5-193">OUTPUTS</span></span>

### <span data-ttu-id="2edf5-194">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2edf5-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2edf5-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2edf5-195">NOTES</span></span>

## <span data-ttu-id="2edf5-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2edf5-196">RELATED LINKS</span></span>

[<span data-ttu-id="2edf5-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2edf5-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="2edf5-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2edf5-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="2edf5-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="2edf5-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="2edf5-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2edf5-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


