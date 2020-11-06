---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553979"
---
# <span data-ttu-id="98d46-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="98d46-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="98d46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98d46-102">SYNOPSIS</span></span>
<span data-ttu-id="98d46-103">Tworzy konfigurowalny obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98d46-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d46-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98d46-105">DESCRIPTION</span></span>
<span data-ttu-id="98d46-106">Polecenie cmdlet **New-AzureRmVMConfig** tworzy konfigurowalny lokalny obiekt maszyny wirtualnej dla platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98d46-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="98d46-107">Innych poleceń cmdlet można użyć w celu skonfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface i Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="98d46-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="98d46-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98d46-108">EXAMPLES</span></span>

### <span data-ttu-id="98d46-109">Przykład 1. Tworzenie obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="98d46-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="98d46-110">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="98d46-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="98d46-111">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="98d46-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="98d46-112">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="98d46-113">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="98d46-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="98d46-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98d46-114">PARAMETERS</span></span>

### <span data-ttu-id="98d46-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="98d46-115">-AssignIdentity</span></span>
<span data-ttu-id="98d46-116">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="98d46-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="98d46-117">-AvailabilitySetId</span></span>
<span data-ttu-id="98d46-118">Określa identyfikator zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="98d46-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="98d46-119">Aby uzyskać obiekt zestawu dostępności, użyj polecenia cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="98d46-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="98d46-120">Obiekt zestawu dostępności zawiera Właściwość ID.</span><span class="sxs-lookup"><span data-stu-id="98d46-120">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="98d46-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d46-121">-DefaultProfile</span></span>
<span data-ttu-id="98d46-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98d46-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d46-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="98d46-123">-IdentityType</span></span>
<span data-ttu-id="98d46-124">Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="98d46-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d46-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="98d46-125">-LicenseType</span></span>
<span data-ttu-id="98d46-126">Typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.</span><span class="sxs-lookup"><span data-stu-id="98d46-126">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="98d46-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="98d46-127">-Tags</span></span>
<span data-ttu-id="98d46-128">Znaczniki dołączone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="98d46-128">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="98d46-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="98d46-129">-VMName</span></span>
<span data-ttu-id="98d46-130">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-130">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="98d46-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="98d46-131">-VMSize</span></span>
<span data-ttu-id="98d46-132">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-132">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="98d46-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="98d46-133">-Zone</span></span>
<span data-ttu-id="98d46-134">Określa listę stref dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98d46-134">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="98d46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d46-135">CommonParameters</span></span>
<span data-ttu-id="98d46-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d46-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d46-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d46-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98d46-138">INPUTS</span></span>

## <span data-ttu-id="98d46-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98d46-139">OUTPUTS</span></span>

## <span data-ttu-id="98d46-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98d46-140">NOTES</span></span>

## <span data-ttu-id="98d46-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98d46-141">RELATED LINKS</span></span>

[<span data-ttu-id="98d46-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="98d46-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="98d46-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="98d46-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="98d46-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="98d46-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="98d46-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="98d46-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


