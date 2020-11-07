---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898981"
---
# <span data-ttu-id="67c1e-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="67c1e-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="67c1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="67c1e-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67c1e-104">SYNTAX</span></span>

### <span data-ttu-id="67c1e-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67c1e-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67c1e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c1e-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67c1e-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c1e-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67c1e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="67c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="67c1e-109">Polecenie cmdlet **New-AzureRmVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="67c1e-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="67c1e-110">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface i Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="67c1e-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="67c1e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67c1e-111">EXAMPLES</span></span>

### <span data-ttu-id="67c1e-112">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="67c1e-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="67c1e-113">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67c1e-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="67c1e-114">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="67c1e-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="67c1e-115">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="67c1e-116">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67c1e-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="67c1e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67c1e-117">PARAMETERS</span></span>

### <span data-ttu-id="67c1e-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="67c1e-118">-AssignIdentity</span></span>
<span data-ttu-id="67c1e-119">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="67c1e-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="67c1e-120">-AvailabilitySetId</span></span>
<span data-ttu-id="67c1e-121">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="67c1e-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="67c1e-122">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67c1e-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="67c1e-123">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="67c1e-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="67c1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c1e-124">-DefaultProfile</span></span>
<span data-ttu-id="67c1e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67c1e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c1e-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="67c1e-126">-IdentityId</span></span>
<span data-ttu-id="67c1e-127">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="67c1e-128">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="67c1e-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="67c1e-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="67c1e-129">-IdentityType</span></span>
<span data-ttu-id="67c1e-130">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="67c1e-130">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="67c1e-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="67c1e-131">-LicenseType</span></span>
<span data-ttu-id="67c1e-132">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="67c1e-132">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="67c1e-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="67c1e-133">-Tags</span></span>
<span data-ttu-id="67c1e-134">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="67c1e-134">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="67c1e-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="67c1e-135">-VMName</span></span>
<span data-ttu-id="67c1e-136">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="67c1e-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="67c1e-137">-VMSize</span></span>
<span data-ttu-id="67c1e-138">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="67c1e-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="67c1e-139">-Zone</span></span>
<span data-ttu-id="67c1e-140">Określa listę stref dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67c1e-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="67c1e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c1e-141">CommonParameters</span></span>
<span data-ttu-id="67c1e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c1e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c1e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c1e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c1e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67c1e-144">INPUTS</span></span>

### <span data-ttu-id="67c1e-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="67c1e-145">None</span></span>
<span data-ttu-id="67c1e-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="67c1e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67c1e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67c1e-147">OUTPUTS</span></span>

### <span data-ttu-id="67c1e-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="67c1e-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="67c1e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67c1e-149">NOTES</span></span>

## <span data-ttu-id="67c1e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67c1e-150">RELATED LINKS</span></span>

[<span data-ttu-id="67c1e-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67c1e-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="67c1e-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67c1e-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="67c1e-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="67c1e-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="67c1e-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="67c1e-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


