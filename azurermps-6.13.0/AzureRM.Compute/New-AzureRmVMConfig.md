---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548839"
---
# <span data-ttu-id="1793c-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="1793c-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="1793c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1793c-102">SYNOPSIS</span></span>
<span data-ttu-id="1793c-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1793c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1793c-104">SYNTAX</span></span>

### <span data-ttu-id="1793c-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1793c-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1793c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1793c-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1793c-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="1793c-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1793c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1793c-108">DESCRIPTION</span></span>
<span data-ttu-id="1793c-109">Polecenie cmdlet **New-AzureRmVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1793c-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="1793c-110">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface i Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="1793c-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="1793c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1793c-111">EXAMPLES</span></span>

### <span data-ttu-id="1793c-112">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1793c-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="1793c-113">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="1793c-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1793c-114">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1793c-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1793c-115">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1793c-116">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="1793c-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="1793c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1793c-117">PARAMETERS</span></span>

### <span data-ttu-id="1793c-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1793c-118">-AssignIdentity</span></span>
<span data-ttu-id="1793c-119">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="1793c-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="1793c-120">-AvailabilitySetId</span></span>
<span data-ttu-id="1793c-121">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="1793c-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="1793c-122">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="1793c-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="1793c-123">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="1793c-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="1793c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1793c-124">-DefaultProfile</span></span>
<span data-ttu-id="1793c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1793c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1793c-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="1793c-126">-EnableUltraSSD</span></span>
<span data-ttu-id="1793c-127">Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="1793c-128">Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.</span><span class="sxs-lookup"><span data-stu-id="1793c-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="1793c-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="1793c-129">-IdentityId</span></span>
<span data-ttu-id="1793c-130">Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="1793c-131">Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="1793c-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="1793c-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1793c-132">-IdentityType</span></span>
<span data-ttu-id="1793c-133">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="1793c-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="1793c-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1793c-134">-LicenseType</span></span>
<span data-ttu-id="1793c-135">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="1793c-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="1793c-136">-Tagi</span><span class="sxs-lookup"><span data-stu-id="1793c-136">-Tags</span></span>
<span data-ttu-id="1793c-137">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="1793c-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="1793c-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="1793c-138">-VMName</span></span>
<span data-ttu-id="1793c-139">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="1793c-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="1793c-140">-VMSize</span></span>
<span data-ttu-id="1793c-141">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="1793c-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="1793c-142">-Zone</span></span>
<span data-ttu-id="1793c-143">Określa listę stref dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1793c-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="1793c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1793c-144">CommonParameters</span></span>
<span data-ttu-id="1793c-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1793c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1793c-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1793c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1793c-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1793c-147">INPUTS</span></span>

### <span data-ttu-id="1793c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1793c-148">System.String</span></span>

### <span data-ttu-id="1793c-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="1793c-149">System.String[]</span></span>

### <span data-ttu-id="1793c-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1793c-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1793c-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1793c-151">OUTPUTS</span></span>

### <span data-ttu-id="1793c-152">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1793c-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1793c-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1793c-153">NOTES</span></span>

## <span data-ttu-id="1793c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1793c-154">RELATED LINKS</span></span>

[<span data-ttu-id="1793c-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1793c-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="1793c-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1793c-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="1793c-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="1793c-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="1793c-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1793c-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


