---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710272"
---
# <span data-ttu-id="84159-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="84159-101">New-AzVMConfig</span></span>

## <span data-ttu-id="84159-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84159-102">SYNOPSIS</span></span>
<span data-ttu-id="84159-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="84159-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84159-104">SYNTAX</span></span>

### <span data-ttu-id="84159-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84159-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84159-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="84159-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84159-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="84159-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84159-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84159-108">DESCRIPTION</span></span>
<span data-ttu-id="84159-109">Polecenie cmdlet **New-AzVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="84159-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="84159-110">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="84159-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="84159-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84159-111">EXAMPLES</span></span>

### <span data-ttu-id="84159-112">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="84159-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="84159-113">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="84159-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="84159-114">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="84159-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="84159-115">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="84159-116">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="84159-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="84159-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84159-117">PARAMETERS</span></span>

### <span data-ttu-id="84159-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="84159-118">-AssignIdentity</span></span>
<span data-ttu-id="84159-119">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="84159-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="84159-120">-AvailabilitySetId</span></span>
<span data-ttu-id="84159-121">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="84159-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="84159-122">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="84159-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="84159-123">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="84159-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="84159-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84159-124">-DefaultProfile</span></span>
<span data-ttu-id="84159-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84159-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84159-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="84159-126">-EnableUltraSSD</span></span>
<span data-ttu-id="84159-127">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="84159-128">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="84159-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="84159-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="84159-129">-IdentityId</span></span>
<span data-ttu-id="84159-130">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="84159-131">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="84159-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="84159-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="84159-132">-IdentityType</span></span>
<span data-ttu-id="84159-133">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="84159-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="84159-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="84159-134">-LicenseType</span></span>
<span data-ttu-id="84159-135">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="84159-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="84159-136">-Tagi</span><span class="sxs-lookup"><span data-stu-id="84159-136">-Tags</span></span>
<span data-ttu-id="84159-137">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="84159-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="84159-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="84159-138">-VMName</span></span>
<span data-ttu-id="84159-139">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="84159-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="84159-140">-VMSize</span></span>
<span data-ttu-id="84159-141">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="84159-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="84159-142">-Zone</span></span>
<span data-ttu-id="84159-143">Określa listę stref dostępności dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="84159-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="84159-144">Dozwolone wartości są zależne od możliwości obszaru tego regionu.</span><span class="sxs-lookup"><span data-stu-id="84159-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="84159-145">Dozwolone wartości będą zwykle 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="84159-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="84159-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84159-146">CommonParameters</span></span>
<span data-ttu-id="84159-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84159-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84159-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84159-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84159-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84159-149">INPUTS</span></span>

### <span data-ttu-id="84159-150">System. String</span><span class="sxs-lookup"><span data-stu-id="84159-150">System.String</span></span>

### <span data-ttu-id="84159-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="84159-151">System.String[]</span></span>

### <span data-ttu-id="84159-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84159-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="84159-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84159-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84159-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84159-154">OUTPUTS</span></span>

### <span data-ttu-id="84159-155">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="84159-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="84159-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84159-156">NOTES</span></span>

## <span data-ttu-id="84159-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84159-157">RELATED LINKS</span></span>

[<span data-ttu-id="84159-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="84159-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="84159-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="84159-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="84159-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="84159-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="84159-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="84159-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


