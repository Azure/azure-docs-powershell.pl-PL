---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238599"
---
# <span data-ttu-id="999c1-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="999c1-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="999c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="999c1-102">SYNOPSIS</span></span>
<span data-ttu-id="999c1-103">Ustawia właściwości profilu magazynu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="999c1-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="999c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="999c1-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="999c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="999c1-105">DESCRIPTION</span></span>
<span data-ttu-id="999c1-106">Polecenie **cmdlet Set-AzVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skal maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="999c1-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="999c1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="999c1-107">EXAMPLES</span></span>

### <span data-ttu-id="999c1-108">Przykład 1. Ustawianie właściwości profilu magazynu dla usługi maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="999c1-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="999c1-109">To polecenie ustawia właściwości profilu magazynu dla maszyn wirtualnych o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="999c1-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="999c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="999c1-110">PARAMETERS</span></span>

### <span data-ttu-id="999c1-111">-DataDrive</span><span class="sxs-lookup"><span data-stu-id="999c1-111">-DataDisk</span></span>
<span data-ttu-id="999c1-112">Określa obiekt dysku danych.</span><span class="sxs-lookup"><span data-stu-id="999c1-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999c1-113">-DefaultProfile</span></span>
<span data-ttu-id="999c1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="999c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="999c1-115">-Diff Diff DiffSetting</span><span class="sxs-lookup"><span data-stu-id="999c1-115">-DiffDiskSetting</span></span>
<span data-ttu-id="999c1-116">Określa różne ustawienia dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="999c1-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="999c1-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="999c1-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="999c1-118">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="999c1-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="999c1-119">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="999c1-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="999c1-120">— Obraz</span><span class="sxs-lookup"><span data-stu-id="999c1-120">-Image</span></span>
<span data-ttu-id="999c1-121">Określa identyfikator URI obiektu blob dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="999c1-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="999c1-122">Narzędzie MASZYNY.WIRTUALNE tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="999c1-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="999c1-123">-ImageReferenceId</span></span>
<span data-ttu-id="999c1-124">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="999c1-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="999c1-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="999c1-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="999c1-126">Określa typ oferty obrazu maszyny wirtualnej (VIRTUALImage).</span><span class="sxs-lookup"><span data-stu-id="999c1-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="999c1-127">Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="999c1-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="999c1-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="999c1-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="999c1-129">Określa nazwę wydawcy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="999c1-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="999c1-130">Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="999c1-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="999c1-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="999c1-131">-ImageReferenceSku</span></span>
<span data-ttu-id="999c1-132">Określa wartość SKU MASZYNY.WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="999c1-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="999c1-133">Aby uzyskać jednostki SKU, użyj Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="999c1-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="999c1-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="999c1-135">Określa wersję programu VMImage.</span><span class="sxs-lookup"><span data-stu-id="999c1-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="999c1-136">Aby użyć najnowszej wersji, określ wartość najnowszej zamiast określonej wersji.</span><span class="sxs-lookup"><span data-stu-id="999c1-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="999c1-137">-Managed Jednak</span><span class="sxs-lookup"><span data-stu-id="999c1-137">-ManagedDisk</span></span>
<span data-ttu-id="999c1-138">Określa dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="999c1-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="999c1-139">-OsDriveCaching</span><span class="sxs-lookup"><span data-stu-id="999c1-139">-OsDiskCaching</span></span>
<span data-ttu-id="999c1-140">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="999c1-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="999c1-141">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="999c1-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="999c1-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="999c1-142">ReadOnly</span></span>
- <span data-ttu-id="999c1-143">ReadWrite Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="999c1-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="999c1-144">Jeśli zmienisz wartość buforowania, polecenie cmdlet uruchomi ponownie maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="999c1-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="999c1-145">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="999c1-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-146">-OsCreateOption</span><span class="sxs-lookup"><span data-stu-id="999c1-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="999c1-147">Określa sposób, w jaki to polecenie cmdlet tworzy maszyny wirtualne MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="999c1-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="999c1-148">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="999c1-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="999c1-149">Dołączanie: ta wartość jest używana podczas tworzenia maszyny wirtualnej MASZYNY WIRTUALNEJ przy użyciu dysku specjalistycznego.</span><span class="sxs-lookup"><span data-stu-id="999c1-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="999c1-150">FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej MASZYNY WIRTUALNEJ za pomocą obrazu.</span><span class="sxs-lookup"><span data-stu-id="999c1-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="999c1-151">Jeśli używasz obrazu platformy, będziesz również używać *parametru imageReference.*</span><span class="sxs-lookup"><span data-stu-id="999c1-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-152">-Os Jednakowa_nazwa</span><span class="sxs-lookup"><span data-stu-id="999c1-152">-OsDiskName</span></span>
<span data-ttu-id="999c1-153">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="999c1-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-154">-OsDriveOsType</span><span class="sxs-lookup"><span data-stu-id="999c1-154">-OsDiskOsType</span></span>
<span data-ttu-id="999c1-155">Określa typ systemu operacyjnego na dysku.</span><span class="sxs-lookup"><span data-stu-id="999c1-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="999c1-156">Jest ona potrzebna tylko w przypadku scenariuszy obrazów użytkowników, a nie dla obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="999c1-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-157">-Os JednakowyAccelerator</span><span class="sxs-lookup"><span data-stu-id="999c1-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="999c1-158">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="999c1-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-159">- VhdContainer</span><span class="sxs-lookup"><span data-stu-id="999c1-159">-VhdContainer</span></span>
<span data-ttu-id="999c1-160">Określa adresy URL kontenera używane do przechowywania dysków systemu operacyjnego dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="999c1-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="999c1-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="999c1-162">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="999c1-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="999c1-163">Aby uzyskać obiekt, użyj New-AzVmssConfig obiektu.</span><span class="sxs-lookup"><span data-stu-id="999c1-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="999c1-164">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="999c1-164">-Confirm</span></span>
<span data-ttu-id="999c1-165">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="999c1-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="999c1-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999c1-166">-WhatIf</span></span>
<span data-ttu-id="999c1-167">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="999c1-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="999c1-168">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="999c1-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="999c1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999c1-169">CommonParameters</span></span>
<span data-ttu-id="999c1-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="999c1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999c1-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="999c1-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999c1-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="999c1-172">INPUTS</span></span>

### <span data-ttu-id="999c1-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="999c1-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="999c1-174">System.String</span><span class="sxs-lookup"><span data-stu-id="999c1-174">System.String</span></span>

### <span data-ttu-id="999c1-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="999c1-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="999c1-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="999c1-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="999c1-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="999c1-177">System.String[]</span></span>

### <span data-ttu-id="999c1-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDataDla]</span><span class="sxs-lookup"><span data-stu-id="999c1-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="999c1-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="999c1-179">OUTPUTS</span></span>

### <span data-ttu-id="999c1-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="999c1-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="999c1-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="999c1-181">NOTES</span></span>

## <span data-ttu-id="999c1-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="999c1-182">RELATED LINKS</span></span>

[<span data-ttu-id="999c1-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="999c1-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="999c1-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="999c1-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="999c1-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="999c1-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="999c1-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="999c1-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


