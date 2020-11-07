---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893625"
---
# <span data-ttu-id="8d6ab-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8d6ab-101">New-AzVMConfig</span></span>

## <span data-ttu-id="8d6ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6ab-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="8d6ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d6ab-104">SYNTAX</span></span>

### <span data-ttu-id="8d6ab-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d6ab-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d6ab-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6ab-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d6ab-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6ab-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d6ab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8d6ab-108">DESCRIPTION</span></span>
<span data-ttu-id="8d6ab-109">Polecenie cmdlet **New-AzVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="8d6ab-110">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="8d6ab-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d6ab-111">EXAMPLES</span></span>

### <span data-ttu-id="8d6ab-112">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8d6ab-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="8d6ab-113">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="8d6ab-114">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8d6ab-115">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8d6ab-116">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="8d6ab-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d6ab-117">PARAMETERS</span></span>

### <span data-ttu-id="8d6ab-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8d6ab-118">-AssignIdentity</span></span>
<span data-ttu-id="8d6ab-119">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="8d6ab-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="8d6ab-120">-AvailabilitySetId</span></span>
<span data-ttu-id="8d6ab-121">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="8d6ab-122">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="8d6ab-123">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6ab-124">-DefaultProfile</span></span>
<span data-ttu-id="8d6ab-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d6ab-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="8d6ab-126">-IdentityId</span></span>
<span data-ttu-id="8d6ab-127">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="8d6ab-128">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="8d6ab-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="8d6ab-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8d6ab-129">-IdentityType</span></span>
<span data-ttu-id="8d6ab-130">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6ab-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d6ab-131">-LicenseType</span></span>
<span data-ttu-id="8d6ab-132">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6ab-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="8d6ab-133">-Tags</span></span>
<span data-ttu-id="8d6ab-134">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6ab-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d6ab-135">-VMName</span></span>
<span data-ttu-id="8d6ab-136">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6ab-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="8d6ab-137">-VMSize</span></span>
<span data-ttu-id="8d6ab-138">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="8d6ab-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="8d6ab-139">-Zone</span></span>
<span data-ttu-id="8d6ab-140">Określa listę stref dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="8d6ab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6ab-141">CommonParameters</span></span>
<span data-ttu-id="8d6ab-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6ab-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6ab-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6ab-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d6ab-144">INPUTS</span></span>

### <span data-ttu-id="8d6ab-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8d6ab-145">None</span></span>
<span data-ttu-id="8d6ab-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8d6ab-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d6ab-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d6ab-147">OUTPUTS</span></span>

### <span data-ttu-id="8d6ab-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d6ab-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8d6ab-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d6ab-149">NOTES</span></span>

## <span data-ttu-id="8d6ab-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d6ab-150">RELATED LINKS</span></span>

[<span data-ttu-id="8d6ab-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d6ab-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="8d6ab-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8d6ab-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="8d6ab-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="8d6ab-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="8d6ab-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8d6ab-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


